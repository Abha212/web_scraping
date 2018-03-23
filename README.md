# web_scraping
This project scrapes various borrower/loan details from Sales prospectuses filed by Lending Club with the SEC. Lending Club is a 
peer-to-peer online lending marketplace that facilitates unsecured personal loans to US borrowers in the range of $4,000-$10,000. More 
specifically, it enables US borrowers raise funds directly from investors (both retail & institutional investors) via its platform and
earns fees from loan originations and servicing. 

While loan/borrower details can be easily scraped from SEC filings, much of this info is already provided in a comprehensive 
format by Lending Club on its website.  Therefore instead of scraping all details from filings, I focus my attention on 
3 relevant items that aren't available via Lending Club:
1. Borrower FICO scores aren't available with the traditional loan data. Only if you are an investor with Lending Club can you obtain 
loan-level info on FICO scores. 
2. I scrape data on each loan's complete origination date i.e. after a loan has successfully secured funding from investors. In 
Lending Club's data, we see the origination month/year of a loan but not the actual date. This date can be used to investigate and 
find evidence for weekly/monthly sales pressures potentially faced by Lending Club originators especially after going public in Dec 2014. 
3. I also scrape data on the request dates of loans i.e. when borrowers initially post their loans on Lending Club's platform. By 
comparing the difference between a loan's successful completion date and its initial request date, we can identify which 
types of loans were "more in demand" and "less in demand" by investors. 

According to Rule 424(b) of the Securities Act of 1933, Lending Club is required to file two types of prospectuses with the SEC - (a) details of all loans offered to investors and (b) details of loans actually sold to investors. I am interested in only identifying the Sales filings as these details can be combined with other borrower/loan details to investigate economic questions like Likelihood of default, prepayment and credit scoring. Note: historically many prospectus and sales documents have been filed by Lending Club. 

[SEC filings for Lending Club](https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0001409970&type=424B3&dateb=&owner=exclude&count=40)

Author: Abha Kapoor

Code: Python, pandas, bs4, requests
