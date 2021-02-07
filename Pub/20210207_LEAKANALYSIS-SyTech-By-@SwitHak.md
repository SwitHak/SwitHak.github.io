# SyTech Leak Analysis

# Introduction
- Сайтэк (SyTech) a national Russian defense contractor has been hacked according several sources. The (@0v1ruS) seems to be the threat actor behind that. 
- The announcement says there's more than 7,5 Terabytes of stolen information. This leak includes several Russian state projects. 

# Intrusion in Sytech
- Screenshots from the threat actor indicates an attack against sytech[.]ru infrastructures and the access of their internal Jira.
![Alt Text](https://pbs.twimg.com/media/D_5xDoXXYAA_wKq?format=jpg&name=small)
![Alt Text](https://pbs.twimg.com/media/D_5xEJEWwAE8wO2?format=jpg&name=small)
![Alt Text](https://pbs.twimg.com/media/D_5xEkGWsAAe9Zx?format=jpg&name=small)
![Alt Text](https://pbs.twimg.com/media/D_5xFGXW4AAOSeh?format=jpg&name=small)


- It's showing the account used to compromise the company network :  "tarasov" was used against an Active Directory under Windows Server 2008 (R2?). 
- A file is uploaded "DuSYKLBE[.]exe.
![Alt Text](https://pbs.twimg.com/media/D_5xFxyWkAADmVS?format=jpg&name=small)

- After that they gained the NT AUTHORITY / SYSTEM Acces on the machine named "AD2008"
- They gained an access to the email server too where they showed the emails addresses in use in the sytech[.]ru domain.
![Alt Text](https://pbs.twimg.com/media/D_5xGZoX4AQxF4H?format=jpg&name=small)

- They gained an Administrator access to the Jira (jira[.]stretch[.]ru and screenshot the projects page.
![Alt Text](https://pbs.twimg.com/media/D_5xHVjXkAYh5yE?format=jpg&name=small)

- We can see they were connected to TITAN Windows server.
- Not confirmed but I would say it's a Windows server 2008 too.
- They've showed first the disks as it and second the hard drive empties, cleaned probably after copying the content. 
![Alt Text](https://pbs.twimg.com/media/D_5xH6pXUAApbH6?format=jpg&name=small)
![Alt Text](https://pbs.twimg.com/media/D_5xIqSXkAAdOEG?format=jpg&name=small)

- These screenshots are from Active Directory Users sytech[.]ru OU before and after the cleaning operation.
![Alt Text](https://pbs.twimg.com/media/D_5xJWHX4AEJ5zn?format=jpg&name=small)
![Alt Text](https://pbs.twimg.com/media/D_5xKC0XkAIUOCj?format=jpg&name=small)

- And the last one is an deface of the www[.]sytech[.]ru website. With a YOBA (Youth Oriented, Bydlo-Approved) Face , also known as ПеКа-фейс which is frequently used by russian trolls on different forums.
![Alt Text](https://pbs.twimg.com/media/D_5xK_pXsAA6iUY?format=jpg&name=small)

- From screenshots, tools used: 
  - proxychains (http://proxychains.sourceforge.net)
  - PSExec (https://docs.microsoft.com/en-us/sysinternals/downloads/psexec)
  - ticketer[.]py (impacket script - based on the work of @gentilkiwi - by @agsolino https://github.com/SecureAuthCorp/impacket/blob/master/examples/ticketer.py)

# Leak analysis

## Project names RU -> EN
- АРИОН -> ARION
- Буйвол -> Buffalo
- Всякое говно -> Every shit
- Гамбит -> Gambit
- Енот -> Raccoon
- камертон -> Kammerton
- Москит -> Mosquito
- Награда -> Reward
- Надежда -> Hope
- Наитие -> Influx
- Наставник -> Mentor
- Настройка -> Customization
- Натиск-2 -> Onslaught-2
- Наутилус -> Nautilus
- Нокаут -> Knockout
- Педант -> Pedant
- Реалия -> Reality
- Спутник -> Satellite
- Эксперт-МПИ ->  Expert-MPI

## Project description (short)
### Expert-MPI:
- Creating a set of software and hardware information and legal support of the state system of legal information

### ARION: 
- System belongs to the class of information-analytical systems and is designed to solve the problems of operative search, communication and analysis of all available heterogeneous information on each object, fact and situation of operative interest.

### Buffalo: 
- Seems to be a software & hardware experimental platform designed to OCR and translate documents.
- Study of the possibility of text recognition in graphic information and construction of a complex of special information processing.

### Gambit:
- project seems to be related to cipher but I don't understand the thing completely.

### coon: 
- pre-project inspection of the objects of placement of the automated system of operational monitoring of processing and distribution of special materials

### Kammerton: 
- Creating a Distributed Protected Computing System

### Mosquito: 
- Study of the possibility of creating a hardware and software complex that performs the functions of search and collection of information materials on the Internet, taking into account the provision of anonymity and concealment of information interest

### Reward: 
- Study on the feasibility of developing SPS penetration and covert use of peer-to-peer and hybrid network resources.

### HOPE: 
- Study on the possibility of developing SPSs that would ensure the accumulation, processing and visualization of technical information on cross-border traffic routes on the Internet

### INFLUX: 
- Exploring the possibility of creating a situational awareness centre in a secure environment (recent, 2018)

### TAX-3: 
- Creating a system which can interface with the Russian IRS databases with the goal of removing information about individuals inside it. 
- The people concerned are state protected like victims, witnesses and other participants in criminal proceedings but also state employees.

### Mentor: 
- Investigation of the possibility of developing an integrated automated system for collecting information
- A big information crawler through different means.

### Customization (or Adjustment): 
- Study of the possibility of developing a hardware-software complex of visualization of analysis of large amounts of special information Visual Data Mining software & infrastructure

### Onslaught-2: 
- creation of a geographically distributed software and hardware complex analysis and development of specialized software

### Reality:
Analyze, determine the characteristics, organize and describe the attributes and metadata of MI (metadata of information materials):
1) text-graphic files and files of electronic books: DOC (X), XLS (X), PPT (X), ODT, ODS, ODP, PDF, RTF, ePUB, ABW;
2) image files: JPEG, PNG, TIFF, GIF;
3) audio & audiovisual files: AVI, MP4 (MPEG/MPG), MP3, FLV, WAV, WebM, OGG, MOV, MKV;
4) archives: ZIP, RAR, TAR, 7Z

Classify identified attributes & metadata of IM in EXIF, IPTC, XMP, Maker standards into the following classes:

1) identification data of the means of preparing the IM or the owner(operating system, software, hardware name and/or network settings,copyright holder of the IM)
2) history of changes in IM (creation, editing)
3) location data (geodata)
4) data on national identity

Examine viewing and editing tools for Windows, Mac OS, nix-derived systems, including
1) Text-graphic and e-book files (Microsoft Office, Apache OpenOffice, FreeOffice, LibreOffice, WPS Office, Abi Word, Ulysses, iA Writer, Adobe Acrobat Reader, Adobe Premier Pro, Icecream Ebook Reader Pro);
2) graphic files (Adobe Photoshop; Adobe Illustrator; Windows Photo Viewer, Microsoft Paint);
3) speech recognition tools with the ability to save the recognition results as a text file: Festival, Balabolk, Real Speaker, Dragon Dictation, Speechlogger;
4) Audio-visual files (Windows Media Player, VLC Media Player, Adobe After Effects, Adobe Audition, Sony Vegas Pro, FL Studio, Blender, Character Creator, Crazy Talk 8 Pipeline);
5) archives: WinRAR, 7-Zip, TAR, GZip.

Explore the tools for viewing and editing IMs for mobile OS:
1) Text and image files for iOS (iA Writer, ByWord, Pages, Bear, Ulysses, Scrivener);
2) Texts and audio-visual files for Android (Polaris Office Standard, Mobisytems OfficeSuite, WPS Office, Acapella);

Explore cloud-based file viewing and editing:
1) Text and image files (Microsoft Office Web Apps, Google Docs, Adobe Document Cloud);
2) Audio-visual files (YouTube Video Editor).

Explore IM conversion software (Format Factory, XMedia Recode, Freemake Video Converter, Any Video Converter, Total Media Converter).
Explore existing software tools that allow for automated modification of IM attributes and metadata, including tools based on Metadata Anonymisation Toolkit and ExifTool libraries.- 
Reality, what a cool project.
Huge work on Metadata by SyTech really.


## Errors, typos, something to say ?
  - Feel free to report any mistake directly below in the comment or in DM on Twitter [@SwitHak](https://twitter.com/SwitHak)
