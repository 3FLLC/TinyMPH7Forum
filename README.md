# TinyMPH7Forum
Modern Pascal xBase Tiny Forum

This is the second version of TinyForum. Based upon the previous version which was 61kb of source, this version aims to be smaller while extending the functionality even more. Our previous version was 100kb smaller than "TinyPHPForum" and introduced an array of features that the original code did not have... however, we had elected to build it using INI files instead of text files like the PHP code did. The flaw was, the INI object kept the file in memory, and does not introduce file locking - so obviously it was not multi-user safe.

### v2.0 Design Changes
* Switched out TINIFIle for THalcyonDataset
* Introduced mkdbfs.p (Make all DBF files to instantly spin up a new FORUM!)
* Introduced Bootstrap and jQuery, to improve the GUI (Bootswatch allows you to quick change the look of your Forum!)
* Followed the model of my http://fido.pwnz.org/ fidonet forum
 * allowing your forum to integrate Fidonet forum(s) if you wish!
 * expanded the user levels to support moderators,
 * previewing a post before the world see's it on new users,
 * authenticate a new user via emailed link (SMS support would be nice - hints on how???)
* Added support for QWK offline reader
