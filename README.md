# _libLog2Doc

This is intended to be a Lotusscript Library to use for loggin application critical activities.

Problem. Have the detail log that allows the developer to get the log he wants without disturbing the user in any way. The user may not be aware at all that errors are happening in the code he is activating.
This Lotusscript library allows handling and reporting of Lotusscript errors from within applications in full background, which works even if the user is completely disconnected from the server. These logs were collected via email messages and queued together with the others email messages.
These are some features
- works "remote" and "disconnected", i.e. wherever the Notes client is (also on Nomad web and Nomad Mobile)
- allows to collect logs and debug without disturbing the user. The user can certainly get errors in Messagebox, but collecting the debug log may not tell him anything, so it allows to separate the debug log required by the developer from the one useful for the user to make him understand that something went wrong
- allows you to collect the log and make it available both via email for prompt reporting, such as alerting, and to a centralized application for log registration
- allows you to "activate" even only in "on error" case. That is, the application does not emit any logs if all goes well, but if an "on error" is triggered, the Lib comes into play sending the history of everything that was logged
- shows the normal text of logging messages differently than error messages, and makes it clear where the problem is. The "cluster" of reported errors reports the entire on-error stack in cascade
- does not require a "save" neither "send" action by the code, the save or send is triggered in Delete class destructor, so you can record all of operation from beginning and only at the end or after an error choose whether to save or not

Other features are in the code, located at this repository:
https://github.com/fmarzolo/_libLog2Doc/
