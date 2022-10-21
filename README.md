Use tess4j on mac to convert scanned pdf to searchable.

## Getting Started

1. Clone the repo: 

``` shell 
git clone git@github.com:pexa-AAppuhamy/mdeed-tess4j
```
2. Ensure Tessaract is installed using homebrew.
``` shell 
brew install tesseract
```
3. Determine the directory where tesseract is installed on your device using:
``` shell 
brew info tesseract
```
![tesseract location](docs/tessloc.png)

4. Copy the dynamic library file to the root directory of where the repo was cloned.
``` shell 
cp <path/to/tesseract(step3)>/lib/libtesseract.5.dylib <path-to-repo-root-dir>
```
5. Open the application in Intellij, and add the following environment variable to run/debug configuration.
``` shell 
TESSDATA_PREFIX=<path/to/tesseract(step3)>/share/tessdata
```
![tesseract env variable](docs/tessenv.png)

6. Build and run the application it will output to console the scanned document image within assets folder.
