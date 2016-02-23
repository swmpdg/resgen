* Support for finding soundlist, globalmodellist, globalsoundlist (in bsp + map cfg), + adding the files themselves to the resource list
* Support for parsing the right column of gmr/gsr/txt files, adding the files to the resource list
* Skip the line while parsing when the key is "targetname" (only if targetname isn't used for resource files, not sure about that) as this leads to false positives (targetname test3.wav & message test/test.wav -> sound/test3.wav is added to the resource list)
* If possible: For every .mdl found, open the file (only if existing) and check if it inherits/requires additional models like modelT.mdl or model01.mdl etc. - if so, add them to the resource list -- this actually is option -u, at least for the external texture files, but it throws a bad_alloc right now
* Add auto-generation of the rfa excludes (new parameter?)
* Implement SteamPipeFS https://github.com/ValveSoftware/halflife/blob/5d761709a31ce1e71488f2668321de05f791b405/dmc/cl_dll/cdll_int.cpp#L155
