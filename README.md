# Exploring Coffee Quality Data with Power BI
## 1.	Project Over View:
### 1.1	Title:   
         Report Based on Exploring Coffee Quality 
### 1.2	Description:
        The Coffee Quality Institute (CQI) is a non-profit organization that works to improve the quality and value of coffee worldwide. 
        It was founded in 1996 and has its headquarters in California, USA. CQI's mission is to promote coffee quality through a range 
        of activities that include research, training, and certification programs. The organization works with coffee growers, processors, 
        roasters, and other stakeholders to improve coffee quality standards, promote sustainability, and support the development 
        of the specialty coffee industry.
### 1.3 Objective:
       The primary goal of this project is to leverage the rich dataset provided by CQI to understand the factors contributing to coffee quality. 
## 2.	Data Source:
### 2.1	Data Source Overview: 
       The File used in this analysis is df_arabica_clean (2).csv. The data includes information on coffee production, processing, 
       and sensory evaluation. It also contains data on coffee genetics, soil types, and other factors affecting coffee quality.
### 2.2 Data Fields:
       The Data includes the following fields.
#### •	ID: 
        Unique Identifier of each coffee data.
#### •	Country Of Origin: 
        The Country where the coffee is produced/cultivated.
#### •	Lot Number: 
        Unique code assigned to identify a batch of products with similar attributes.
#### •	Altitude:  
       Altitude, like elevation, is the distance above sea level. "High- Altitude " if they reach at least 2,400 meters.
#### •	Region: 
       An area, especially part of a country.
#### •	Number of Bags: 
       Count of bags generated by each region.
#### •	Bag Weight: 
       The Weight of each bag.
#### •	In-country partner: 
       A local entity or service provider who assists businesses in navigating the complexities of coffee production.
#### •	Harvest Year: 
       The crop year in which the harvest begins.
#### •	Grading Date:
       When harvested crops are sorted or graded according to their size, quality, or other criteria.
#### •	Variety: 
       Type of coffee depending on the species, region, and processing methods.
#### •	Processing Method: 
       Refers to the specific procedures or techniques used in the production of coffee.
#### •	Aroma:
       Refers to the scent or fragrance of the coffee.
#### •	Flavor: 
       The flavor of coffee is evaluated based on the taste, including any sweetness, bitterness, acidity, and other flavor notes.
#### •	Aftertaste: 
       Refers to the lingering taste that remains in the mouth after swallowing the coffee.
#### •	Acidity: 
       Acidity in coffee refers to the brightness or liveliness of the taste.
#### •	Body: 
       The body of coffee refers to the thickness or viscosity of the coffee in the mouth.
#### •	Balance: 
       Balance refers to how well the different flavor components of the coffee work together.
#### •	Uniformity: 
       Uniformity refers to the consistency of the coffee from cup to cup.
#### •	Clean Cup: 
        A clean cup refers to a coffee that is free of any off-flavors or defects, such as sourness, mustiness, or staleness.
#### •	Sweetness: 
       It can be described as caramel-like, fruity, or floral, and is a desirable quality in coffee.
#### •	Overall: 
       Average quality of coffee.
#### •	Defects: 
      Value refers to defects in coffee.
#### •	Total Cup Points: 
      'Total Cup Points' is the total of 10 features i.e., Aroma, Flavor, Aftertaste, Acidity, Body, Balance, Uniformity, Clean Cup, Sweetness, Overall.
#### •	Moisture Percentage: 
       The percent of moisture present in coffee.
#### •	Category One Defects: 
        Category One defects are primary defects that can be perceived through visual inspection of the coffee beans. 
        These defects include Black beans, sour beans, insect-damaged beans, fungus-damaged beans, etc.
#### •	Category Two defects: 
        Category Two defects are secondary defects that are more subtle and can only be detected through tasting. 
        These defects include Over-fermentation, staleness, rancidness, chemical taste, etc.
#### •	Quakers: 
       Coffee refers to defective coffee beans that haven't ripened properly.
#### •	Color: 
       The color of coffee beans.
#### •	Expiration:  
        Refers to the point at which coffee loses its optimal flavor and freshness.
## 3.	Data Transformation:
### 3.1	Data Cleaning:
- Considering the feature engineer concept, analysis needs only a few attributes ID, Country Of Origin, Region, variety, 
  Processing Method, Aroma, Flavour, Aftertaste, Acidity, Body, Balance, Uniformity, Sweetness, Clean cup, Overall, 
  Total Cup Points, Category One Defects, Category Two Defects and remaining attributes are removed.
- One Row With ID=105 doesn't contain values for attributes region, variety, and  Processing Method Which is important 
  for analysis, it is removed as there is no way to fill Or replace it.
- Duplicates are removed from combining the selected columns Country Of Origin, Region, Variety, and Processing Method. 
  Almost 38 Rows are removed.
- Variety column contains blanks, unknown, unknow, unknownn values mentioned are replaced with a single value unknown.
- In column Region there is a full detail that is not required so, I split the column using a comma as a delimiter and removed another part of the column. 
   Region contains one blank value based on the hierarchy using the country column replaced with ESTELI and some values in other languages are replaced with 
   English and capitalized.
- In the Processing Method the blank values are replaced with Washed / Wet after analyzing the data hierarchy using country, region, and variety.
- Using text analysis techniques in Variety Column some values are replaced.
## 4. Report:
![](https://github.com/BhavanaBalasa/CoffeeQuality_Power-BI/blob/main/Power_BI_Report.png)
 

## 5. Explored the following research questions:
#### 1.	What are the key determinants of coffee quality as evaluated through sensory attributes such as aroma, flavor, acidity, etc.?
- The key determinants of coffee quality are Aroma, Flavor, Aftertaste, Acidity, Body, overall, uniformity, sweetness, clean cup, and Balance.
- These Factors impact the coffee efficiency.

#### 2. Is there a correlation between processing methods, origin regions, and coffee quality scores?
- Based on the processing method quality of the coffee produced will vary.
- Double Anaerobic Washed and Semi Washsed processes are the top methods to serve good coffee.
- Piendamo, Tarrazu, and Loas borofen plateau are top regions in producing good quality coffee.

#### 3. Can we identify any trends or patterns in defect occurrences and their impact on coffee quality?
- Natural/Dry, Washed / Wet, and Pulped natural / honey methods produce more defects.
- Category Two Defects are more the Category One Defects. 

#### 4. How do different variables influence the Total Cup Points, which represent an overall measure of coffee quality?
- The Overall Cup points of a Coffee is influenced by attributes Acidity, flavor, Aroma, Body, Balance, and After taste.
   The increase in these attributes enhances the Coffee Quality Points.
- Double Anaerobic washed, Semi washed had high Total Cup Points.
-  Piendamo and Chiayi are the regions with high points.
- Castillo, Gesha, and Java are top coffee varieties.


