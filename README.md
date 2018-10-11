# civic-loader
TSV loader for CIViC networks


## **Overview**

This package provides a scripted way to load CIViC networks to NDEx from a flat (tab separated) file.



### **Script**

process_civic.py

_Note: the following python3 package needs to be installed prior to running the script: **ndexutil**_

### **Required parameters**

* username


* password


### **Optional parameters**

* **--server**

   The NDEx server to load the networks to. Default value: **public.ndexbio.org**


* **--file**

   The name of the file to be processed Default value: **civic-nightly.txt**


* **--template**

   The uuid of the network from which the style template will be used.  Default value: **If updating the existing CIViC networks in NDEx then the corresponding templates will be used, otherwise: default NDEx style**


* **--type**

  The type of load plan to use. Default value: **run all types**

  Possible values:


<table>
  <tr>
    <td>Value</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Variant-Drug Associations</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Variant-Disease Associations</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Gene-Disease Associations</td>
  </tr>
  <tr>
    <td>4</td>
    <td>Gene-Variant Associations</td>
  </tr>
  <tr>
    <td>all</td>
    <td>Run 1-4</td>
  </tr>
</table>



### Example:

```
python3 process_civic.py temp 1234 --server public.ndexbio.org --file civic-nightly.txt --template 4ce6075a-cd88-11e8-aaa6-0ac135e8bacf --type all

```



