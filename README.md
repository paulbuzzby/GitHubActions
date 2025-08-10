# GitHubActions
A dumping grounds for github automation files

# KiCad Document extractor

Drop the kibot-autodiscover.yml into the .github\workflows folder 
Drop config.kibot.yaml into the root

This action will find ALL kicad projects within the repo

 - Create a PDF export of the schematic
 - Create a CSV of the BOM 
 - Will export a fixed column and requires the Notes and RSONLINE field to exist. Field names are case sensitive (I think)
 - Create a PCB render of the viewed from the top
 - Create a PCB render viewed from the bottom

These will get added to a root docs\ folder with a folder being created for each KiCAD project. The 4 files will be put into the folder

It will then combine ALL of the found *_bom.csv files within the docs\ folder to create a single all_project_bom.csv

Further improvements could be made to run DRC checks and auto create gerbers etc
