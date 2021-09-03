# Printing-in-SOC
The detailed instructions for printing in SOC using terminal :grin:

## Step 1. Transferring files
_(NOTE: This is to be done without SSHing into sunfire)._ 

Use the following command to transfer local files or directories.

Replace /Downloads/lab1 with the proper path and a<span>xxxxxx@<span>sunfire.comp.nus.edu.sg with your actual account. 
```
scp -r ~/Downloads/lab1 axxxxxx@sunfire.comp.nus.edu.sg:~/
```

## Step 2. Logging in to Sunfire
Use the following command to log in to Sunfire:
```
ssh axxxxxx@sunfire.comp.nus.edu.sg
```
Then enter your password. 

## Step 3. Printing
* Check if you have the file you want to print in .ps. 
  
  Otherwise, use the following command to change .pdf to .ps
```
pdftops toPrint.pdf
```

* Now print using the doc printers with this command: 
  
  _(NOTE: name of printer can be found on the printer.)_
```
lpr -Ppstsb print_this.ps
```

* If you want to print multiple pages per sheet, use the following command and then use the previous command to print output.ps.
```
psnup -2up input.ps output.ps
```


### Referenced: 
Printing via Sunfire for NUS SoC Students: https://medium.com/@aaroncql/printing-via-sunfire-for-nus-soc-students-a879ce381630

NUS SOC Handbook/Accessing Sunfire: https://hansel.gitbooks.io/moodle-setup/content/accessing-sunfire.html 
