# Summary

## Item type module creation procedure manual
* [Introduction](README.md)
* [Basic Information](basic-information.md)
* [Detail Information](detail-information.md)
* correspondence of Basic Information and Detail Information

-----
* callback function
* Create a screen
* data manipulation

-----
* installation process
* update process
* uninstall process

-----
* implementation of the data class
* implementation of the handler class

-----
* [Basic Information](basic-information.md)
* index keyword
* Detail Information

-----
* Registration Form request

-----
* registration content confirmation form request

-----
* The item registration request

-----
* edit form request

-----
* Edit content confirmation form request

-----
* item update request

-----
* generation of items Overview

-----
* generation form of Basic Information
* generation form of Detail Information

-----
* Delete the Basic Information

-----
* BasicInformation meta-information

-----
* Search form creation

-----
* statement create a search query \(SQL\)

-----
* license agreement\)
* Export of Detail Information\)

-----
* [Class](class.md)
* class name
* The file name, file path
* implementation of import items class

-----
* implementation of import items handler class

-----
* Other function

-----
* OAI-PMH processing

-----
* Download previous agreement request

-----
* presence or absence of a download of notification
* agreement request block
* change history

## Common library function list
* type function\_name\( argument, …. \)

-----
* function name rules
* Notes of form generation function

-----
* Data structure of Basic Information
* form data structure of Basic Information
* array xnpGetBasicInformationDetailBlock\( int item\_id \)
* array xnpGetBasicInformationEditBlock\( int item\_id \)
* array xnpGetBasicInformationConfirmBlock\( int item\_id \)
* array xnpGetBasicInformationRegisterBlock\(\)
* bool xnpInsertBasicInformation\( int &item\_id \)
* bool xnpUpdateBasicInformation\( int item\_id \)
* bool xnpDeleteBasicInformation\( int item\_id \)

-----
* array xnpGetIndexDetailBlock\( int item\_id, bool button\_flag = true \)
* array xnpGetIndexEditBlock\( int item\_id \)
* array xnpGetIndexConfirmBlock\( int item\_id \)
* array xnpGetIndexRegisterBlock\(\)
* xnpInsertIndex: \(none\)
* bool xnpUpdateIndex\( int item\_id \)
* xnpDeleteIndex: \(none\)

-----
* array xnpGetPreviewDetailBlock\( int item\_id \)
* array xnpGetPreviewEditBlock\( int item\_id \)
* array xnpGetPreviewConfirmBlock\( int item\_id \)
* array xnpGetPreviewRegisterBlock\(\)
* xnpInsertPreview: \(none\)
* bool xnpUpdatePreview\( int item\_id \)
* xnpDeletePreview: \(none\)

-----
* array xnpGetAttachmentDetailBlock\( int item\_id, string name \)
* array xnpGetAttachmentEditBlock\( int item\_id, string name \)
* array xnpGetAttachmentConfirmBlock\( int item\_id, string name \)
* array xnpGetAttachmentRegisterBlock\( string name \)
* xnpInsertAttachemnt: \(none\)
* bool xnpUpdateAttachment\( int item\_id, string name \)
* xnpDeleteAttachemnt: \(none\)
* bool xnpGetDownloadLimitationOptionRegisterBlock\( string dirname, int option = 0 \)
* bool xnpGetDownloadLimitationOptionEditBlock\( string dirname, int option \)
* bool xnpGetDownloadLimitationOptionConfirmBlock\( string dirname \)
* bool xnpGetDownloadNotificationOptionRegisterBlock\( string dirname, int option = 0 \)
* bool xnpGetDownloadNotificationOptionEditBlock\( string dirname, int option \)
* bool xnpGetDownloadNotificationOptionConfirmBlock\( string dirname \)
* bool xnpGetDownloadConfirmationBlock\( int item\_id, int download\_file\_id, bool attachment\_dl\_notify, bool use\_license, int use\_cc, string rights \)

-----
* array xnpGetTextFileDetailBlock\( int item\_id, string name, string text \)
* array xnpGetTextFileEditBlock\( int item\_id, string name, string text \)
* array xnpGetTextFileConfirmBlock\( int item\_id, string name, int maxlen=65535 \)
* array xnpGetTextFileRegisterBlock\( string name \)
* string xnpGetTextFile\( string name \)

-----
* array xnpGetRightsDetailBlock\( int item\_id, int use\_cc=1, string text='', int cc\_commercial\_use=1, int cc\_modification=2 \)\)
* array xnpGetRightsEditBlock\( int item\_id, int use\_cc=1, string text='', int cc\_commercial\_use=1, int cc\_modification=2 \)\)
* array xnpGetRightsConfirmBlock\( int item\_id, int maxlen=65535 \)\)
* array xnpGetRightsRegisterBlock\( \)\)
* array xnpGetRights\(\)\)

-----
* array xnpGetBasicInformationArray\( int item\_id \)
* bool xnpBasicInformation2XML\( resource fhdl, array item, bool is\_absolute, int base\_index\_id=false \)

-----
* array xnpGetBasicInformationAdvancedSearchBlock\( string modulename, array &search\_var \)
* string xnpGetBasicInformationAdvancedSearchQuery\( string moduleName \)
* string xnpGetKeywordQuery \(string dbVarName, string postVarName\)
* array xnpGetKeywordsQueries\( array dbVarNames, array keywords \)
* array xnpKeywordsToFulltextSql\( keywords \)

-----
* string xnpGetBasicInformationMetadata\( string metadataPrefix, int item\_id \)

-----
* array xnpTrimString\( string str, int length, string enc=null \)
* [void xnpTrimColumn\( array &assoc, string table\_without\_prefix, array names=null, string enc=null \)](void-xnptrimcolumn-array-assoc-string-tablewithoutprefix-array-namesnull-string-encnull-.md)
* [void xnpConfirmHtml\( array &assoc, string table\_without\_prefix, array names=null, string enc=null \)](void-xnpconfirmhtml-array-assoc-string-tablewithoutprefix-array-namesnull-string-encnull-.md)
* bool xnpHasWithout\( array assoc \)
* array xnpGetColumnLengths\( string table\_without\_prefix \)
* string xnpWithinWithoutHtml\( string within, string without \)

-----
* [double xnpGetTotalFileSize\( array iids \)](double-xnpgettotalfilesize-array-iids-.md)
* bool xnpIsPending\( int item\_id \)
* string xnpGetTopBlock\( string moduleName, string displayName, string iconPath, string explanation, string subtypeVarName, array subtypes \)
* bool xnpIsAttachmentModified\( string file\_type\_name, int item\_id \)
* string xnpISO8601\( int year, int month, int day \)
* string xnpDate\( int year, int month, int day \)
* bool xnpExportFile\( string export\_path, resource fhdl, int item\_id \)

-----
* [Credits](book/9credits.md)
* [About XOOPS CMS](book/10aboutxoops.md)

