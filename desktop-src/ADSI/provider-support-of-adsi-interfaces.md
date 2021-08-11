---
title: Prise en charge par le fournisseur des interfaces ADSI
description: le tableau suivant présente une brève description des interfaces prises en charge par les fournisseurs inclus avec ADSI pour Windows 2000 et DS Client.
ms.assetid: 8eb9a88c-cf18-4fe4-b256-1d6fcaf96c62
ms.tgt_platform: multiple
keywords:
- Prise en charge par le fournisseur des interfaces ADSI ADSI
- ADSI ADSI, fournisseurs de services, interfaces prises en charge par chaque fournisseur
- Prise en charge du fournisseur pour IADsUser
- Prise en charge du fournisseur pour IADsComputer
- Prise en charge du fournisseur pour IADsComputerOperations
- Prise en charge du fournisseur pour IADsDomain
- Prise en charge du fournisseur pour IADsFileService
- Prise en charge du fournisseur pour IADsGroup
- Prise en charge du fournisseur pour IADsClass
- Prise en charge du fournisseur pour IADsProperty
- Prise en charge du fournisseur pour IADsSyntax
- Prise en charge du fournisseur pour IADsContainer
- Prise en charge du fournisseur pour IADsNamespaces
- Prise en charge du fournisseur pour IADsAccessControlEntry
- Prise en charge du fournisseur pour IADsAccessControlList
- Prise en charge du fournisseur pour IADsSecurityDescriptor
- Prise en charge du fournisseur pour IADsObjectOptions
- Prise en charge du fournisseur pour IADsCollection
- Prise en charge du fournisseur pour IADsMembers
- Prise en charge du fournisseur pour IADsPathname
- Prise en charge du fournisseur pour IADsPrintQueue
- Prise en charge du fournisseur pour IADsPrintQueueOperations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c393cb8476830617a300f33eac741bd27b3cacbd686442dd4def5bf6c35526e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178828"
---
# <a name="provider-support-of-adsi-interfaces"></a>Prise en charge par le fournisseur des interfaces ADSI

le tableau suivant présente une brève description des interfaces prises en charge par les fournisseurs inclus avec ADSI pour Windows 2000 et DS Client. Une entrée marquée avec « Oui » indique qu’au moins un objet ADSI du fournisseur spécifié prend en charge l’interface associée. « No » indique qu’aucun objet du fournisseur ne prend en charge l’interface dans cette version. À l’avenir, les interfaces actuellement non prises en charge peuvent être prises en charge par les fournisseurs fournis par le système.

Pour plus d’informations sur les détails de l’implémentation spécifique au fournisseur ADSI, consultez :

-   [Fournisseur LDAP ADSI](adsi-ldap-provider.md)
-   [Fournisseur WinNT ADSI](adsi-winnt-provider.md)
-   [ROUTEUR ADSI](adsi-router.md)

Pour plus d’informations sur la propriété ou la méthode prise en charge pour chaque interface, cliquez sur le nom d’interface approprié dans la première colonne de la table.



| Nom de l'interface                                                 | LDAP | NT |
|----------------------------------------------------------------|------|-------|
| [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)                                           | Oui  | Oui   |
| [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)       | Oui  | Non    |
| [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)         | Oui  | Non    |
| [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)                                     | Non   | Non    |
| [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)                           | Non   | Non    |
| [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)               | Non   | Non    |
| [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                 | Oui  | Oui   |
| [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)                       | Non   | Oui   |
| [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                           | Non   | Oui   |
| [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)       | Non   | Oui   |
| [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                         | Oui  | Oui   |
| [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)                         | Oui  | Non    |
| [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                               | Non   | Oui   |
| [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)                                 | Non   | Non    |
| [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)                         | Oui  | Oui   |
| [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)                         | Non   | Non    |
| [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)                     | Non   | Oui   |
| [**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations) | Non   | Oui   |
| [**IADsFileShare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)                         | Non   | Oui   |
| [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                 | Oui  | Oui   |
| [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)                                   | Non   | Non    |
| [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                   | Oui  | Non    |
| [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                           | Oui  | Non    |
| [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                             | Oui  | Oui   |
| [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)                       | Oui  | Oui   |
| [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)                       | Non   | Non    |
| [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)                                         | Oui  | Non    |
| [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)                 | Oui  | Non    |
| [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)                         | Non   | Non    |
| [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                   | Oui  | Oui   |
| [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                       | Oui  | Non    |
| [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)                                   | Non   | Non    |
| [**IADsPathName**](/windows/desktop/api/Iads/nn-iads-iadspathname)                           | Oui  | Oui   |
| [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)                 | Non   | Non    |
| [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)                           | Non   | Oui   |
| [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)       | Non   | Oui   |
| [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)                       | Oui  | Oui   |
| [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)   | Oui  | Oui   |
| [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                           | Oui  | Oui   |
| [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                 | Oui  | Oui   |
| [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                   | Oui  | Oui   |
| [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                 | Oui  | Oui   |
| [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)               | Oui  | Oui   |
| [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)               | Non   | Non    |
| [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource)                           | Non   | Oui   |
| [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)       | Oui  | Non    |
| [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)                             | Non   | Oui   |
| [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)         | Non   | Oui   |
| [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession)                             | Non   | Oui   |
| [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                               | Oui  | Oui   |
| [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)                         | Non   | Non    |
| [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)                         | Non   | Non    |
| [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                   | Oui  | Oui   |
| [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)                   | Oui  | Non    |
| [**Rubrique IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)                   | Oui  | Non    |



 

## <a name="provider-support-for-iadsuser"></a>Prise en charge du fournisseur pour IADsUser



| Propriété                                                    | LDAP          | NT         |
|-------------------------------------------------------------|---------------|---------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | Prise en charge     | Prise en charge     |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | Prise en charge     | Prise en charge     |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | Non pris en charge   | Non pris en charge |
| [**BadLoginCount**](iadsuser-property-methods.md)          | Prise en charge     | Prise en charge     |
| [**department**](iadsuser-property-methods.md)             | Prise en charge     | Non pris en charge   |
| [**Description**](iadsuser-property-methods.md)            | Prise en charge     | Prise en charge     |
| [**Division**](iadsuser-property-methods.md)               | Prise en charge     | Non pris en charge   |
| [**EmailAddress**](iadsuser-property-methods.md)           | Prise en charge     | Non pris en charge   |
| [**EmployeeID**](iadsuser-property-methods.md)             | Prise en charge     | Non pris en charge   |
| [**FaxNumber**](iadsuser-property-methods.md)              | Prise en charge     | Non pris en charge   |
| [**FirstName**](iadsuser-property-methods.md)              | Prise en charge     | Non pris en charge   |
| [**FullName**](iadsuser-property-methods.md)               | Prise en charge     | Prise en charge     |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | Non pris en charge | Non pris en charge   |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | Non pris en charge | Non pris en charge   |
| [**HomeDirectory**](iadsuser-property-methods.md)          | Prise en charge     | Prise en charge     |
| [**HomePage**](iadsuser-property-methods.md)               | Prise en charge     | Non pris en charge   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | Prise en charge     | Prise en charge     |
| [**Langages**](iadsuser-property-methods.md)              | Non pris en charge | Non pris en charge   |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | Prise en charge     | Non pris en charge   |
| [**Lastlogi**](iadsuser-property-methods.md)              | Prise en charge     | Prise en charge     |
| [**LastLogoff**](iadsuser-property-methods.md)             | Prise en charge     | Prise en charge     |
| [**LastName**](iadsuser-property-methods.md)               | Prise en charge     | Non pris en charge   |
| [**LoginHours**](iadsuser-property-methods.md)             | Prise en charge     | Prise en charge     |
| [**LoginScript**](iadsuser-property-methods.md)            | Prise en charge     | Prise en charge     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | Prise en charge     | Prise en charge     |
| [**Gestion**](iadsuser-property-methods.md)                | Prise en charge     | Non pris en charge   |
| [**MaxLogins**](iadsuser-property-methods.md)              | Non pris en charge   | Non pris en charge   |
| [**MaxStorage**](iadsuser-property-methods.md)             | Prise en charge     | Prise en charge     |
| [**NamePrefix**](iadsuser-property-methods.md)             | Prise en charge     | Non pris en charge   |
| [**NameSuffix**](iadsuser-property-methods.md)             | Prise en charge     | Non pris en charge   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | Prise en charge     | Non pris en charge   |
| [**OtherName**](iadsuser-property-methods.md)              | Prise en charge     | Non pris en charge   |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Non pris en charge   | Prise en charge     |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | Prise en charge     | Non pris en charge   |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Non pris en charge   | Prise en charge     |
| [**PasswordRequired**](iadsuser-property-methods.md)       | Prise en charge     | Prise en charge     |
| [**Aperçu**](iadsuser-property-methods.md)                | Prise en charge     | Non pris en charge   |
| [**PostalAddresses**](iadsuser-property-methods.md)        | Prise en charge     | Non pris en charge   |
| [**PostalCodes**](iadsuser-property-methods.md)            | Prise en charge     | Non pris en charge   |
| [**Profil**](iadsuser-property-methods.md)                | Prise en charge     | Prise en charge     |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Non pris en charge   | Non pris en charge   |
| [**SeeAlso**](iadsuser-property-methods.md)                | Prise en charge     | Non pris en charge   |
| [**TelephoneHome**](iadsuser-property-methods.md)          | Prise en charge     | Non pris en charge   |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | Prise en charge     | Non pris en charge   |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | Prise en charge     | Non pris en charge   |
| [**TelephonePager**](iadsuser-property-methods.md)         | Prise en charge     | Non pris en charge   |
| [**Titre**](iadsuser-property-methods.md)                  | Prise en charge     | Non pris en charge   |



 

## <a name="provider-support-for-iadscomputer"></a>Prise en charge du fournisseur pour IADsComputer



| Propriétés                                     | LDAP                    | NT       |
|------------------------------------------------|-------------------------|-------------|
| [**ComputerID**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interface non prise en charge | Non pris en charge |
| [**department**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interface non prise en charge | Non pris en charge |
| [**Description**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Interface non prise en charge | Non pris en charge |
| [**Division**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Interface non prise en charge | Prise en charge   |
| [**Emplacement**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Interface non prise en charge | Non pris en charge |
| [**MemorySize**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Interface non prise en charge | Non pris en charge |
| [**Modèle**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Interface non prise en charge | Non pris en charge |
| [**Adresses**](/windows/desktop/api/Iads/nn-iads-iadscomputer)           | Interface non prise en charge | Non pris en charge |
| [**Exploitation**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Interface non prise en charge | Prise en charge   |
| [**OperatingSystemVersion renvoyée**](/windows/desktop/api/Iads/nn-iads-iadscomputer) | Interface non prise en charge | Prise en charge   |
| [**Propriétaire**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Interface non prise en charge | Prise en charge   |
| [**PrimaryUser**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Interface non prise en charge | Non pris en charge |
| [**Processeur**](/windows/desktop/api/Iads/nn-iads-iadscomputer)              | Interface non prise en charge | Prise en charge   |
| [**ProcessorCount**](/windows/desktop/api/Iads/nn-iads-iadscomputer)         | Interface non prise en charge | Prise en charge   |
| [**Rôle**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Interface non prise en charge | Non pris en charge |
| [**Site**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Interface non prise en charge | Non pris en charge |
| [**StorageCapacity**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Interface non prise en charge | Non pris en charge |



 

## <a name="provider-support-for-iadscomputeroperations"></a>Prise en charge du fournisseur pour IADsComputerOperations



| Propriété                                   | LDAP                    | NT           |
|--------------------------------------------|-------------------------|-----------------|
| [**Correct**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) | Interface non prise en charge | Non implémenté |
| [**État**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)   | Interface non prise en charge | Non implémenté |



 

## <a name="provider-support-for-iadsdomain"></a>Prise en charge du fournisseur pour IADsDomain



| Propriété                                         | LDAP                    | NT           |
|--------------------------------------------------|-------------------------|-----------------|
| [**IsWorkgroup**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                | Interface non prise en charge | Non implémenté |
| [**MinPasswordLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)          | Interface non prise en charge | Prise en charge       |
| [**MinPasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Interface non prise en charge | Prise en charge       |
| [**MaxpasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Interface non prise en charge | Prise en charge       |
| [**MaxBadPasswordsAllowed**](/windows/desktop/api/Iads/nn-iads-iadsdomain)     | Interface non prise en charge | Prise en charge       |
| [**PasswordHistoryLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)      | Interface non prise en charge | Prise en charge       |
| [**PasswordAttributes**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Interface non prise en charge | Non pris en charge     |
| [**AutoUnlockInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Interface non prise en charge | Prise en charge       |
| [**LockoutObservationInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain) | Interface non prise en charge | Prise en charge       |



 

## <a name="provider-support-for-iadsfileservice"></a>Prise en charge du fournisseur pour IADsFileService



| Propriété                                | LDAP                    | NT     |
|-----------------------------------------|-------------------------|-----------|
| [**Description**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)  | Interface non prise en charge | Prise en charge |
| [**MaxUserCount**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) | Interface non prise en charge | Prise en charge |



 

## <a name="provider-support-for-iadsgroup"></a>Prise en charge du fournisseur pour IADsGroup



| Propriété                         | LDAP      | NT     |
|----------------------------------|-----------|-----------|
| [**Description**](/windows/desktop/api/Iads/nn-iads-iadsgroup) | Prise en charge | Prise en charge |



 

## <a name="provider-support-for-iadsclass"></a>Prise en charge du fournisseur pour IADsClass



| Propriété                                   | LDAP               | NT           |
|--------------------------------------------|--------------------|-----------------|
| [**PrimaryInterface**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Prise en charge          | Prise en charge       |
| [**IDENTIFICATEUR**](/windows/desktop/api/Iads/nn-iads-iadsclass)                 | Prise en charge          | Prise en charge       |
| [**OID**](/windows/desktop/api/Iads/nn-iads-iadsclass)                   | Prise en charge          | Prise en charge       |
| [**Résumé**](/windows/desktop/api/Iads/nn-iads-iadsclass)              | Prise en charge          | Prise en charge       |
| [**Appoint**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Prise en charge          | Prise en charge       |
| [**MandatoryProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)   | Prise en charge          | Prise en charge       |
| [**(OptionalProperties)**](/windows/desktop/api/Iads/nn-iads-iadsclass)    | Prise en charge          | Prise en charge       |
| [**NamingProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Prise en charge          | Non implémenté |
| [**DerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Prise en charge          | Non pris en charge     |
| [**AuxDerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)        | Prise en charge          | Non pris en charge     |
| [**PossibleSuperiors**](/windows/desktop/api/Iads/nn-iads-iadsclass)     | Prise en charge          | Prise en charge       |
| [**Containment**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Pris en charge pour la lecture | Prise en charge       |
| [**Conteneur**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Pris en charge pour la lecture | Prise en charge       |
| [**HelpFileName**](/windows/desktop/api/Iads/nn-iads-iadsclass)          | Prise en charge          | Prise en charge       |
| [**HelpFileContext**](/windows/desktop/api/Iads/nn-iads-iadsclass)       | Prise en charge          | Prise en charge       |
| Méthode                                     | LDAP               | NT           |
| [**Qualificateurs**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers) | Non implémenté    | Non implémenté |



 

## <a name="provider-support-for-iadsproperty"></a>Prise en charge du fournisseur pour IADsProperty



| Propriété                            | LDAP      | NT     |
|-------------------------------------|-----------|-----------|
| [**OID**](/windows/desktop/api/Iads/nn-iads-iadsproperty)         | Prise en charge | Prise en charge |
| [**Syntaxe**](/windows/desktop/api/Iads/nn-iads-iadsproperty)      | Prise en charge | Prise en charge |
| [**MaxRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Prise en charge | Prise en charge |
| [**MinRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Prise en charge | Prise en charge |
| [**À valeurs multiples**](/windows/desktop/api/Iads/nn-iads-iadsproperty) | Prise en charge | Prise en charge |



 

## <a name="provider-support-for-iadssyntax"></a>Prise en charge du fournisseur pour IADsSyntax



| Propriété                              | LDAP      | NT     |
|---------------------------------------|-----------|-----------|
| [**OleAutoDataType**](/windows/desktop/api/Iads/nn-iads-iadssyntax) | Prise en charge | Prise en charge |



 

## <a name="provider-support-for-iadscontainer"></a>Prise en charge du fournisseur pour IADsContainer



| Propriété                        | LDAP            | NT           |
|---------------------------------|-----------------|-----------------|
| [**Saut**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Non implémenté | Non implémenté |
| [**Indicateurs**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Prise en charge       | Non implémenté |
| [**Filtres**](/windows/desktop/api/Iads/nn-iads-iadscontainer) | Prise en charge       | Prise en charge       |



 

## <a name="provider-support-for-iadsnamespaces"></a>Prise en charge du fournisseur pour IADsNamespaces



| Propriété                                   | LDAP      | NT     |
|--------------------------------------------|-----------|-----------|
| [**defaultContainer**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) | Prise en charge | Prise en charge |



 

## <a name="provider-support-for-iadsaccesscontrolentry"></a>Prise en charge du fournisseur pour IADsAccessControlEntry



| Propriété                                              | LDAP      | NT       |
|-------------------------------------------------------|-----------|-------------|
| [**AccessMask**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Prise en charge | Non pris en charge |
| [**AccessType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Prise en charge | Non pris en charge |
| [**AccessFlags**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)         | Prise en charge | Non pris en charge |
| [**Indicateurs**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)               | Prise en charge | Non pris en charge |
| [**ObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Prise en charge | Non pris en charge |
| [**InheritedObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) | Prise en charge | Non pris en charge |
| [**Tiers**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)             | Prise en charge | Non pris en charge |



 

## <a name="provider-support-for-iadsaccesscontrollist"></a>Prise en charge du fournisseur pour IADsAccessControlList



| Propriété                                                       | LDAP      | NT       |
|----------------------------------------------------------------|-----------|-------------|
| [**AceCount**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                      | Prise en charge | Non pris en charge |
| [**AceRevision**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                   | Prise en charge | Non pris en charge |
| Méthode                                                         | LDAP      | NT       |
| [**AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace)                 | Prise en charge | Non pris en charge |
| [**CopyAccessList**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-copyaccesslist) | Prise en charge | Non pris en charge |
| [**RemoveAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-removeace)           | Prise en charge | Non pris en charge |
| [**Obtient la \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-get__newenum)   | Prise en charge | Non pris en charge |



 

## <a name="provider-support-for-iadssecuritydescriptor"></a>Prise en charge du fournisseur pour IADsSecurityDescriptor



| Propriété                                                                        | LDAP      | NT       |
|---------------------------------------------------------------------------------|-----------|-------------|
| [**Contrôler**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                       | Prise en charge | Non pris en charge |
| [**DaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Prise en charge | Non pris en charge |
| [**DiscretionaryAcl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                              | Prise en charge | Non pris en charge |
| [**Groupe**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Prise en charge | Non pris en charge |
| [**GroupDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Prise en charge | Non pris en charge |
| [**Propriétaire**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Prise en charge | Non pris en charge |
| [**OwnerDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Prise en charge | Non pris en charge |
| [**SaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Prise en charge | Non pris en charge |
| [**SystemAcl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                     | Prise en charge | Non pris en charge |
| Méthode                                                                          | LDAP      | NT       |
| [**CopySecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecuritydescriptor-copysecuritydescriptor) | Prise en charge | Non pris en charge |



 

## <a name="provider-support-for-iadsobjectoptions"></a>Prise en charge du fournisseur pour IADsObjectOptions



| Méthode                                           | LDAP      | NT                   |
|--------------------------------------------------|-----------|-------------------------|
| [**GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) | Prise en charge | Interface non prise en charge |
| [**SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) | Prise en charge | Interface non prise en charge |



 

## <a name="provider-support-for-iadscollection"></a>Prise en charge du fournisseur pour IADsCollection



| Méthode                                                | LDAP                    | NT       |
|-------------------------------------------------------|-------------------------|-------------|
| [**Ajouter**](/windows/desktop/api/Iads/nf-iads-iadscollection-add)                     | Interface non prise en charge | Non pris en charge |
| [**Obtient la \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) | Interface non prise en charge | Prise en charge   |
| [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscollection-getobject)         | Interface non prise en charge | Prise en charge   |
| [**Installez**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)               | Interface non prise en charge | Prise en charge   |



 

## <a name="provider-support-for-iadsmembers"></a>Prise en charge du fournisseur pour IADsMembers



| Propriété                                           | LDAP                                                      | NT       |
|----------------------------------------------------|-----------------------------------------------------------|-------------|
| [**Saut**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                       | Pris en charge pour GroupCollection, mais pas pour UserCollection | Non pris en charge |
| [**Filtres**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                      | Prise en charge                                                 | Prise en charge   |
| Méthode                                             | LDAP                                                      | NT       |
| [**Obtient la \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum) | Prise en charge                                                 | Prise en charge   |



 

## <a name="provider-support-for-iadspathname"></a>Prise en charge du fournisseur pour IADsPathname



| Propriété                                                    | LDAP      | NT       |
|-------------------------------------------------------------|-----------|-------------|
| [**EscapedMode**](/windows/desktop/api/Iads/nn-iads-iadspathname)                         | Prise en charge | Prise en charge   |
| Méthode                                                      | LDAP      | NT       |
| [**Définie**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)                             | Prise en charge | Prise en charge   |
| [**SetDisplayType**](/windows/desktop/api/Iads/nf-iads-iadspathname-setdisplaytype)       | Prise en charge | Prise en charge   |
| [**Récupération**](/windows/desktop/api/Iads/nf-iads-iadspathname-retrieve)                   | Prise en charge | Prise en charge   |
| [**GetNumElements**](/windows/desktop/api/Iads/nf-iads-iadspathname-getnumelements)       | Prise en charge | Prise en charge   |
| [**GetElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getelement)               | Prise en charge | Prise en charge   |
| [**GetEscapedElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getescapedelement) | Prise en charge | Non pris en charge |
| [**RemoveLeafElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-removeleafelement) | Prise en charge | Prise en charge   |
| [**CopyPath**](/windows/desktop/api/Iads/nf-iads-iadspathname-copypath)                   | Prise en charge | Prise en charge   |



 

## <a name="provider-support-for-iadsprintqueue"></a>Prise en charge du fournisseur pour IADsPrintQueue



| Propriété                                     | LDAP        | NT       |
|----------------------------------------------|-------------|-------------|
| [**PrinterPath**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Prise en charge   | Non pris en charge |
| [**Modèle**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)              | Prise en charge   | Pris en charge.  |
| [**Décimal**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Non pris en charge | Prise en charge   |
| [**PrintProcessor**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)     | Non pris en charge | Prise en charge   |
| [**Description**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Prise en charge   | Prise en charge   |
| [**Emplacement**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Prise en charge   | Prise en charge   |
| [**StartTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Prise en charge   | Prise en charge   |
| [**UntilTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Prise en charge   | Prise en charge   |
| [**DefaultJobPriority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) | Non pris en charge | Prise en charge   |
| [**Priorité**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Prise en charge   | Prise en charge   |
| [**BannerPage**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)         | Prise en charge   | Prise en charge   |
| [**PrintDevices**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Prise en charge   | Prise en charge   |
| [**Adresses**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Non pris en charge | Non pris en charge |



 

## <a name="provider-support-for-iadsprintqueueoperations"></a>Prise en charge du fournisseur pour IADsPrintQueueOperations



| Propriété                                                | LDAP      | NT      |
|---------------------------------------------------------|-----------|------------|
| [**État**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)              | Prise en charge | Prise en charge  |
| Méthode                                                  | LDAP      | NT      |
| [**Suspendre**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-pause)         | Prise en charge | Pris en charge. |
| [**PrintJobs**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-printjobs) | Prise en charge | Prise en charge  |
| [**Purge**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-purge)         | Prise en charge | Prise en charge  |
| [**Reprendre**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-resume)       | Prise en charge | Prise en charge  |



 

 

 




