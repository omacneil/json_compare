# DEPRECATED

The [diffant](https://github.com/omacneil/diffant) project does everything
json_compare does and more. For example, it handles yaml and ini in addition
to json.  Unless you like ruby more than python, you should use diffant.

# json_compare

See how keys and values differ between json files. Works better than diff for
more than 2 files or structures that are deeply nested or aren't line oriented.
Originally made to compare chef environment attribute files.

# USAGE

```bash
./json_compare DIRECTORY
```
# SAMPLE OUTPUT
```code
  :color:red:file01.json
  :color:red:file02.json
  :color:red:file03.json
  :color:red:file04.json

  :fruit:apple:file01.json
  :fruit:cherry:file02.json
  :fruit:apple:file03.json
  :fruit:MISSING:file04.json

  :inspiration:art:Pablo Picasso:file01.json
  :inspiration:art:Frida Kahlo:file02.json
  :inspiration:art:Pablo Picasso:file03.json
  :inspiration:art:MISSING:file04.json

  :inspiration:music:Dead Kennedys:file01.json
  :inspiration:music:Dead Kennedys:file02.json
  :inspiration:music:Dead Kennedys:file03.json
  :inspiration:music:MISSING:file04.json

  :inspiration:tools:MISSING:file01.json
  :inspiration:tools:["hammer", "rack"]:file02.json
  :inspiration:tools:MISSING:file03.json
  :inspiration:tools:MISSING:file04.json

  :vegetable:MISSING:file01.json
  :vegetable:MISSING:file02.json
  :vegetable:spinach:file03.json
  :vegetable:MISSING:file04.json
```

# SAMPLE INPUT
### file01.json
```json
{
   "color": "red",
   "fruit": "apple",
   "inspiration": {"art":"Pablo Picasso","music":"Dead Kennedys"}
  }
```
### file02.json
```json
  {
   "color": "red",
   "fruit": "cherry",
   "inspiration": {"art":"Frida Kahlo","music":"Dead Kennedys","tools":["hammer","rack"]}
  }
```

### file03.json
```json
 {
   "vegetable": "spinach",
   "color": "red",
   "fruit": "apple",
   "inspiration": {"art":"Pablo Picasso","music":"Dead Kennedys"}
  }
```
### file04.json
```json
{
   "color": "red"
  }
```
# REQUIREMENTS
1. Ruby
2. The ruby-json library

```code
sudo apt install ruby ruby-json`
```





