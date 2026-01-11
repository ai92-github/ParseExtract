## Sample Output:

`Below we have provided some sample outputs.` You may [contact us](https://parseextract.com/#contact) for any `custom solutions.`

### Examples:

* 🌐[Webpage / URL Scraping or Crawling](#webpage--url-scraping-or-crawling)🕷️
  
* 📑[PDF / Docx Parsing](#pdf--docx-parsing)

* 🎞️[Image / Scanned Document Parsing](#image--scanned-document-parsing)

* 💲[Output Token Based Pricing Examples](#output-token-based-pricing-examples)
 
* 𝄜 [Table Extraction](#table-extraction)
 
* 🗃️[Structured Data Extraction](#structured-data-extraction)

---

## 🌐Webpage / URL Scraping or Crawling:

`The API is able to extract all the contents with webpage urls, image urls and complex tables (refer last table in the input link below)`

`The output is formatted for LLM input in such a way that it will consume less input tokens, resulting in cost saving for the downstream tasks`


`Input URL:` [https://afd.calpoly.edu/web/sample-tables](https://afd.calpoly.edu/web/sample-tables)

`Output LLM Ready Text:`

```markdown
  Skip to content: https://afd.calpoly.edu/web/sample-tables#content
      https://afd.calpoly.edu/framework/images/calpoly-logo-1x.png : http://www.calpoly.edu/

      Administration & Finance: https://afd.calpoly.edu/

          A&F Services: https://afd.calpoly.edu/services my CalPoly login: https://myportal.calpoly.edu
              Search

      A&F Web Support: https://afd.calpoly.edu/web/

        * Accessibility: https://wiki.calpoly.edu/display/usr/Web+Editing+-+Accessible+Documents
        * Style Guide: https://afd.calpoly.edu/web/style-guide
        * Request Website Changes: mailto:afd-web@calpoly.edu?subject=%5Bwebsite name%5D - %5Bdescriptor%5D
        * A&F Home: https://afd.calpoly.edu/
        * Web: https://afd.calpoly.edu/web/
        * Current: Sample Tables

      Sample Page - Data Tables

      For more information on creating accessible data tables see the Accessibility > Row and Column section of the Web Authoring Resource Center: http://warc.calpoly.edu/accessibility/508indepth/rowcolumn.html .

      Examples of Accessible Data Tables

      These example tables contain captions and summaries. When you copy any of these tables into your page you must edit the caption and summary. The caption can be edited in the Design view but the summary text must be edited in Code view. Click inside the table, then select the table tag on the tag selector, then switch to Code view and edit the text in the summary attribute.

      Basic Data Table with Column Headings


Table caption (name and description of table)
        You can describe your table here or in the context of your page.  
        This table is read using the first row as the header for each column.
        (Replace this caption with your own description of the table)
        
| Description | Date | Location: https://afd.calpoly.edu/web/sample-tables |
|---|---|---|
| Academic Senate Meeting | May 25, 2205 | Building 99 Room 1 |
| Commencement Meeting | December 15, 2205 | Building 42 Room 10 |
| Dean's Council | February 1, 2206 | Building 35 Room 5 |
| Committee on Committees | March 3, 2206 | Building 1 Room 201 |
| Lorem ipsum dolor sit amet,consectetuer adipiscing elit: https://afd.calpoly.edu/web/sample-tables. Sed lacus arcu, porta posuere, varius et. | Loremipsum dolor: https://afd.calpoly.edu/web/sample-tablessit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et. | Loremipsum dolor: https://afd.calpoly.edu/web/sample-tablessit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et. |
| Lorem ipsum dolor: https://afd.calpoly.edu/web/sample-tables | Lorem ipsum dolor: https://afd.calpoly.edu/web/sample-tables | Lorem ipsum dolor: https://afd.calpoly.edu/web/sample-tables |

Directory Listing Table - Roll Cursor Over an Item


Directory Listing   (Table caption - name and description of table)
          Apply the "directory" style to the <table> tag to remove the borders and add roll-over styling to rows.
          You can describe  your table here or in the context of your page.  This table is read using the  first row as the header for each column. (Replace this caption with your  own description of the table)
        
| Name | Telephone | Email | Office |
|---|---|---|---|
| Dr. Sally | 555-1234 | sally@calpoly.edu | 12-34 |
| Dr. Steve | 555-5678 | steve@calpoly.edu | 56-78 |
| Dr. Kathy | 555-9012 | kathy@calpoly.edu | 90-123 |

Column and Row Headings Example


Table caption (name and description of table)
        This table is read using the first row as a column header and then the first item of the first column as a row header.
        (Replace this caption with your own description of the table)
        
| Instructor | Class | Location |
| --- | --- | --- |
| Dr. Sally | Surgery 101 | Building 2 Room 3 |
| Dr. Steve | Radiology 101: https://afd.calpoly.edu/web/sample-tables | Building 2 Room 5: https://afd.calpoly.edu/web/sample-tables |
| Dr. Kathy | Orthopedics 101 | Building 2 Room 20 |

Table Data Alignment Styles - Left, Middle, Right


Table caption (name and description of table)
          This table uses classes center and right to align text or images within a table cell. Default alignment is left. You can describe your table here or in the context of your page.  
          This table is read using the first row as the header for each column.
          (Replace this caption with your own description of the table)
        
| Aligned Left | Aligned Center | Aligned Right |
|---|---|---|
| Academic Senate Meeting | May 25, 2205 | Building 99 Room 1 |
| Commencement Meeting | December 15, 2205 | Building 42 Room 10 |
| Lorem ipsum dolor sit amet,consectetuer adipiscing elit: https://afd.calpoly.edu/web/sample-tables. Sed lacus arcu, porta posuere, varius et. | Loremipsum dolor: https://afd.calpoly.edu/web/sample-tablessit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et. | Loremipsum dolor: https://afd.calpoly.edu/web/sample-tablessit amet, consectetuer adipiscing elit. Sed lacus arcu, porta posuere, varius et. |
| Lorem ipsum dolor: https://afd.calpoly.edu/web/sample-tables | Lorem ipsum dolor: https://afd.calpoly.edu/web/sample-tables | Lorem ipsum dolor: https://afd.calpoly.edu/web/sample-tables |

Table No Outline - H2


No Style Table Listing    (Table caption - name and description of table)
Apply the "table_noStyle" style to the <table> tag to remove the borders
        . You can describe  your table here or in the context of your page.  This table is read using the  first row as the header for each column. (Replace this caption with your  own description of the table)
        
| Day | Time | Location |
|---|---|---|
| Wednesday | 3-6 pm | Cal Poly Campus (follow U-Pick Signs: https://afd.calpoly.edu/web/sample-tables) |
| Thursday | 2:30-5pm | Morro Bay Farmer's Market |
| Thursday | 6:10-9pm | Downtown SLO Farmer's Market |
| Saturday | 8-10:30am | Farmer's Market new Embassy Suites |
| Saturday | 11am-2pm | Cal Poly Campus (follow U-Pick signs: https://afd.calpoly.edu/web/sample-tables) |

Complex Data Table


Table caption (name and description of table)
        This is an example of a Complex Data table that associates column headers with row headers that span multiple rows. The underlying HTML code of this table belies the necessary associations that make the table readable using a screen reading technology (Replace this caption with your own description of the table)
        
| NAME OF SYSTEM OR PORTAL CHANNEL | NAME OF SYSTEM OR ACTIVITY | STATUS DURING OUTAGE | DATA FROZEN AS OF | EXPECTED UP TIME |
| --- | --- | --- | --- | --- |
| Personal Information | Addresses | View Only | 1/18/2008 | Go live date |
| Personal Information | Names | View Only | 1/18/2008 | Go live date |
| Personal Information | Phone Numbers | View Only | 1/18/2008 | Go live date |
| Personal Information | Emergency Contacts | View Only | 1/18/2008 | Go live date |
| Group Leave Balance | Group Leave Balances | View Only | 12/31/2007 | 3/1/2008 |
| Leave/CTO Balances | Leave and CTO Balances | View Only | 12/31/2007 | 3/1/2008 |
| Faculty Course Info: https://afd.calpoly.edu/web/sample-tables | Class Search/Browse Catalog |  |  |  |
| Faculty Course Info: https://afd.calpoly.edu/web/sample-tables | Record Grades |  |  |  |
| Faculty Course Info: https://afd.calpoly.edu/web/sample-tables | Access Class Roster |  |  |  |
| Faculty Course Info: https://afd.calpoly.edu/web/sample-tables | Student Data |  |  |  |
| Faculty Course Info: https://afd.calpoly.edu/web/sample-tables | View My Class Schedule |  |  |  |
| Faculty Course Info: https://afd.calpoly.edu/web/sample-tables | View My Weekly Schedule |  |  |  |
| Enrollment Planning | View CourseCatalog: https://afd.calpoly.edu/web/sample-tablesand Schedule of Classes |  |  |  |
| Student Pay | Timekeeper Access: https://afd.calpoly.edu/web/sample-tables | Unavailable | 1/18/2008 |  |
| PolyData | ???? |  |  |  |
| PolyData |  |  |  |  |
| PolyProfile |  |  |  |  |
| PolyProfile |  |  |  |  |
| PolyProfile |  |  |  |  |

              https://afd.calpoly.edu/framework/images/calpoly-logo-vertical-rev-400.png

              AFD Web

              1 Grand Ave, Building 58: http://maps.calpoly.edu/?vlist=058-0 : Room 107, San Luis Obispo, CA 93407

                    * Phone: 805-756-6475
                    * afd-web@calpoly.edu: mailto:afd-web@calpoly.edu

                  Office Hours

                    * Monday — Friday
                    * 7:30 a.m. - 5:00 p.m.
          https://afd.calpoly.edu/framework/images/logo-inside-calpoly.png Visit Instagram : https://www.instagram.com/insidecalpoly/ Visit Facebook : https://www.facebook.com/insidecalpoly/

      Popular Links

        * Information Security: https://security.calpoly.edu
        * Information Classification and Handling Standard: https://security.calpoly.edu/content/policies/standards/classification/index
        * Password Changes: https://wiki.calpoly.edu/x/DouFDw
        * ITS Service Desk: https://tech.calpoly.edu/services
      https://afd.calpoly.edu/framework/images/calpoly-logo-rev-1x.png : http://www.calpoly.edu/

      © 2025 California Polytechnic State University — San Luis Obispo, California 93407 — Phone: 805-756-1111

        * Privacy Notice: https://www.calpoly.edu/privacy/
        * Web Accessibility Statement: https://accessibility.calpoly.edu/website-accessibility-statement
        * Non-Discrimination: https://crco.calpoly.edu/Notice_of_Non-Discrimination
```

[Visit our website](https://parseextract.com)

[Back to Table of Contents](#sample-output)

---

## PDF / Docx Parsing

### When `inline_images = True`

```In the below sample pdf page you can see 3 images of a product with their technical specifications spread across columns and the corresponding output showing how those 3 images were replaced by some image reference id.```

```Now some application like RAG that uses some chunking strategy to create collections of snippets can now have the image reference embedded with the plain text. So while retrieval, the code can parse for such image id ([Image_xx_xx]) and then fetch the image from some storage/db. The image now can be just shown to the user (as product image) or can be added to any LLM that accepts image input, this will enrich the context(if the image has important data) and create better dynamic responses based on the user query as the LLM will have the image along with the textual data.```

```Input PDF Page:```

![pdf_parsing_inline_images_1](/examples_images/pdf_parsing_image_inline_1.png)

```Output:```

```markdown
# DIESEL ENGINE &
# DIESEL ENGINE PUMPSET

[Image_1_1]

Water Cooled Engine

[Image_1_2]

Lister Engine

[Image_1_3]

Diesel Engine Pumpset

## DIESEL ENGINE

Crompton Greaves Water/Air Cooled
Diesel Engines are used for
Agriculture, Power Generation
(D.G. Sets), Industrial, Construction
and other applications.

### Technical Specifications

*   Type: Vertical, Single / Twin
    Cylinder, Air / Water cooled, Totally
    Enclosed, Compression
    Ignition, 4 Stroke Cycle, Cold
    Starting Diesel Engine.
*   Fuel System: Fuel is supplied to
    the fuel pump by gravity feed
    through the fuel tank and efficient
    paper element filter.
*   Lubrication: All moving parts in
    engine are lubricated partly by
    force feed and partly by splash
    lubrication. Parts like Valves, Push
    Rods etc. could be lubricated with
    oil can for slow speed Engines.
*   Cooling: Engine can be cooled
    with the help of run through water
    supply arrangement or with radiator
    / tank cooling in water cooled
    engine. In case of air cooled
    engine, cold air is forced on the
    cylinder and cylinder head by radial
    fan mounted on flywheel and
    directed through a cowling.
*   Governing: Mechanical,
    Centrifugal, for pumping application
    class B1, for D.G. Set application
    class A2.

*   Rotation: Standard direction of
    rotation is clockwise while facing
    the flywheel end, reverse rotation
    engines can be supplied if
    specifically ordered.
*   Starting: Hand start (manually),
    electric start can also be offered on
    request.
*   Drive: Standard power take off is
    from flywheel end. Power take off
    from gear end at half engine speed
    can be provided against specific
    requirement.
*   Standard Equipment: Starting
    handle, exhaust silencer, air
    cleaner, set of tools. Plus drive
    pulley, oiler for slow speed
    engines. (marked * in technical
    data table)

### Optional Equipment

*   Pump Application: Base plate,
    moving frame with wheels, run
    through cooling arrangement,
    coupling arrangement.
*   Genset Application: Coupling
    arrangement, moving frame, base
    plate, radiator cooling
    arrangement.

## DIESEL ENGINE
## PUMPSET

### Special Features

*   Excellent efficiency High discharge
    rate consuming less diesel.
*   Extremely simple construction -
    Easy for maintenance, easy gland
    packing replacement, suitable for
    direct drive with engine.
*   Shaft is of high carbon steel,
    ground accurately and ample size -
    can transmit maximum power
    without vibrations.
*   Bearing Housing - Sturdy and
    robust construction to give long
    continuous service - fitted with
    bronze bearing bush and ball
    bearing, both ample size to
    withstand all operating conditions.
*   Low NPSH requirement - Highest
    suction lift. Can suck water from
    depths as low as 9 meters.
*   C.I. Components of higher grade -
    Much higher mechanical strength.
*   Central Delivery - No air release
    cock required - No need to go
    down in the well to release air.
*   Back pull out design - No need to
    disturb piping while maintenance
    and servicing.
```

---

```Another example with images and tables.```

```Input PDF Page:```

![pdf_parsing_inline_images_2](/examples_images/pdf_parsing_image_inline_2.png)

```Output:```

```markdown
# AIR TANK COMPRESSOR 

[Image_1_1]

## Features

- Very high operating efficiency with close tolerance production.
- Enhanced cooling efficiency due to closely finned cylinder head, supported by fan and inter-cooler.
- Connecting rod and crank shaft made out of forged alloy steel.
- Splash lubrication and equipped with oil level indicator.
- Efficient Air Filter design and Silencer incorporated.
- Valves are finger plate type for easy flow and are self scavenging.
- Non-return valves are robust in construction that can be easily dismantled and assembled.
- Air receivers are hydraulically tested, manholes are provided for easy access for cleaning and maintenance in big size receivers.
- Tested to IS-5456.


## Applications

- Garages
- Textile units
- Spray painting
- Blasting
- Pneumatically operated fixtures
- Chuck cleaning
- Testing valve systems


## TECHNICAL SPECIFICATIONS

| Rating | Motor kW (HP) | No.of 
 Cylinder | Tank Capacity (Ltrs) | RPM | FAD |  |  | Displacement |  |  | Max. Pressure |  |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
|  |  |  |  |  | CFM | LPM | M³/Hr. | CFM | LPM |  M³/Hr. | kg/cm² | PSI |
| 140TC0.5 
 140TCM0.5 | 0.37 (0.5) | 1 | 40 | 650 | 2.0 | 55 | 3.4 | 2.7 | 77 | 4.6 | 4 | 57 |
| 170TC1 
 170TCM1 | 0.75 (1.0) | 1 | 70 | 910 | 2.45 | 70 | 4.2 | 3.5 | 100 | 5.9 | 6 | 86 |
| 190TC1 
 190TCM1 | 0.75 (1.0) | 1 | 90 | 910 | 2.45 | 70 | 4.2 | 3.5 | 100 | 5.9 | 6 | 86 |
| 1110TC1 
 1110TCM1 | 0.75 (1.0) | 1 | 110 | 1150 | 3.5 | 100 | 5.9 | 5.0 | 142 | 8.5 | 9 | 129 |
| 1110TC1.5 
 1110TCM1.5 | 1.1 (1.5) | 1 | 110 | 850 | 4.1 | 116 | 7.0 | 5.6 | 160 | 9.5 | 9 | 129 |
| 1130TC1.5 
 1130TCM1.5 | 1.1 (1.5) | 1 | 130 | 850 | 4.1 | 116 | 7.0 | 5.6 | 160 | 9.5 | 9 | 129 |
| 1160TC2 
 1160TCM2 | 1.5 (2.0) | 1 | 160 | 1070 | 4.9 | 140 | 8.3 | 7.0 | 200 | 12.0 | 9 | 129 |
| 2110TC1.5 
 2110TCM1.5 | 1.1 (1.5) | 2 | 110 | 650 | 4.2 | 119 | 7.1 | 6.0 | 170 | 10.2 | 9 | 129 |
| 2130TC1.5 
 2130TCM1.5 | 1.1 (1.5) | 2 | 130 | 650 | 6.5 | 185 | 10.9 | 8.6 | 245 | 14.6 | 9 | 129 |
| 2130TC2 
 2130TCM2 | 1.5 (2.0) | 2 | 130 | 650 | 5.8 | 165 | 9.9 | 8.3 | 235 | 14.1 | 9 | 129 |
```

### When `inline_images = False`

```You will get similar output as above but without the inline image id. For both options you will get a seperate list of extracted images with bounding box data and base64 encoded string of the image.```

[Visit our website](https://parseextract.com)

[Back to Table of Contents](#sample-output)

---

## Image / Scanned Document Parsing

```input Image:```

![image_parsing_1](/examples_images/image_parsing_1.png)

```Output:```

```markdown
EXECUTIVE SUMMARY

|                                                              | Three Months Ended September 30, |        |Nine Months Ended September 30, |       |
| :----------------------------------------------------------- | :-----------------------------: | :-----------------------------: | :---: | :---: |
| (in millions, except per share data)                         |              2023               |              2022               | 2023  | 2022  |
| GAAP basis (1):                                             |                                 |                                 |       |       |
| Total revenue                                                |             $ 4,522             |             $ 4,311             | 13,228 | 13,536 |
| Total expense                                                |              2,885              |              2,785              | 8,538  | 8,578  |
| Operating income                                             |             $ 1,637             |             $ 1,526             | 4,690  | 4,958  |
| Operating margin                                             |            36.2%              |            35.4%              | 35.5%  | 36.6%  |
| Nonoperating income (expense), less net income               |                                 |                                 |       |       |
| (loss) attributable to noncontrolling interests              |               180               |               210               |  478  |  (88) |
| Income tax expense                                           |               213               |               330               | 1,041  |  951  |
| Net income attributable to BlackRock                         |             $ 1,604             |             $ 1,406             | 4,127  | 3,919  |
| Diluted earnings per common share                            |             $ 10.66             |             $ 9.25              | 27.36  | 25.67  |
| Effective tax rate                                           |            11.7%              |            19.0%              | 20.1%  | 19.5%  |
| As adjusted(2):                                              |                                 |                                 |       |       |
| Operating income                                             |             $ 1,691             |             $ 1,585             | 4,877  | 5,134  |
| Operating margin                                             |            42.3%              |            42.0%              | 41.8%  | 43.3%  |
| Nonoperating income (expense), less net income               |                                 |                                 |       |       |
| (loss) attributable to noncontrolling interests              |             $ 184             |             $ 210             |  449  |  (88) |
| Net income attributable to BlackRock                         |             $ 1,642             |             $ 1,451             | 4,241  | 4,035  |
| Diluted earnings per common share                            |             $ 10.91             |             $ 9.55              | 28.11  | 26.43  |
| Effective tax rate                                           |            12.4%              |            19.2%              | 20.4%  | 20.0%  |
| Other:                                                       |                                 |                                 |       |       |
| Assets under management (end of period)                      |         $ 9,100,825         |         $ 7,961,373         | 9,100,825 | 7,961,373 |
| Diluted weighted-average common shares outstanding           |              150.5              |              152.0              | 150.9  | 152.6  |
| Shares outstanding (end of period)                           |              148.9              |              150.5              | 148.9  | 150.5  |
| Book value per share (3)                                     |             $ 259.34            |             $ 246.99            | 259.34 | 246.99 |
| Cash dividends declared and paid per share                   |             $ 5.00              |             $ 4.88              | 15.00  | 14.64  |

(1) Accounting principles generally accepted in the United States ("GAAP").

(2) As adjusted items are described in more detail in Non-GAAP Financial Measures. Beginning in the first quarter of 2023, BlackRock updated the definitions of its non-GAAP financial measures to exclude the impact of market valuation changes on certain deferred cash compensation plans which the Company began economically hedging in 2023.

(3) Total BlackRock stockholders' equity divided by total shares outstanding at September 30 of the respective period-end.

Three Months Ended September 30, 2023 Compared with Three Months Ended September 30, 2022

GAAP. Operating income of $1.6 billion increased $111 million and operating margin of 36.2% increased 80 bps from the three months ended September 30, 2022. Increases in operating income and operating margin reflected higher investment advisory and administration fees (collectively "base fees"), primarily driven by organic base fee growth and the impact of market movements over the past twelve months on average AUM, and higher technology services revenue.

Nonoperating income (expense) less net income (loss) attributable to noncontrolling interests ("NCI") decreased $30 million from the three months ended September 30, 2022, reflecting the impact of $267 million of noncash gains related to BlackRock's strategic minority investment in iCapital Network, Inc. ("iCapital") during 2022, partially offset by higher mark-to-market revaluation of the Company's seed capital portfolio, net of impact of certain hedges, higher gains on private equity co-investment portfolios, and higher interest and dividend income during the three months ended September 30, 2023.
```

[Visit our website](https://parseextract.com)

[Back to Table of Contents](#sample-output)
  
---

## 💲Output Token Based Pricing Examples

```Example 1:```

The below Page has multiple images and sufficient amount of text on a single page. The output token for below comes out to be 650 which will be charged as $0.0008125

![output_token_1](/examples_images/output_token_1.png)

```
[Image_3_1]

AN OVERVIEW - PUMPS:

Crompton Greaves Ltd., started manufacturing pumps in 1964 at worli. It was shifted to Ahmednagar later in 2000-2001. Today CG Pumps manufacture all types of pumps suitable for handling clear cold water, for Domestic Agricultural, and Industrial Segment. In the last 20 years, the CG Pumps has undergone a dramatic transformation in the areas of product range and capacities.

The driving strengths of the CG Pumps are thrust on Quality, new product development and customer focus, which has led the CG Pumps to enjoy the status of market leadership in India.

Today CG Pumps is offering widest product range under one roof, which differentiates it from it's competitors.

QUALITY STANDARDS

'Crompton' pumps are manufactured in accordance with and conforming to relevant B.I.S. standards. The products are designed to suit continuously changing environment, for easy installation, low running cost, improved efficiency and minimal maintenance. Factory has modern state of art Inspection and Testing set-up. Strict quality assurance plan and rigorous testing of pumps ensures high efficiency and enhanced life of products. Modern dynamic balancing m/c, digital test panels, digital flow meters, digital pressure measuring devises, 60-cycle power generating set, automatic box strapping m/c, ensure precision and consistency in Quality. Continuos training to all employees is the thrust to improve their skill, performance and efficiency. CG Pumps is practicing Six Sigma Quality Drive to improve the Quality of the products as per International Standards.

Today CG Pumps has an Approval from various Govt. Dept. like,

*   Govt. of Tripura • Rajasthan P.H.E.D. • Delhi MES, Jal Board • OLIC - Bhubaneshwar, Govt. of Orissa • Northen Railway
*   Maharashtra Jeevan Pradhikaran • DGS & D.

We are regular suppliers to various Govt. bodies.

The pumpset supplied to these Govt. bodies have been approved by third party like DGS & D, S.G.S. Lloyd's etc.

Crompton Greaves Limited, is committed towards the society by giving pollution free, non-hazardous, energy efficient products.

[Image_3_6]

Quality Assurance

[Image_3_2]

Inspection

[Image_3_3]

Computerized routine test

[Image_3_4]

Type testing

[Image_3_5]

Training Centre
```

```Example 2:```

The below page has math equations with good amount of text. The output token for this comes out to be 1175 which is charged as $0.001468.

![output_token_2](/examples_images/output_token_2.png)

```
# TECHNICAL DATA

## TERMINOLOGY AND HEAD CALCULATIONS

1.  **CAPACITY (Discharge):** Rate of flow of liquid measured in litres per minute or gallons per minute.
2.  **TOTAL HEAD:** The standard unit for expressing head shall be the metres, thus the head in metres of liquid column = pressure in kg/cm² x 10.
3.  **FRICTIONAL LOSSES:** Resistance by inner surface of pipe and fittings through which liquid is being pumped.
4.  **CAVITATION:** The formation of cavities in a fluid, is a phenomenon involving the appearance and subsequent sudden collapse of vapour bubbles in a flow of fluid.
5.  **SUCTION LIFT (HS):** Is the vertical distance between pump center line and water level.
6.  **DELIVERY HEAD(HD):** Vertical Distance above the pump centreline to the top most point of the delivery.
7.  **N.P.S.H.:** Net Positive Suction Head. It is the pressure in terms of absolute head in meters or feet at a pump suction branch minus vapour pressure of the liquid at its working temperature. It can be simply taken as entry loss at the impeller eye in the case of centrifugal pump.
8.  **VAPOUR PRESSURE:** Can be defined as that pressure which is just necessary to keep a liquid from boiling at a particular given temperature.
9.  **DUTY POINT:** The pump is designed for one point where the maximum pump Eff. / overall Eff is achieved. This point is called Duty Point or operating Point.
10. **PUMP EFF.:** The ratio of the pump output to the pump input
    Thus Pump eff. =  
    $\\frac{(T. Head \\times Discharge) \\text{ in } kW}{Motor Out put \\text{ in } kW} \\times 100$

11. **OVERALL EFF.:** The ratio of the pump output to the motor input
    Thus Overall Eff. =  
    $\\frac{Pump Efficiency \\times Motor Efficiency}{Pump Input} \\times \\frac{Motor Output}{Motor Input} = \\frac{Pump Output}{Motor Input}$

12. **SPECIFIC GRAVITY:** Ratio of wt of given volume of fluid compared to same wt of equal volume of water at std temp & pressure. Specific Gravity of Water is 1.0.If fluid has Specific gravity other than water (1.0) multiply brake horsepower for water by specific gravity of fluid to obtain horsepower required.
13. **VISCOSITY:** Property of Internal Friction of a fluid or resistance to motion of its particles. Measuring a fluid's resistance to flow will give coefficient of viscosity. High viscosity fluids are resistant to flow and appear thick and sluggish. Viscosity is independent of specific gravity and increases with increase in temperature. Viscous fluids tend to reduce the capacity, head and efficiency while increasing the brake horsepower required. Centrifugal Pumps may be used for viscosities upto 1000 1500 SSU. Above this limit Rotary Pumps are used.

## CALCULATION OF TOTAL HEAD

Total Head H of the Pumpset is given by:
(Ref. Sketch)

$H = HS^* + Hd + hfs^* + hfd + HLf + \\frac{Vd^2}{2g}$

\* In case of submersible pumpset HS & hfs = 0

Where

HS = Static suction lift, the difference in level between the center line of pump and the water level in the sump in feet or metres.

Hd = Static Delivery head, the difference in level between the centre line of the pump and the highest point in the delivery line in feet or metres.

hfs = Friction losses in suction pipe line in feet or metres.

hfd = Friction losses in delivery pipe line in feet or metres.

HLf = Total friction losses due to pipe fittings in suction and delivery pipeline in feet or meters, e.g. strainer with foot valve, bends, valves, etc.

$\\frac{Vd^2}{2g}$ = Velocity head of water in the delivery pipe in feet or meters.

Where Vd = Velocity of water in delivery pipe = Discharge / Area of pipe in ft/sec or m/sec.

g = Acceleration due to gravity = 9.81 m/sec² = 32.2 ft/sec²

To calculate the above parameters, the following details are required.
a. Required discharge in LPM or GPM.
b. Size and length of the suction & delivery pipes.
c. Size, type and number of pipe fittings on suction and delivery sides.
d. Variation in water level on suction side.

In working out the above, care has to be taken to see that constant units are used.
```

```Example 3:```

The below page is full of tables which results in lots of texts in an small area. The output token comes out to be 1728 which is charged as $0.00216.

![output_token_3](/examples_images/output_token_3.png)

```
# CONVERSION TABLE

| Discharge : |  |  |
|---|---|---|
| 1 Imp Gallon | - | 4.546 ltrs. |
| 1 US Gallon | - | 3.785 ltrs. |
| 1 Cu m. | - | 1000 ltrs. |
| 1 Cu ft. | - | 28.32 ltrs. |

## Discharge rate :

| 1 m³/h | - | 16.67 l/min. |
| 1 m³/s | - | 60,000 l/min. |
| 1 l/s | - | 60 l/min |
| 1 Cu ft/s | - | 1699.2 l/min. |
| 1 Imp. GPH | - | 0.0757 l/min |
|  |  | 0.00126 l/Sec. |

## Head :

| 1 mtrs. | - | 3.28 ft. |
| 1 ft | - | 0.3048 m. |
| 1 kg/cm² | - | 10 mtrs |

## Pressure :

| 1 Atmosphere | - | 1.033 kg/cm² |
| 1 Atmosphere | - | 14.7 lb/in² |
| 1 Atmosphere | - | 10.34 mwc |
| 1 lb/in² | - | 0.704 mwc |
| 1 lb/in² | - | 2.31 ft wc |
| 1 lb/in² | - | 51.6 mm of mercury. |
| 1 cusec | - | 1705 lpm |
|  | - | 1 Acre inch/hr |
| 1 Cu mec | - | 20558.3 lpm. |
|  | - | 1 Acre ft/hr. |

## Power :

| 1 HP (Si) | - | 0.746 kW |
|  | - | 746 W |
| 1 HP (Metric) | - | 0.736 kW |
|  | - | 736W |
| 1 kW | - | 1000 W |

## Weight :

| 1 kg. | - | 1000 gm. |
| 1 kg. | - | 2.2046 lb. |
| 1 lb. | - | 0.4536 kg. |

# DISCHARGE RATE TABLE

| Veenotch reading in inch | Veenotch reading in mm. | Discharge rate in GPH (imp) | Discharge rate in lpm. |
|---|---|---|---|
| 1/2" | 12.7 | 21 | 1.59 |
| 3/4" | 19.05 | 57.42 | 4.35 |
| 1" | 25.4 | 117.22 | 8.88 |
| 1 1/4" | 31.75 | 203.8 | 15.44 |
| 1 1/2" | 38.1 | 320.5 | 24.28 |
| 1 3/4" | 44.45 | 469.52 | 35.57 |
| 2" | 50.8 | 653.8 | 49.53 |
| 2 1/4" | 57.15 | 875.56 | 66.33 |
| 2 1/2" | 63.5 | 1137.05 | 86.14 |
| 2 3/4" | 69.85 | 1440.12 | 109.1 |
| 3" | 76.2 | 1786.49 | 135.39 |
| 3 1/4" | 82.55 | 2179.45 | 165.11 |
| 3 3/4" | 95.25 | 3108.07 | 235.46 |
| 4" | 101.6 | 3647.56 | 276.33 |
| 4 1/4" | 107.95 | 4239.31 | 321.16 |
| 4 1/2" | 114.3 | 4884.92 | 370.07 |
| 4 3/4" | 120.65 | 5585.84 | 423.17 |
| 5" | 127 | 6343.95 | 480.6 |
| 5 1/4" | 133.35 | 7159.55 | 542.39 |
| 5 1/2" | 139.7 | 8034.97 | 608.71 |
| 5 3/4" | 146.05 | 8991.64 | 679.67 |
| 6" | 152.4 | 9970.22 | 755.32 |
| 6 1/4" | 158.75 | 11032.43 | 835.79 |
| 6 1/2" | 165.1 | 12159.44 | 921.17 |
| 6 3/4" | 171.45 | 13352.46 | 1011.55 |
| 7" | 177.08 | 14466.41 | 1095.94 |
| 7 1/4" | 184.15 | 15941.38 | 1207.68 |
| 7 1/2" | 190.5 | 17339.65 | 1313.61 |
| 7 3/4" | 196.85 | 18808.55 | 1424.89 |
| 8" | 203.2 | 20349.38 | 1541.62 |

```

[Visit our website](https://parseextract.com)

[Back to Table of Contents](#sample-output)

---

## Table Extraction

The API will only extract any ```Tables``` or ```Tabular Data``` and convert to excel sheet or csv. Adding one ```Bank Statement``` Example:

```Input:```

![table_extract_1](/examples_images/table_extract_1.png)

```Output (you will get below tables as excel sheets or csv, here just adding plain text):```

```markdown
| Description                        | Amount         |
| Beginning Balance on May 3, 2003   | $7,126.11      |
| Deposits & Other Credits           | +3,615.08     |
| ATM Withdrawals & Debits           | -20.00        |
| VISA Check Card Purchases & Debits | -0.00         |
| Withdrawals & Other Debits         | -0.00         |
| Checks Paid                        | -200.00       |
| **Ending Balance on June 5, 2003** | **$10,521.19** |

---------------------------------------------

| Description                        | Ref Nbr   | Date Credited | Amount        |
| Deposit                            | 130012345 | 05-15         | $3,615.08     |
| **Total Deposits & Other Credits** |           |               | **$3,615.08** |

---------------------------------------------

| Description                                                | Tran Date | Date Paid | Amount     |
| ATM Withdrawal 1000 Walnut St Kansas City MO M119 00005678 | 05-18     | 05-19     | $20.00     |
| **Total ATM Withdrawals & Debits**                         |           |           | **$20.00** |

---------------------------------------------

| Date Paid             | Check Number | Amount | Reference Number |
| 05-12                 | 1001         | 75.00  | 00012576589      |
| 05-18                 | 1002         | 30.00  | 00036547854      |
| 05-24                 | 1003         | 200.00 | 00094613547      |
| **Total Checks Paid** |              |        | **$305.00**      |

---------------------------------------------
```

```Another Example:```

![table_extract_2](/examples_images/table_extract_2.png)

```Output (you will get below tables as excel sheets or csv, here just adding plain text):```

```
| CODIGO  | DESCRIPCION               | UN  | UN PRECIO | DTOS. | TOTAL |
| 1168554 | COCACOLA ZERO UR237 C24   | 2   | 24,72     | -9,89 | 39,55 |
|         | Promoción Múltiple: 55878 |     |           |       |       |
| 1020429 | LLET NOSTRA ENT 1,5L 6BOT | 1   | 10,24     | -8,94 | 9,30  |

---------------------------------------------

| ENVASE  | DESCRIPCION          | ENTREGA | RECOGIDA | IMPORTE |
| 1160960 | BOTELLA UR237 COBEGA | 2 CJ    | -2 CJ    | 0,00    |
| 1160001 | PLASTICO UR20 COBEGA | 2 UN    | -2 UN    | 0,00    |

---------------------------------------------

| CONCEPTO           | IMPORTE   | BASE IVA | %IVA | CUOTA IVA |
| PROD+ENVASES       | 59,68     | 9,30     | 2.0  | 0.19      |
| DESCUENTOS         | -10,83    | 58,43    | 21.0 | 12,27     |
| PTO.VERDE          |           |          |      |           |
| SERV.LOG           | 18,88     |          |      |           |
| **TOTAL ENTREGA:** | 88,19 EUR |          |      |           |

---------------------------------------------
```

[Visit our website](https://parseextract.com)

[Back to Table of Contents](#sample-output)
  
---

## Structured Data Extraction

```Consider the URL: ```[https://www.ikea.com/in/en/cat/sofas-fu003/](https://www.ikea.com/in/en/cat/sofas-fu003/)

```We will ask to extract with this prompt:```

*extract the product name, product link, image link and price for all the products*

```Output Extractions:```

```markdown
{
    "product_name": "EKTORP 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/ektorp-3-seat-sofa-hakebo-dark-grey-s19508999/",
    "image_link": "https://www.ikea.com/ext/ingkadam/m/18cac20c564a2bb3/original/PE902096-crop001.JPG?f=s",
    "price": "Rs.33,990"
  },
  {
    "product_name": "LANDSKRONA 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/landskrona-3-seat-sofa-gunnared-light-green-wood-s19270327/",
    "image_link": "https://www.ikea.com/ext/ingkadam/m/720cb948eae89d88/original/PE923432-crop001.jpg?f=s",
    "price": "Rs.69,990"
  },
  {
    "product_name": "GAMMALBYN 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/gammalbyn-3-seat-sofa-kilanda-light-beige-10615526/",
    "image_link": "https://www.ikea.com/in/en/images/products/gammalbyn-3-seat-sofa-kilanda-light-beige__1449308_pe989846_s5.jpg?f=xxs",
    "price": "Rs.22,990"
  },
  {
    "product_name": "EKTORP 3-seat sofa with chaise longue",
    "product_link": "https://www.ikea.com/in/en/p/ektorp-3-seat-sofa-with-chaise-longue-kilanda-light-beige-s19509041/",
    "image_link": "https://www.ikea.com/in/en/images/products/ektorp-3-seat-sofa-with-chaise-longue-kilanda-light-beige__1194849_pe902099_s5.jpg?f=xxs",
    "price": "Rs.37,990"
  },
  {
    "product_name": "ORMARYD 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/ormaryd-3-seat-sofa-dark-blue-60477594/",
    "image_link": "https://www.ikea.com/in/en/images/products/ormaryd-3-seat-sofa-dark-blue__0919663_pe786703_s5.jpg?f=xxs",
    "price": "Rs.20,990"
  },
  {
    "product_name": "GLOSTAD 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/glostad-3-seat-sofa-knisa-dark-grey-40595937/",
    "image_link": "https://www.ikea.com/in/en/images/products/glostad-3-seat-sofa-knisa-dark-grey__1234948_pe917261_s5.jpg?f=xxs",
    "price": "Rs.12,990"
  },
  {
    "product_name": "GLOSTAD 2-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/glostad-2-seat-sofa-knisa-dark-grey-10489009/",
    "image_link": "https://www.ikea.com/in/en/images/products/glostad-2-seat-sofa-knisa-dark-grey__0950864_pe800736_s5.jpg?f=xxs",
    "price": "Rs.9,990"
  },
  {
    "product_name": "LINANÄS 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/linanaes-3-seat-sofa-vissle-beige-90512237/",
    "image_link": "https://www.ikea.com/in/en/images/products/linanaes-3-seat-sofa-vissle-beige__1013894_pe829446_s5.jpg?f=xxs",
    "price": "Rs.24,990"
  },
  {
    "product_name": "JÄTTEBO U-shaped sofa",
    "product_link": "https://www.ikea.com/in/en/p/jaettebo-u-shaped-sofa-7-seat-with-chaise-longue-right-with-headrests-tonerud-grey-s39510618/",
    "image_link": "https://www.ikea.com/in/en/images/products/jaettebo-u-shaped-sofa-7-seat-with-chaise-longue-right-with-headrests-tonerud-grey__1179836_pe896109_s5.jpg?f=xxs",
    "price": "Rs.2,93,500"
  },
  {
    "product_name": "EKTORP 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/ektorp-3-seat-sofa-kilanda-light-beige-s49509011/",
    "image_link": "https://www.ikea.com/in/en/images/products/ektorp-3-seat-sofa-kilanda-light-beige__1194853_pe902103_s5.jpg?f=xxs",
    "price": "Rs.29,990"
  },
  {
    "product_name": "LANDSKRONA 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/landskrona-3-seat-sofa-gunnared-light-green-wood-s19270327/",
    "image_link": "https://www.ikea.com/in/en/images/products/landskrona-3-seat-sofa-gunnared-light-green-wood__0602122_pe680191_s5.jpg?f=xxs",
    "price": "Rs.69,990"
  },
  {
    "product_name": "SÖDERHAMN Corner sofa",
    "product_link": "https://www.ikea.com/in/en/p/soederhamn-corner-sofa-6-seat-tonerud-grey-s89452079/",
    "image_link": "https://www.ikea.com/in/en/images/products/soederhamn-corner-sofa-6-seat-tonerud-grey__1057827_pe849007_s5.jpg?f=xxs",
    "price": "Rs.1,19,080"
  },
  {
    "product_name": "LINANÄS 3-seat sofa with chaise longue",
    "product_link": "https://www.ikea.com/in/en/p/linanaes-3-seat-sofa-with-chaise-longue-vissle-dark-grey-60512248/",
    "image_link": "https://www.ikea.com/in/en/images/products/linanaes-3-seat-sofa-with-chaise-longue-vissle-dark-grey__1013908_pe829460_s5.jpg?f=xxs",
    "price": "Rs.35,990"
  },
  {
    "product_name": "SÖDERHAMN 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/soederhamn-3-seat-sofa-gransel-natural-colour-s39442158/",
    "image_link": "https://www.ikea.com/images/a-soederhamn-sofa-in-a-living-room-with-different-cushions-l-9ea3ab1b5308e61f33cab2df355f59f9.jpg?f=s",
    "price": "Rs.52,990"
  },
  {
    "product_name": "SÖDERHAMN 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/soederhamn-3-seat-sofa-with-open-end-viarp-beige-brown-s79305692/",
    "image_link": "https://www.ikea.com/ext/ingkadam/m/1427af785fe647b8/original/PH181137-crop001.jpg?f=s",
    "price": "Rs.63,000"
  },
  {
    "product_name": "KIVIK 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/kivik-3-seat-sofa-kelinge-grey-turquoise-s19443050/",
    "image_link": "https://www.ikea.com/in/en/images/products/kivik-3-seat-sofa-kelinge-grey-turquoise__1055806_pe848110_s5.jpg?f=xxs",
    "price": "Rs.39,990"
  },
  {
    "product_name": "EKHOLMA 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/ekholma-3-seat-sofa-hakebo-dark-grey-s39537415/",
    "image_link": "https://www.ikea.com/in/en/images/products/ekholma-3-seat-sofa-hakebo-dark-grey__1360613_pe954532_s5.jpg?f=xxs",
    "price": "Rs.41,990"
  },
  {
    "product_name": "EKTORP 3-seat sofa with chaise longue",
    "product_link": "https://www.ikea.com/in/en/p/ektorp-3-seat-sofa-with-chaise-longue-hakebo-grey-green-s09509032/",
    "image_link": "https://www.ikea.com/in/en/images/products/ektorp-3-seat-sofa-with-chaise-longue-hakebo-grey-green__1194845_pe902095_s5.jpg?f=xxs",
    "price": "Rs.41,990"
  },
  {
    "product_name": "HYLTARP 3-seat sofa w chaise longue",
    "product_link": "https://www.ikea.com/in/en/p/hyltarp-3-seat-sofa-w-chaise-longue-left-gransel-grey-s59514960/",
    "image_link": "https://www.ikea.com/in/en/images/products/hyltarp-3-seat-sofa-w-chaise-longue-left-gransel-grey__1193852_pe901663_s5.jpg?f=xxs",
    "price": "Rs.79,990"
  },
  {
    "product_name": "HOLMSUND 3-seat sofa bed",
    "product_link": "https://www.ikea.com/in/en/p/holmsund-3-seat-sofa-bed-kilanda-dark-blue-s39516922/",
    "image_link": "https://www.ikea.com/in/en/images/products/holmsund-3-seat-sofa-bed-kilanda-dark-blue__1212731_pe910735_s5.jpg?f=xxs",
    "price": "Rs.59,990"
  },
  {
    "product_name": "SÖDERHAMN 3-seat sofa",
    "product_link": "https://www.ikea.com/in/en/p/soederhamn-3-seat-sofa-fridtuna-light-beige-s69449691/",
    "image_link": "https://www.ikea.com/in/en/images/products/soederhamn-3-seat-sofa-fridtuna-light-beige__1057770_pe848964_s5.jpg?f=xxs",
    "price": "Rs.51,990"
  }
```

It's better to also provide a schema in the prompt so that you know the keys of the json to extract and process further e.g. prompt:

```
extract the product name, product link, image link and price for all the products. The format should be:
[
  {
    "product_name": ,
    "product_link": ,
    "image_link": ,
    "price":
  },
  {
    "product_name": ,
    ...
  },
  ...
]
```

[Visit our website](https://parseextract.com)

[Back to Table of Contents](#sample-output)

------------------------------------------------
