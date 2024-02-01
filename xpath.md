# xpath
- Xpath stands for XML path language.
- Is used to find the location of an element on a webpage using HTML document object model.
- Xpath = //tagname[@Attribute='value']

```
/html/body/div/h1  # get h1 element
//*[@id='firstname'] # get element with id equals firstname
//input[@name='firstname'] # get element with id equals firstname
```

# 2 type of Xpath (ví dụ trên)
## Absolute xpath
- contains the complete path from the root element of page to the element.
- start with single slash (/)
## Relative xpath
- Start from the middle of HTML DOM structure.
- Start with double slash(//)


# Xpath function - "starts-with"
- for finding dynamic web elements also static elements
- format: ```xpath = //tagname[starts-with(@attribute, 'value')]```
- 
