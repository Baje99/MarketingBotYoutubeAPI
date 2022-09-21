"""
This bot was created by Baje99 in python using SendGrind and YoutubeAPI

This code will loop through a csv file introduced manually(which will contain the company website and mail address) and check if every website have an youtube channel.
If it has, it will verify if the channel is active( by the video duration and date posted by the operator), it will scrap the data from the video and the channel including their social links and it will save it an CSV file.
After, an email will be send with SendGrid to the address specified offering the option to increase his channel engagement.
N O T E S !
As it is considered an personal information, the email address can't be scraped from youtube as it is protected by a CAPTCHA code, so it has to be introduced manually.
Youtube API doesn't allow to make more than 10.000 quotes per day( check console.clould.google.com to see your remaining quotes) so the maximum requests will be about 48-50 channels per day!

Used libraries will be posted in requirements.txt

In order to function you will need to create accounts on SendGrid and GoogleDevelopers(which is free to do) and insert in the main.py the specified API keys.

If you need help regarding the account creation process here are some videos:

SendGrid: https://www.youtube.com/watch?v=xCCYmOeubRE
P.S. Remember to specify the FullAccess when creating the key otherwise it won't work. Also you will need to create a sender domain(the email address from which the email will be sent)
What you will have to insert from here:

message = Mail(
        from_email= your emaill addres created in the sender section,
        ...

sg = SendGridAPIClient( your API KEY)

YoutubeAPI:  https://www.youtube.com/watch?v=th5_9woFJmk&t=991s
What you will have to insert from here:
youtube = build('youtube', 'v3', developerKey= your YoutubeAPI KEY)

N O T E S:
Problems that will be solved soon:
- The company website from the csv doesn't have the domain_name included in the url. Example: www.ar.capital or www.before.tomorrow ( this will search for "ar" and "before" on youtube)
- Most of the companies have their youtube channels similar to their domain_name, but that's not the case so it might not find all youtube channels.

"""
