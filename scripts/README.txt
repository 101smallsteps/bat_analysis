Environment setup

	Software requirements
		Python 3.10
		

	STEP 1 - clone the code 

		git clone https://github.com/101smallsteps/bat_analysis.git
		
	STEP 2 - IDE install 
		As a first step to run the scripts the settings needs to be achieved 

			Install pycharm IDE
				https://www.youtube.com/watch?v=2EB8siO-_OM
				
	STEP 3 - Project setup
		Open the bat_analysis folder from the code downloaded in STEP 1
		
		Open the Terminal tab in the pycharm IDE , located in the lower tabs
			Run the below command 
				pip install -r requirements.txt
				
Process to follow 
	
	STEP 1 - Download the data 
			open the pycharm terminal 
			
			Run the below command 
				python .\scripts\download_yfin.py -sym AAPL  -d 2023-09-30
				
				dir *.csv
				
				you will see three csv files 
				
				quarterly_balance...*csv  (balance sheet)
				quarterly_cash....*csv     (cash flow)
				quarterly_income....*csv    (income statement)
				
	
	STEP 2 - Process the csv to remove the spaces in Field columns using the script below 
	
		input -> quarterly_balance_AAPL_2023-09-30.csv
		output -> quarterly_balance_AAPL_2023-09-30_nsp.csv
		
		python .\scripts\processCSV.py quarterly_balance_AAPL_2023-09-30.csv quarterly_balance_AAPL_2023-09-30_nsp.csv
		
		python .\scripts\processCSV.py quarterly_cash_AAPL_2023-09-30.csv quarterly_cash_AAPL_2023-09-30_nsp.csv
		
		python .\scripts\processCSV.py quarterly_incomestmt_AAPL_2023-09-30.csv quarterly_incomestmt_AAPL_2023-09-30_nsp.csv

	STEP 3 - update csv files
			open the csv files and update the first line as below 
			
			FROM 
				,2023-09-30
			TO
				Field,Value		
		
	STEP 3 - Perform manual analysis for the following metrics 
	
	STEP 5 - Create a report based on your manual analysis
	
	STEP 4 - Update the data and report to the github
	
		copy the *_nsp.csv files to your school data folder, for example at 
			bat_analysis/california/sacramento/95630/FHS/AAPL/2023-09-30/
	
	STEP 5 - Notify your school admin with the report  
	
	
	
		