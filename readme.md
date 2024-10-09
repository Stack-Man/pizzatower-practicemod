Steps to patch:

1. Create obj_practice_mod and obj_tas_tool objects first (code comes later). Mark both as persistent.
2. Create scr_getpracticeinput and scr_tas_tools and add code
3. Modify all other files
4. Create and add code for all obj_practice_mod and obj_tas_tool files. Set step to beginStep and draw to drawGUI
5. For obj_debugcontroller_step_0:

5a. Replace all instances of self.DoCommand with just DoCommand

5b. In disassembly, replace the following line:

call.i DoCommand(argc=1)

With the following lines:

call.i @@This@@(argc=0)

push.v builtin.DoCommand

callv.v 1

5c. Remove "DoCommand" from the list of functions on the side of UTMT

6. Place an instance of obj_tas_tool and obj_practice_mod in the room Loadiingroom (mispelling is correct)

If you get the error "could not save do to some error in the save function", just change any file and undo it, then save.
