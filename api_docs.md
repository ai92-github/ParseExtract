## APIs:
`Below you will find API usage examples using python with details given for various request parameters.`

`We are in process to add other languages. Till then we request you to use any LLM to create an equivalent script in your required language.`

* 🌐[Webpage / URL Scraping API](#webpage--url-scraping)
  - [Sync](#sync-api-call)
  - [Async](#async-api-call)
  - [Request Parameters](#request-parameters)


* 🕷️[Webpage / URL Crawling API](#%EF%B8%8Fwebpage--url-crawling)
  - [Sync](#sync-api-call-1)
  - [Async](#async-api-call-1)
  - [Fetch Results API](#fetch-results-using-the-job_id)
  - [Request Parameters](#request-parameters-1)

* 📑[PDF / Docx Parsing](#pdf--docx-parsing)
  - [Sync](#sync-api-call-2)
  - [Async](#async-api-call-2)
  - [Fetch Results API](#fetch-results-using-the-job_id-for-documents-with-more-than-5-pages)
  - [Form Data Parameters](#form-data-parameters)


* 🎞️[Image / Scanned Document Parsing](#%EF%B8%8Fimage--scanned-document-parsing)
  - [Sync](#sync-api-call-3)
  - [Async](#async-api-call-3)
  - [Form Data Parameters](#form-data-parameters-1)


* 𝄜 [Table Extraction](#table-extraction)
  - [Sync](#sync-api-call-4)
  - [Async](#async-api-call-4)
  - [Save Tables as Excel/csv](#save-tables-as-excelcsv)
  - [Form Data Parameters](#form-data-parameters-2)


* 🗃️[Structured Data Extraction](#%EF%B8%8Fstructured-data-extraction)
  - [Sync](#sync-api-call-5)
  - [Async](#async-api-call-5)
  - [Form Data Parameters](#form-data-parameters-3)

---

# 🌐Webpage / URL Scraping:

`API to Scrape a single url. For Crawling refer to:`[Crawling API](#%EF%B8%8Fwebpage--url-crawling)

### Sync API Call
```python
import requests

# API URL
api_url = "https://api.parseextract.com/v1/url-parse"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The URL to scrape
url = ""

# Other Parameters (refer table below for all available parameters)
wait = 1.5

# Timeouts
timeout = (10, 60) # 10 seconds connect, 60 seconds read

# Payload
payload = {"url":url, "wait":wait}  # add all other parameters

# POST Request (Sync)
response = requests.post(api_url, json=payload, headers=headers, timeout=timeout)

scraped_text = response.json().get('text','')
print(scraped_text)
```

### Async API Call
```python
import httpx

# API URL
api_url = "https://api.parseextract.com/v1/url-parse"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The URL to scrape
url = ""

# Other Parameters (refer table below for all available parameters)
wait = 1.5

# Payload
payload = {"url":url, "wait":wait}  # add all other parameters

# POST Request (Async)
async def parse_url_async(api_url, url=url, wait=wait):
    timeout = httpx.Timeout(10.0, read=60)
    async with httpx.AsyncClient() as client:
        response = await client.post(api_url, json=payload, headers=headers, timeout=timeout)
        return response

# response = await parse_url_async(api_url, url, wait)
# or use asyncio
import asyncio
async def get_response_async():
    response = await parse_url_async(api_url, url, wait)
    print(response.json().get('text',''))

# Run the async function
asyncio.run(get_response_async())
```
### Request Parameters:

| Name   | Description                              |
| -------- | ---------------------------------------- |
| `url`    | The url to scrape. |
| `wait`   | Time to wait for the page to load in seconds. Default: 1.5. Keep higher value for better results.|
| `keep_images`  | Keep image links. Default: True. If False, it will remove image links from the text if image link are not required while scraping, this saves tokens to be processed by the LLM.|
| `remove_svg_image`    | Remove .svg image. usually .svg files are not required while scraping. Default: True |
| `remove_gif_image`    | Remove .gif image. usually .gif files are not required while scraping. Default: True |
| `remove_image_types` | Add any image extensions which you want to remove inside a list. eg: ['.png', '.jpg']. Default [ ] |
| `keep_webpage_links`    | Keep webpage links. If scraping job does not require links then can remove them to reduce input token count to LLM. Default True (i.e. keep webpage links)|
| `remove_script_tag`   | Default: True |
| `remove_style_tag`  | Default: True |
| `remove_tags`    | List of tags to be remove. Default [ ] |

* [Back to Table of Contents](#apis)

---

## 🕷️Webpage / URL Crawling:

`You will get a job_id in the response which will be used to fetch the output using the `[/fetchcrawloutput](#fetch-results-using-the-job_id)` API`

### Sync API Call
```python
import requests

# API URL
api_url = "https://api.parseextract.com/v1/url-crawl"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The URL to crawl
url = ""

# Other Parameters (refer table below for all available parameters)
wait = 1.5
crawl_limit = 1000

# Timeouts
timeout = (10, 10) # 10 seconds connect, 10 seconds read

# Payload
payload = {"url":url, "wait":wait, 'crawl_limit":crawl_limit}  # add all other parameters

# POST Request (Sync)
response = requests.post(api_url, json=payload, headers=headers, timeout=timeout)
print(response.json())
```

### Async API Call
```python
import httpx

# API URL
api_url = "https://api.parseextract.com/v1/url-crawl"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The URL to crawl
url = ""

# Other Parameters (refer table below for all available parameters)
wait = 1.5
crawl_limit = 1000

# Payload
payload = {"url":url, "wait":wait, "crawl_limit":crawl_limit}  # add all other parameters

# POST Request (Async)
async def crawl_url_async(api_url, url=url, wait=wait, crawl_limit=crawl_limit):
    timeout = httpx.Timeout(10.0, read=60)
    async with httpx.AsyncClient() as client:
        response = await client.post(api_url, json=payload, headers=headers, timeout=timeout)
        return response

# response = await crawl_url_async(api_url, url, wait, crawl_limit)
# or use asyncio
import asyncio
async def get_response_async():
    response = await crawl_url_async(api_url, url, wait, crawl_limit)
    print(response.json())

# Run the async function
asyncio.run(get_response_async())
```

### Fetch Results using the job_id
```python
import requests

# Job ID
job_id = 'the-job-id-from-the-url-crawl-endpoint'

# API URL
# Add the job id as the query string parameter
api_url = f"https://api.parseextract.com/v1/fetchcrawloutput?job_id={job_id}"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# GET Request
response = requests.get(api_url, headers=headers)
print(response.json().get('output',''))
```

### Request Parameters:

| Name   | Description                              |
| -------- | ---------------------------------------- |
| `url`    | The url to crawl. |
| `wait`   | Time to wait for the page to load in seconds. Default: 1.5. Keep higher value for better results.|
| `include_parent_url`    | This will crawl all the sub directories of the parent url. Default: True. e.g. if the url is example.com then it will crawl all sub directories like example.com/abc, example.com/abc/xyz |
| `include_keyword`   | If the url has this keyword it will be added for crawling. `Note:` It's better to use the 'include_path' parameter that accepts regex pattern instaed of this raw keyword match. If you happen to give keyword like instagram and give max_depth=2 then it will extract unwanted instagram url when it crawls to depth 2. Refer below parameters to more details.  Default: [ ] |
| `exclude_keyword`  | Same function as the 'include_keyword' but this excludes urls having the keyword. Default: [ ] |
| `include_path`    | Include urls matching the regex pattern. Give all patterns inside a list. e.g. [".\*/blog/\*"].  Default: [ ] |
| `exclude_path`    | Similar to above but this will exclude such urls.  Default: [ ] |
| `max_depth` | Depth of crawling required. if max_depth=0, it will scrape only the url given. If max_depth=1, then it will scarpe all the urls available from the parent url based on the inclusion/exclusion conditions given from the above parameters. More depth will repeat the cycle until crawl_limit is reached or crawling is over. Default: 2 |
| `crawl_limit`    | Maximum no. of urls to scrape while crawling. Default: 1000 |
| `keep_images`  | Keep image links. Default: True. If False, it will remove image links from the text if image link are not required while scraping, this saves tokens to be processed by the LLM.|
| `remove_svg_image`    | Remove .svg image. usually .svg files are not required while scraping. Default: True |
| `remove_gif_image`    | Remove .gif image. usually .gif files are not required while scraping. Default: True |
| `remove_image_types` | Add any image extensions which you want to remove inside a list. eg: ['.png', '.jpg']. Default [ ] |
| `keep_webpage_links`    | Keep webpage links. If scraping job does not require links then can remove them to reduce input token count to LLM. Default True (i.e. keep webpage links)|
| `remove_script_tag`   | Default: True |
| `remove_style_tag`  | Default: True |
| `remove_tags`    | List of tags to be remove. Default [ ] |

* [Back to Table of Contents](#apis)

---

## 📑PDF / Docx Parsing:

`When the no. of pages are more than 5 then you will get a job_id and for less than or equal to 5 pages you will get the parsed output in the response of the same API call.`

`You will have to use the `[/fetchparseoutput](#fetch-results-using-the-job_id-for-documents-with-more-than-5-pages)` API to fetch the parsed output using the job_id.`

### Sync API Call
```python
import requests

# API URL
api_url = "https://api.parseextract.com/v1/pdf-parse"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The pdf/docx file path or url
pdf_file_path = 'your-pdf-or-docx-file-path.pdf or url'

# Other Form Data Parameters (refer table below for all available parameters)
pdf_option = 'option_b'
inline_images = True
get_base64_images = True

# Timeouts
timeout = (10, 300) # 10 seconds connect, 60 seconds read

# Payload
payload = {"pdf_option":pdf_option, "inline_images":inline_images, "get_base64_images':get_base64_images}  # add all other parameters

# POST Request (Sync)
# We send the file and all parameters as multi-form data
with open(pdf_file_path, 'rb') as f:
    files = {'file': (pdf_file_path, f)}
    response = requests.post(api_url, files=files, data=payload, headers=headers, timeout=timeout)

parsed_text = response.json().get('text','')
extracted_images = response.json().get('images','')
job_id = response.json().get('job_id','')
print(parsed_text)
print(extracted_images)
print(job_id)
```

### Async API Call
```python
import httpx

# API URL
api_url = "https://api.parseextract.com/v1/pdf-parse"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The pdf/docx file path or url
pdf_file_path = 'your-pdf-or-docx-file-path.pdf or url'

# Other Form Data Parameters (refer table below for all available parameters)
pdf_option = 'option_b'
inline_images = True
get_base64_images = True

# Payload
payload = {"pdf_option":pdf_option, "inline_images":inline_images, "get_base64_images':get_base64_images}  # add all other parameters

# POST Request (Async)
# We send the file and all parameters as multi-form data
async def parse_pdf_async(api_url, pdf_file_path, pdf_option, inline_images, get_base64_images):
    async with aiofiles.open(pdf_file_path, 'rb') as file:
        file_content = await file.read()
        files = {'file': (pdf_file_path, file_content)}
        timeout = httpx.Timeout(10, read=300)
        async with httpx.AsyncClient() as client:
            response = await client.post(api_url, files=files, data=payload, headers=headers, timeout=timeout)
            return response

# response = await parse_pdf_async(api_url, pdf_file_path, pdf_option, inline_images, get_base64_images)
# or use asyncio
import asyncio
async def get_response_async():
    response = await parse_pdf_async(api_url, pdf_file_path, pdf_option, inline_images, get_base64_images)
    print(response.json().get('text',''))
    print(response.json().get('images',''))
    print(response.json().get('job_id',''))

# Run the async function
asyncio.run(get_response_async())
```

### Fetch Results using the job_id (for documents with more than 5 pages)
```python
import requests

# Job ID
job_id = 'the-job-id-from-the-pdf-parse-endpoint'

# API URL
# Add the job id as the query string parameter
api_url = f"https://api.parseextract.com/v1/fetchoutput?job_id={job_id}"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# GET Request
response = requests.get(api_url, headers=headers)
print(response.json().get('text',''))
print(response.json().get('images',''))
```

### Form Data Parameters:

| Name   | Description                              |
| -------- | ---------------------------------------- |
| `files`    | The pdf/docx file. Refer the above example for usage. |
| `url`   | The pdf url (you can either use file upload or give a url) |
| `pdf_option`  | either 'option_a' or 'option_b'. Default: 'option_b'. Refer www.parseextract.com/#FAQ for more details. |
| `inline_images`    | Should the images ID be added inline with the text in the same position as they appear in the document. Default: True |
| `get_base64_images`    | Get the extracted images as base64 strings. At present only the base64 encoded string is available if you want to save the images locally. Default: True |

* [Back to Table of Contents](#apis)

---

## 🎞️Image / Scanned Document Parsing:

### Sync API Call
```python
import requests

# API URL
api_url = "https://api.parseextract.com/v1/image-parse"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The pdf/docx file path or url
image_file_path = 'your-image-file-path.pdf or url'

# Other Form Data Parameters (refer table below for all available parameters)
image_option = 'option_b'

# Timeouts
timeout = (10, 60) # 10 seconds connect, 60 seconds read

# Payload
payload = {"image_option":image_option}  # add all other parameters

# POST Request (Sync)
# We send the file and all parameters as multi-form data
with open(image_file_path, 'rb') as f:
    files = {'file': (image_file_path, f)}
    response = requests.post(api_url, files=files, data=payload, headers=headers, timeout=timeout)

parsed_text = response.json().get('text','')
print(parsed_text)
```

### Async API Call
```python
import httpx

# API URL
api_url = "https://api.parseextract.com/v1/image-parse"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The pdf/docx file path or url
image_file_path = 'your-image-file-path or url'

# Other Form Data Parameters (refer table below for all available parameters)
image_option = 'option_b'

# Payload
payload = {"image_option":image_option}  # add all other parameters

# POST Request (Async)
# We send the file and all parameters as multi-form data
async def parse_image_async(api_url, image_file_path, image_option):
    async with aiofiles.open(pdf_file_path, 'rb') as file:
        file_content = await file.read()
        files = {'file': (image_file_path, file_content)}
        timeout = httpx.Timeout(10, read=60)
        async with httpx.AsyncClient() as client:
            response = await client.post(api_url, files=files, data=payload, headers=headers, timeout=timeout)
            return response

# response = await parse_image_async(api_url, image_file_path, pdf_option)
# or use asyncio
import asyncio
async def get_response_async():
    response = await parse_image_async(api_url, image_file_path, image_option)
    print(response.json().get('text',''))

# Run the async function
asyncio.run(get_response_async())
```

### Form Data Parameters:

| Name   | Description                              |
| -------- | ---------------------------------------- |
| `files`    | The image file. Refer the above example for usage. |
| `url`   | The image url (you can either use file upload or give a url) |
| `image_option`  | either 'option_a' or 'option_b'. Default: 'option_b'. Refer www.parseextract.com/#FAQ for more details. |

* [Back to Table of Contents](#apis)

---

## 𝄜Table Extraction:

`It will extract all the tables and tabular data from pdf, docx, images. The API response will have excel and csv file as base64 encoded strings which you can decode to excel and csv files.`

`Note:` If the no. of pages in the document is more than 1 then you will get a job_id in the API response with estimated time. You can later use the `/fetch-table-extract` API to get the status and output using the job_id. If you pass a single page document or multi-page document but with a page_no or a single image (multiple image is not supported) then you will receive the output in the same API response without any job_id.

### Sync API Call
```python
import requests

# API URL
api_url = "https://api.parseextract.com/v1/table-extract"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The pdf/docx/image file path
file_path = 'your-file-path'

# Timeouts
timeout = (10, 60) # 10 seconds connect, 60 seconds read

# POST Request (Sync)
# We send the file as multi-form data
with open(file_path, 'rb') as f:
    files = {'file': (file_path, f)}
    response = requests.post(api_url, files=files, headers=headers, timeout=timeout)

print(response.json())
if response.json().get('job_id','')!='':
  print(f'Extraction in process. {response.json().get('tables','')})
```

### Async API Call
```python
import httpx

# API URL
api_url = "https://api.parseextract.com/v1/table-extract"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The pdf/docx file path
file_path = 'your-file-path'

# POST Request (Async)
# We send the file and all parameters as multi-form data
async def extract_table_async(api_url, file_path):
    async with aiofiles.open(file_path, 'rb') as file:
        file_content = await file.read()
        files = {'file': (file_path, file_content)}
        timeout = httpx.Timeout(10, read=60)
        async with httpx.AsyncClient() as client:
            response = await client.post(api_url, files=files, headers=headers, timeout=timeout)
            return response

# response = await extract_table_async(api_url, file_path)
# or use asyncio
import asyncio
async def get_response_async():
    response = await extract_table_async(api_url, file_path)
    print(response.json())
    if response.json().get('job_id','')!='':
      print(f'Extraction in process. {response.json().get('tables','')})

# Run the async function
asyncio.run(get_response_async())
```

### Fetch Extracted Table using job_id (for multi-page documents)
```python
import requests

# Job ID
job_id = response.json().get('job_id','')  # the-job-id-from-the-table-extract-endpoint

# API URL
# Add the job id as the query string parameter
api_url = f"https://api.parseextract.com/v1/fetch-table-extract?job_id={job_id}"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# GET Request
response = requests.get(api_url, headers=headers)
print(response.json())
```

### Save Tables as Excel/csv:
```python
import json, base64

api_response = response.json()

# get excel and csv files to download from the response
try:
  file_to_download = json.loads(api_response.get('file_to_download',[]))
except:
  file_to_download = []

# You can set download_excel or download_csv = False if you do not need any one of them
download_excel = True
download_csv = True

# saving excel / csv files
if file_to_download!=[]:
  for table_data in file_to_download:
    output_filename =  table_data['id']
    if not download_excel and table_data['id'].endswith('.xlsx'):
      continue
    if not download_csv and table_data['id'].endswith('.csv'):
      continue
    decoded_bytes = base64.b64decode(table_data['base64_string'])
    with open(output_filename, "wb") as f:
        f.write(decoded_bytes)
    print(f"{output_filename} created successfully from Base64 data.")
else:
  print('No files to download')
```

### Form Data Parameters:

| Name   | Description                              |
| -------- | ---------------------------------------- |
| `files`    | The document file. Refer the above example for usage. |
| `extraction_option`    | Either 'option_a' or 'option_b'. Default is 'option_b' |
| `page_no`    | If you want to extract any single page_no. the value should be an integer. Default: None |

* [Back to Table of Contents](#apis)

---

## 🗃️Structured Data Extraction:

`Just mention in the prompt what you want to extract from the uploaded pdf, docx, image file. Add a schema in the same prompt to get output in your required format.`

`Note:` At present it does not support multi-page pdf/docx file. If you upload multi-page documents it will only extract data from the 1st page. Contact Us for multi-page support.

### Sync API Call
```python
import requests

# API URL
api_url = "https://api.parseextract.com/v1/data-extract"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The pdf/docx/image file path
file_path = 'your-file-path'  # if you have a url then pass the url as a separate form data and ignore the files input

# Other Form Data Parameters (refer table below for all available parameters)
prompt = 'your-extraction-prompt-with-a-optional-schema'
url = 'the-url-from-which-data-is-to-be-extracted'

# Timeouts
timeout = (10, 120) # 10 seconds connect, 60 seconds read

# Payload
payload = {"prompt":prompt}  # add url to the payload if your input is an url

# POST Request (Sync)
# We send the file and all parameters as multi-form data
with open(file_path, 'rb') as f:
    files = {'file': (file_path, f)}
    response = requests.post(api_url, files=files, data=payload, headers=headers, timeout=timeout)

print(response.json())
```

### Async API Call
```python
import httpx

# API URL
api_url = "https://api.parseextract.com/v1/data-extract"

# Authorization
api_key = os.environ["PARSEEXTRACT_API_KEY"]
headers = {"Authorization":f"Bearer {api_key}"}

# The pdf/docx/image file path
file_path = 'your-file-path'  # if you have a url then pass the url as a separate form data and ignore the files input

# Other Form Data Parameters (refer table below for all available parameters)
prompt = 'your-extraction-prompt-with-a-optional-schema'
url = 'the-url-from-which-data-is-to-be-extracted'

# Payload
payload = {"prompt":prompt}  # add url to the payload if your input is an url

# POST Request (Async)
# We send the file and all parameters as multi-form data
async def extract_data_async(api_url, image_file_path, image_option):
    async with aiofiles.open(pdf_file_path, 'rb') as file:
        file_content = await file.read()
        files = {'file': (file_path, file_content)}
        timeout = httpx.Timeout(10, read=120)
        async with httpx.AsyncClient() as client:
            response = await client.post(api_url, files=files, data=payload, headers=headers, timeout=timeout)
            return response

# response = await extract_data_async(api_url, file_path)
# or use asyncio
import asyncio
async def get_response_async():
    response = await extract_data_async(api_url, file_path,)
    print(response.json())

# Run the async function
asyncio.run(get_response_async())
```

### Form Data Parameters:

| Name   | Description                              |
| -------- | ---------------------------------------- |
| `files`    | The document file. Refer the above example for usage. |
| `url`   | The url (you can either use file upload or give a url) |
| `prompt`  | Your extraction prompt. Describe what you want to extract. Give a json schema example in the prompt string as plain text if required. |

* [Back to Table of Contents](#apis)

---

