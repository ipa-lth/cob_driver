^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package cob_undercarriage_ctrl
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.5.3 (2014-03-31)
------------------
* removed obsoledte OpenCV reference
* install tags
* Contributors: ipa-fxm

0.5.2 (2014-03-20)
------------------

0.5.1 (2014-03-20)
------------------
* some install tag updates
* merge with groovy_dev
* cherry-pick
* removed a lot of code related to packages not available in hydro anymore
* bugfix flexible odometry calculation based on number of wheels
* edited odometry calculation so that we are now flexible on how many wheels we use
* odometry calculation for 3 wheels
* upstream changes
* cob_undercarriage_ctrl: expose param for watchdog timeout
* Installation stuff
* Some small dependency tweaks.
* cleaned up CMakeLists and added install directives
* further modifications for catkin, now everything is compiling and linking
* futher include and linkpath modifications
* compiling but still some linker errors
* Second catkinization push
* First catkinization, still need to update some CMakeLists.txt
* cleanup in base_drive_chain and undercarriage_ctrl
* integration of cob_base_velocity_smoother, moved here from cob_navigation
* activated tf publishing out of undercarriagectrl
* cob_undercarriage_ctrl: cleaned and improved ucar_ctrl now working properly on real robot (including recover)
* cob_undercarriage: removed odom_tf that conflicts with robot-pose-ekf in simulation
* Merge remote branch 'origin-ipa320/master' into automerge
* fixed calculation error in transform
* changed odometry frames
* undercarriage adaptions
* cob_undercarriage: reverted changes that made recover impossible -> cpc-pk/ucar
* cob_undercarriage CMakeList fixed
* moved cob_undercarriage Trike ctrl to cob3_intern
* cob_undercarriage_ctrl: changed odometry frames
* cob_undercarriage_ctrl: odom in simulation looks great, in reality not
* cob_undercarriage: cleaned up, odom-improvements tested in simu with navigation
* cob_undercarriage_ctrl: corrected tf-name error
* cob_undercarriage_ctrl: now using timer callback instead of ros::Rate
* cob_undercarriage SIM: corrected wheel geometry parameters of PLatform.ini for simulation modell -> much improved odometry in simulation
* cob_undercarriage_ctrl: improved odometry, doubled odom-rate and doing midpoint integration now
* cob_undercarriage_ctrl: experiments on odometry
* merge
* undercarriage_nt: addings in ini-Files
* comment unused code
* removed compiler warnings
* removed dependency to cob_msgs
* rearranging cob_camera_sensors launch files
* cob_base: communication between controller and driver now directly using joint_command and state topics with pr2::JointTrajectoryControllerState msgs
* added is_moving service for undercarriage_ctrl
* Adaptions in base_drive_chain and undercarriage_ctrl for global /joint_states
* Adapted base_drive_chain to communicate with controller using joint names and not only numbers anymore
* camera settings added for head
* Some adaptions for version 2 of tricycle testplatform
* changed position of topic
* added state topic to base controller
* Merge branch 'master' of https://github.com/ipa-fmw/cob_driver into review-fmw
* additional undercarriage ctrl in simulation
* moved service
* moved Emergency stop message
* modified init_test
* changed trigger service
* cob_base_drive_chain DEBUG. GetJointStates Service replaced through cyclical publishing topic in cob_base_drive_chain
* cleanup in cob_driver
* Moved hard-coded lines for head_axis_homing from CanDriveHarmonica.cpp into ElmoCtrl.cpp. Removed debugger in base_drive_chain.launch and undercarriage_ctrl.launch
* added joint_state_combined to cob_bringup, small device modifications on cob3-1
* Starting base_drive_chain and undercarriage_ctrl with GDB-debugger
* added testing and diag to sdh and base
* some fake covariance
* added watchdog to base controller
* restructured base_controller
* base_drive_chain now can be reverted after EMStop
* base_drive_chain: added main loop with evalCanBuffer to enable ElmoRecorderReadout. NEW: evalCanBuffer is only executed, when and until a readout is in process
* Modified launch files of cob_base_drive_chain, cob_relayboard, cob_undercaariage_ctrl and cob_teleop_ucar and made them hierarchic
* added indirect dependencies (relayboard node, base_drive_chain node) to manifest of under_carriage_ctrlr
* merged with cpc-pk: added ctrl for tricycle-kinematic; specification of limit in CanDriveHarmonica can now be specified via Inifile; base_drive_chain can be operated on variable numbers of motors (lesser or equal to eight); variable setting of path to inifile for UndercarriageCtrlGeom; debugged relaysboard - reads Bus now nonblocking
* removed hard coded entry of camera-axis limit switch in CanDriveHarmonica
* Direct Kinematics, publish effort option in base_drive_chain
* Running in teleop_joystick mode, need small adaptions to EncIncrementsOffset of steering motor
* Controller working for cob3_5 using standart ROS cob3 components
* Made interface of undercarriage_ctrl_geom common for cob3 and cob3_5, adapted some launch files
* Working on cob_undercarriage3_5
* update documentation and deleted tf broadcaster
* modifications for navigation with ucar
* debugging odometry calc
* merging with cpc
* implemented, debugged and tested basic undercarriage controller - works on Descartes principal of rigid body motion
* Deployment of undercarriage controller debugged and finished: launch-script cob_ucar_joy starts up relayboard, base_drive_chain and controller; also remaps topics and services in correct namespaces. Debugging of controller itself is work in progress: simplified and removed old stuff - code compiles - controller runs but appaerently has some bugs -> may not yet be used
* Merge branch 'review-cpc'
* updated simulation files
* debugging undercarriage drivers (base_drive_chain + relayboard + ucar_ctrl) - work in progress
* cleanup in cob_driver
* renamed pltf_command topic in ucarctrl
* debugged ucar controller and base drive chain node - still not running
* Implemented base controller - cob_undercarriage_ctrl - based on principle of rigid body motion; controller is not yet tested on hardware; moreover, not yet used: parameterserver for initializing controller, urdf-file to associate joints; also removed some bugs from base_drive_chain
* added files for undercarriage controller
* Contributors: Alexander Bubeck, Christian, Christian Connette, Richard Bormann, abubeck, cob, cpc, cpc-pk, fmw-jk, ipa-cpc, ipa-fmw, ipa-frm, ipa-fxm, ipa-mig, ipa-srd
