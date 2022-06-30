# Copying and Modifying the Website
While I have the website running for everyone to access, if you would like to run it locally,
or modify any of the code, I have left it available to access.

#Copying the code
The website is located at: `/data/aneurysm/pandol75/DeepAneurysmWebsite`
You can copy the code to your local repository by typing the command:
```
cp -r /data/aneurysm/pandol75/DeepAneurysmWebsite
```
At the moment, all of the necessary files are contained within this folder. There is no parts of the site that
call upon files from other parts of the Lambda server. As such, you can transfer this to your local machine without issue.

#Running the website
To run the website, you need Streamlit installed. In your python environment, you can type:
```
pip install streamlit
```
Then, when in the DeepAneurysmWebsite folder, run:
```
streamlit run app.py
```
If you are running it on your local machine, this should automatically open the website in your browser,
and display the IP address on your console. However, I have found that with Lambda, it sometimes
struggles displaying the IP. So, to get around this, you should first run
```
hostname -I
```
This will get you the IP address. The port will usually be **8501**, however if other instances of the
site are currently running, it may be **8502** or **8503**, etc. So, examples of the full address
would be:
**http://10.240.37.18:8501/**
**http://10.240.37.18:8502/**

#Modifying the website
All of the unique code for the website is located in `app.py`. The other files in the folder
come from fasterRCNN, and are used to help run Faster on the site. These could be called
from another location, but they are included here, for ease-of-access. So, if you would
like to make changes to the site, `app.py` should be all you touch.

There are two other folders within the DeepAneurysmWebsite folder, fasterrcnnWeights,
and websiteAssets. They contain what the name describes. The faster folder contains
the 5 .pth files that are used in the site's code. However, they can very easily
be swapped for others. The websiteAssets folder contains all graphics for the site,
such as the Rowan logo, the informational video, and all of the sample images
used for the models.

There is also a README.txt file in the folder to provide similar info about
the website.

#Conclusion
This should provide you with all the tools necessary to use and edit the DeepAneurysm
Website. If you have any questions, reach out to me at `pandol75@students.rowan.edu`, and
I will do my best to get back to you and help out.
