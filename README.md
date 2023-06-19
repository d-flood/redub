# Redub

A simple desktop GUI for renaming images according to either their "landmark" or "actual folio" number.

This is important because the current CSNTM workflow using CaptureOne results in sequentially named files with no "a" or "b" in the name. E.g., the rectos will be numbered 1–50, adn the versos will be numbered 50–100. This reflects the *shooting order*, but not the natural reading order.

## Usage
- Install via a terminal by running `python -m pip install redub`
- Start the app by running `python -m redub`
- Select the Excel spreadsheet that was generated for the artifact.
- Select the directory containing the files exported from CaptureOne
- Choose whether to rename the files according to the "landmark" or "actual folio" column in the spreadsheet.
- Enter the original text and replacement text (because the holding institution probably will not want our naming convention). Here we can swap our naming for theirs.
Finally, choose whether to rename the files in place or make copies with the new names and leave the originals untouched.

## Current Limitation
This will currently only work on the Lambeth images which were taken using the workflow explained above. For images taken after June 2023, we expect that there will **not** be an Excel spreadsheet, instead there will be a JSON file. `Redub` will need to be updated to accept JSON as an optional input format. This will be very easy, because all `Redub` does with an Excel file is convert it to a Python list of dictionaries.