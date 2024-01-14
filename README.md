

# IPS - OSINT PROJECT 

## Case Study
**Evette Slaughter** is someone who approched **Team Recon Rangers** through freelancing platform claiming that her posters are being sold by a facebook page named as "**Anrell Posters**". Now we need to study in detail about them, Let's dive into the OSINT framework for their detailed information gathering

## Strategy Used For Information Gathering
- Facebook Page Link of Anrell Posters Provided by Evette: https://www.facebook.com/profile.php?id=61555345657334
- Phone Number provided on Facebook page: +1 (303) 576-9424
- Reverse Lookup with the phone number.

## Tools Used:
1. **[PhoneInfoga](https://github.com/sundowndev/phoneinfoga/)**
PhoneInfoga is one of the most advanced tools to scan international phone numbers. It allows you to first gather basic information such as country, area, carrier and line type, then use various techniques to try to find the VoIP provider or identify the owner. It works with a collection of scanners that must be configured in order for the tool to be effective. PhoneInfoga doesn't automate everything, it's just there to help investigating on phone numbers.
- Install using the following commands: `bash <( curl -sSL https://raw.githubusercontent.com/sundowndev/phoneinfoga/master/support/scripts/install)`
- Install it globally using `sudo install ./phoneinfoga /usr/local/bin/phoneinfoga` 
- Test to ensure the version you installed is up-to-date `./phoneinfoga version`
- Run the  `scan`  command with the  `-n`  (or  `--number`) option.
`phoneinfoga scan -n "+1 (303) 576-9424"`
`phoneinfoga scan -n "+33 06 79368229`
`phoneinfoga scan -n "33679368229`
- Launching the web server using the following command `phoneinfoga serve` and `
phoneinfoga  serve  -p  8080` respectively.



3. [**That's Them**](https://thatsthem.com/)
- Visit the specific URL in your browser `https://thatsthem.com/reverse-phone-lookup`
- Enter Mobile Number for Lookup.

4. **[Reverse Phone Check](https://www.reversephonecheck.com/)** 
- Browse the website in any browser using the link `https://www.reversephonecheck.com/`
- Enter the phone number for the reverse lookup.
- The specific website will redirect you to [truthfinder.com](https://truthfinder.com/) for the complete report.

5. [**Been Verified**](https://www.beenverified.com/)
- Browse the website `https://www.beenverified.com/`
- Login to your account and search for the specific phone number.


6. **[Sherlock](https://github.com/msaaadd/OSINT-CaseStudy/tree/main/sherlock-master)**
 - Clone the specific repository using the command `git clone https://github.com/sherlock-project/sherlock`
 - Move to your specified folder  using `cd sherlock`
 - Download the specified requirements for installation `python3 -m pip install -r requirements.txt`
 - Now you're good to go with Sherlock, Be a Sherlock
 - You can use sherlock help menu using the command 
 - For the particular scenario we used the ***anika.burell*** as the username in the command `python3 sherlock anika.burell`

*Note: If you're having any errors in the particular tool make sure you have `python3` installed and your pip is updated to the latest version, to update the pip to the latest version run the following command `python3 -m pip install --upgrade pip`*


    

## Final Results of the Information Gathered

|Evette Slaughter| Suspect Scammer |
|--|--|
|Full Name: Evette G Slaughter | Full Name: Anika Burell
|Location: Buffalo, NY|Location: 4641 Fairplay Way, Denver, CO, 80239 |
|Phone: (716) 689-6207|Phone: +1 (303) 576-9424|
|Email: evetteslaughter@gmail.com|  |




## Extra Tools and Tricks
1. **Finding the email of a github user:** 
Follow the following steps to extract email address of github account
```mermaid
graph LR
A[Github User Page] --> B[Choose a Repository] --> C[View Code] --> D[Click Commits] --> E[Click on a commit] --> F[Add `.patch` at the end of the url]
```
This shows email adres of github user who did the commit. 
***Note**: This trick does not work with forked repositories.*
