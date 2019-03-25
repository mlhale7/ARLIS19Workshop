# Open Refine Template for Utah Artists Project

## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
{{if(isBlank(cells['dc:identifier.1'].value), '', '<location><url access="object in context" usage="primary display">' + cells['dc:identifier.1'].value + '</url></location>')}} 
<titleInfo><title>{{cells['dc:title'].value}}</title></titleInfo>
<originInfo>{{if(isBlank(cells['dc:date'].value), '', '<dateCreated>' + cells['dc:date'].value + '</dateCreated>')}}{{if(isBlank(cells['dc:publisher'].value), '', '<publisher>' + cells['dc:publisher'].value + '</publisher>')}}</originInfo>
{{if(isBlank(cells['dc:subject1'].value), '', '<subject' + if(isBlank(cells['dc:subject1_URI'].value), '', ' authority="lcsh" valueURI="' + cells['dc:subject1_URI'].value + '"') + '><topic>' + cells['dc:subject1'].value + '</topic></subject>')}}
{{if(isBlank(cells['dc:language'].value), '', '<language><languageTerm type="code" authority="iso639-2b">' + cells['dc:language'].value + '</languageTerm></language>')}}
{{if(isBlank(cells['dc:rights'].value), '', '<accessCondition>' + cells['dc:rights'].value + '</accessCondition>')}}
</mods>

```

#### Suffix

```
</modsCollection>
```