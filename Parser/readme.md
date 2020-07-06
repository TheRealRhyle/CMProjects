Notes:
- [ ] Take the raid dump, as its created, and move a copy of it to a custom #location. 
- [ ] Trigger this move each time a new dump occurs. 
- [x] The format of these files are RaidRoster_<server name>-<date-time>.txt.
        Loop 1:
            Check for RaidRoster file.
            ifExist move to (#originals) and copy to (#location)
            Loop

    
2) We have an overlay running on top of eq (much like gina and discord does). When a file pops into CMCustom it triggers the overlay with an editable name field that we can change the dump name plus a field to assign dkp to the dump. Once we submit that data it adjusts the name to (and this is just an example) PlaneofTime-June25-10.txt

Task: Build an a window that can sit on top of a game that is usually transparent and click through unless a specific condition is met.

    If file.created.in(#location){
        in overlay{
            Show Editable name field,
            show DKP field,
            OK/Cancel buttons
        };
        rename file(x) to (Editable_name_field.text + datestamp).txt
    }

Note:  Once we get this piece , designing the web page around it will begin
