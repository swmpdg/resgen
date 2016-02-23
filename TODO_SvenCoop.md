* Support for: soundlist, globalmodellist, globalsoundlist
* Support for parsing the right column of gmr/gsr files, adding the files to the resource list
* Support for svencoop/, svencoop_hd/ and svencoop_addon/ directories so parameters which verify if the resources exist etc. work correctly
* Skip the line while parsing when the key is "targetname" (only if targetname isn't used for resource files, not sure about that) as this leads to false positives (targetname test3.wav & message test/test.wav -> sound/test3.wav is added to the resource list)
* If possible: For every .mdl found, open the file (only if existing) and check if it inherits/requires additional models like modelT.mdl or model01.mdl etc. - if so, add them to the resource list
