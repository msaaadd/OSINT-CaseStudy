# ${\textcolor{Red}{IPS \ - \ OSINT \ PROJECT}}$

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
-Lauch the browser and enter `http://<localhost>:<PORT-NUMBER>`

2. [**That's Them**](https://thatsthem.com/)
By Thats Them can search for people by name and address, phone number, just the address, an email address, or an IP address. ThatsThem returns a wealth of information, including address, phone number, email address, length of residence, household size, IP address, age range, estimated net worth, estimated income, education, occupation, language, and then it scores each person on wealth, green, donor, travel, tech, and shopping.
- Visit the specific URL in your browser `https://thatsthem.com/reverse-phone-lookup`
- Enter Mobile Number for Lookup.

3. **[Reverse Phone Check](https://www.reversephonecheck.com/)** 
A reverse phone number lookup/ phone number lookup is exactly what it sounds like – a tool that allows users to enter a phone number and find out the name of the person to whom the number belongs! This is the reverse of the traditional, physical phone books where you search for a person's phone number, hence the name!
- Browse the website in any browser using the link `https://www.reversephonecheck.com/`
- Enter the phone number for the reverse lookup.
- The specific website will redirect you to [truthfinder.com](https://truthfinder.com/) for the complete report.

4. **[Sherlock](https://github.com/msaaadd/OSINT-CaseStudy/tree/main/sherlock-master)**
Sherlock is an open-source intelligence (OSINT) tool to gather information about a specific username or online identity. One of the main features of Sherlock is its ability to search for a specific username across multiple social media platforms and websites.
 - Clone the specific repository using the command `git clone https://github.com/sherlock-project/sherlock`
 - Move to your specified folder  using `cd sherlock`
 - Download the specified requirements for installation `python3 -m pip install -r requirements.txt`
 - Now you're good to go with Sherlock, Be a Sherlock
 - You can use sherlock help menu using the command 
 - For the particular scenario we used the ***anika.burell*** as the username in the command `python3 sherlock anika.burell`

5. **[Blackbird](https://github.com/p1ngul1n0/blackbird)**
The primary purpose of this OSINT tool is to find all the social accounts from 120 social media websites. As the creator believes, this tool scans different 120 websites.
- Clone the specific repository using the command `git clone https://github.com/p1ngul1n0/blackbird`
- Move to your specified folder using `cd blackbird` 
- Download the specified requirements for installation  `pip install -r requirements.txt`
- Now you're a blackbird, be a good one 
- You can use blackbird for seaching usernames through `python blackbird.py -u username`
- Lets deploy on our webserver `python blackbird.py --web`
- Access `http://127.0.0.1:9797` on the browser
- Read results file using `python blackbird.py -f username.json`
- List supported sites `python blackbird.py --list-sites`

6. [**Been Verified**](https://www.beenverified.com/)
BeenVerified empowers consumers to learn more about people by providing access to public record information like criminal history, contact info and more. BeenVerified is dedicated to helping search people and learn more about them in a safe and responsible manner.
- Browse the website `https://www.beenverified.com/`
- Login to your account and search for the specific phone number.


*Note: If you're having any errors in the particular tool make sure you have `python3` installed and your pip is updated to the latest version, to update the pip to the latest version run the following command `python3 -m pip install --upgrade pip`*



## Extra Tools and Tricks
1. **Finding the email of a github user:** 
Follow the following steps to extract email address of github account
```mermaid
graph LR
A[Github User Page] --> B[Choose a Repository] --> C[View Code] --> D[Click Commits] --> E[Click on a commit] --> F[Add `.patch` at the end of the url]
```
This shows email adres of github user who did the commit. 
***Note**: This trick does not work with forked repositories.*
2. **OSINT Dojo:** https://www.osintdojo.com/
3.  **Is Your Data Breached:** https://haveibeenpwned.com/
4. **OSINT Techniques:** https://www.osinttechniques.com/
5. **OSINT Frameworks:** https://osintframework.com/

## Disclaimer
This or previous program is for Educational purpose ONLY. Do not use it without permission.The usual disclaimer applies, especially the fact that me (P1ngul1n0) is not liable for any damages caused by direct or indirect use of the information or functionality provided by these programs. The author or any Internet provider bears NO responsibility for content or misuse of these programs or any derivatives thereof. By using these programs you accept the fact that any damage (dataloss, system crash, system compromise, etc.) caused by the use of these programs is not [msaaadd's](https://github.com/msaaadd/) responsibility.
