# weighted_data
# Project idea: Data Pipeline for ETL (Extract, Transform, Load)

## Project Description:
Build a data pipeline that performs ETL (Extract, Transform, Load) on a dataset. This project will help gain practical experience in data engineering by working with data ingestion, transformation, and loading processes.

> Having a longterm hobby and intrest into sports, fitness and nutrition I've decided to try and use a few data samples on olymipic style weightlifting.
> This will come with some of its own challenges most im sure i havent considered yet, but things like limited data compaired to more popular sports, resource sites term's of use, ...

## Scope
> Question of scope - As a practice exercise, it may be challenging and rewarding enough to just extract the sample data, clean and convert it into a another useable variable type (currently undecided but should reflect common types used in statistical analysis) and then load it into a database or data lake.
> However I would love to revisit this project down the line as i feel it would be fun to build an anaylisis of these records against another event like development and abundance of anabolic steroids for example.


## Project Steps:
- Data Source Selection: Choose a relevant dataset. Publicly available datasets, such as those on government websites or data repositories maybe.

> I plan to use a varriety of different data sources to combat the narrow scope that may occur if the samples were for example just taken from actual recent olymipc weightlifting records;
> International Weightlifting Federation (IWF): The IWF may provide datasets related to Olympic weightlifting, including athlete profiles, competition results, and historical records.
> Kaggle: Kaggle is a popular platform for finding datasets on various topics, including sports.
>  --- probably more as i research further ---

- Data Extraction: Write scripts or use tools to extract data from the chosen data source. The data source could be a CSV file, JSON data, a database, or a RESTful API.

> International Weightlifting Federation (IWF): the sites /robots.txt states;
> - User-agent: *
> - Disallow: /wp-admin/
> - Allow: /wp-admin/admin-ajax.php
> - Sitemap: https://iwf.sport/wp-sitemap.xml
> - It seems the sitemap would be open to a scraper app to access and checking the websites terms of use - i couldnt find anything about fair use of the data-
> - As this is for research purposes and not buisness i hope it would be seen as fair use still -
> the local authority to the iwf is lausanne switzerland whos rules on data access and usage are set by Federal Act on Data Protection (FADP) says alot on what they can do with mydata but i cant find anything on using another sites data. ill continue to research 

> Kaggle - has a data set of summer Olympics Weightlifting records 2000 to 2020
> With competition years, genders, weight classes, bodyweights and records.
> Useful but again the limitation of sources and data variety shows

- Data Transformation: Perform data cleaning, filtering, and transformation operations. This step often involves data normalization, handling missing values, and converting data types.

> International Weightlifting Federation (IWF): The IWF may provide datasets related to Olympic weightlifting, including athlete profiles, competition results, and historical records stored in a online database without an accessible api.
> Becuase of this i will utilise BeautifulSoup to navigate around the site and attain required records, 

> Kaggle's data set is relatively clean from first glance, perhaps this is due to the simplicity of data being handled and recording consitency.
> The data is also stored in a CSV file and so easy to read and navigate.

- Data Validation: Implement data quality checks to ensure data integrity and accuracy. Use libraries like Great Expectations or write custom validation scripts.

> Given how simple the current sample set is this shouldnt require more than basic validation scripts.

- Data Loading: Choose a target database or storage solution to load the transformed data (e.g., PostgreSQL), NoSQL databases (e.g., MongoDB), data warehouses (e.g., Amazon Redshift), or data lakes (e.g., AWS S3).

> I could do all three but seeing as i have used PostgreSQL before it might be best to use MonogoDB or subsitute, aswell as a data warehouse or lake. 

- Automation: Schedule and automate the data pipeline using tools like Apache Airflow, cron jobs, or serverless computing platforms (e.g., AWS Lambda). Automating the pipeline ensures that it regularly updates the data.

> Again this maybe be more in practice than actual intention, that it could be automatically updated if needed.

- Monitoring and Logging: Implement logging and monitoring to track the pipeline's execution and detect issues. Tools like ELK Stack or cloud-specific monitoring services can be used.

> As the provious step I would look to implement this as practice

- Documentation: Document the pipeline thoroughly, including the data source, data schema, transformation steps, and deployment instructions.

> An indepth readme, requirements and commented code will be created, although there could be a standard convention that i could adopt

- Unit Testing: Write unit tests for different components of your data pipeline to ensure reliability and accuracy.

> Creating a sample dataset from the actual dataset and set of unit tests that can be applied as the sample passes through units is my current plan.

- Deployment: Deploy your data pipeline to a production or cloud environment. This could be an on-premises server or a cloud platform like AWS, GCP, or Azure.

> Perhaps this is somehting i should dockerise or use kubernetes for, otherwise i will look into depoloying it most likely to AWS but could be another or aswell as.
  

# Extensions:

-Parameterization: Make the pipeline configurable by allowing users to specify input sources, target destinations, and transformation rules through configuration files.

-Error Handling: Implement error handling and recovery mechanisms in case of pipeline failures.

-Data Versioning: Consider adding data versioning to the pipeline, enabling me trace back to specific versions of the data for reproducibility.

-Scaling: Optimize your pipeline for scalability, allowing it to handle large volumes of data efficiently.
