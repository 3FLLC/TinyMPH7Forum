# TinyMPH7Forum
Modern Pascal xBase Tiny Forum

This is the second version of TinyForum. Based upon the previous version which was 61kb of source, this version aims to be smaller while extending the functionality even more. Our previous version was 100kb smaller than "TinyPHPForum" and introduced an array of features that the original code did not have... however, we had elected to build it using INI files instead of text files like the PHP code did. The flaw was, the INI object kept the file in memory, and does not introduce file locking - so obviously it was not multi-user safe.

### v2.0 Design Changes
* The new github will contain two scripts (mkdbfs.p and index.p) - that is the *whole* product!!
* Switched out TINIFile for THalcyonDataset
* Introduced mkdbfs.p (Make all DBF files to instantly spin up a new FORUM!)
* Introduced Bootstrap and jQuery, to improve the GUI (Bootswatch allows you to quick change the look of your Forum!)
* Followed the model of my http://fido.pwnz.org/ fidonet forum
 * allowing your forum to integrate Fidonet forum(s) if you wish!
 * expanded the user levels to support moderators,
 * previewing a post before the world see's it on new users,
 * authenticate a new user via emailed link (SMS support would be nice - hints on how???)
* Added support for QWK offline reader
* Added support for RSS atom feeds

### What exactly does mkdbfs.p do?
* Has 6 embedded emoticons, and generates the css/emoticon.css file as needed.
* Has the default schema for statistics, authentication, etc. and generated the files as needed.
* Has 13 embedded languages, and generates the lang folder i18n strlist for index.p to be multi-lingual.
 * Country Codes are: de, en, es, fi, fr, hu, it, ja, nl, no, pl, sv, zh

### How do I install this, if I am new to Modern Pascal?
* Request the latest release from www.ModernPascal.com
* Install the .conf file in your /etc/httpd/conf.d/ folder
* Install the libmod_mp2.so file in your /etc/httpd/modules/ folder
* /etc/init.d/httpd restart
 * This is it. Only problem may be v2.2 vs 2.4 of Module Framework
 * (copy the other libmod_mp2.so in step 3 and do step 4 again)
