---
title: Scripts LDIF
description: Le format LDIF (LDAP Data Interchange Format) est une norme IETF (Internet Engineering Task Force) qui définit l’importation et l’exportation des données d’annuaire entre les serveurs d’annuaire qui utilisent des fournisseurs de services LDAP.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- Active Directory de scripts LDIF
- Scripts LDIF Active Directory, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad45c51fc16b3c19c3e59f4cfba2e006d4df900c20ce7ddc1b801478a22982c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187083"
---
# <a name="ldif-scripts"></a>Scripts LDIF

Le format LDIF (LDAP Data Interchange Format) est une norme IETF (Internet Engineering Task Force) qui définit l’importation et l’exportation des données d’annuaire entre les serveurs d’annuaire qui utilisent des fournisseurs de services LDAP. Windows 2000 et Windows Server 2003 incluent un utilitaire de ligne de commande, LDIFDE, qui peut être utilisé pour importer des objets d’annuaire dans Active Directory Domain Services à l’aide de fichiers LDIF. LDIFDE vous permet de définir un filtre sur une chaîne spécifique afin de rechercher et de répertorier les objets d’annuaire dans Active Directory Domain Services en tant que fichiers LDIF pouvant être facilement lus par les administrateurs de schéma.

Lors de l’importation d’un fichier Unicode, LDIFDE importe le fichier au format Unicode s’il contient l’identificateur Unicode au début du fichier. Si vous souhaitez importer un fichier au format Unicode lorsqu’il ne contient pas l’identificateur Unicode au début du fichier, vous pouvez utiliser le commutateur-u afin de le forcer à être importé au format Unicode.

Le mode par défaut pour l’exportation des fichiers est ANSI. S’il existe des entrées Unicode, elles sont converties au format 64 de base. Pour exporter un fichier au format Unicode, utilisez le commutateur-u.

Un fichier LDIF doit appliquer des modifications de schéma lorsqu’il existe des dépendances entre les attributs qui sont ajoutés. Par exemple, les attributs de lien suivant doivent être ajoutés avant l’attribut de lien précédent correspondant. Vous devez également mettre à jour le cache de schéma avant d’ajouter des classes qui dépendent des attributs ou des classes ajoutées précédemment dans le script LDIF. Pour plus d’informations, consultez l’exemple de code suivant.

N’oubliez pas que pour les valeurs binaires, vous devez encoder les valeurs au format Base64. L’encodage Base64 est défini dans la norme IETF RFC 2045, section 6,8.

Pour plus d’informations sur le format des fichiers LDIF, consultez [LDAP Data Interchange Format (LDIF)-Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) sur le site Web de l’IETF (Internet Engineering Task Force).

## <a name="ntds-specific-ldif-changetypes"></a>ChangeTypes LDIF spécifique à NTDS

Il est préférable d’utiliser ntdsSchema \* ChangeTypes au lieu d’appeler LDIFDE-k. L’option-k de LDIFDE ignore un plus grand ensemble d’erreurs LDAP. La liste complète des erreurs ignorées est la suivante :

-   L’objet est déjà membre du groupe.
-   Une violation de classe d’objet (c’est-à-dire que la classe d’objet spécifiée n’existe pas), si l’objet en cours d’importation n’a pas d’autres attributs.
-   l’objet existe déjà **( \_ LDAP \_ existe déjà**)
-   violation de contrainte **( \_ \_ violation de contrainte LDAP**)
-   l’attribut ou la valeur existe déjà (**\_ attribut \_ ou \_ valeur \_ LDAP**)
-   aucun objet de ce type (**LDAP \_ non- \_ \_ objet de ce type**)

Les ChangeTypes suivants sont conçus spécifiquement pour les opérations de mise à niveau de schéma.



| ChangeType                      | Description                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ntdsSchemaAdd**<br/>    | **ntdsSchemaAdd** correspond à **Ajouter** dans un fichier LDIF. La seule différence est que **ntdsSchemaAdd** ferait en sorte que LDIFDE ignore une opération d' **Ajout** si l’objet existe déjà dans le schéma. (**LDAP \_ \_ existe déjà** est ignoré.)<br/>                                   |
| **ntdsSchemaModify**<br/> | **ntdsSchemaModify** correspond à **modifier** dans un fichier LDIF. La seule différence est que **ntdsSchemaModify** ferait en sorte que LDIFDE ignore une opération de **modification** si l’objet est introuvable dans le schéma. (**LDAP \_ non \_ , cet \_ objet** n’est pas pris en compte.)<br/>                        |
| **ntdsSchemaDelete**<br/> | **ntdsSchemaDelete** correspond à **Delete** dans un fichier LDIF. La seule différence est que **ntdsSchemaDelete** ferait en sorte que LDIFDE ignore une opération de **suppression** si l’objet est introuvable dans le schéma. (**LDAP \_ non \_ , cet \_ objet** n’est pas pris en compte.)<br/>                        |
| **ntdsSchemaModRdn**<br/> | **ntdsSchemaModRdn** correspond à **modrdn** dans un fichier LDIF. La seule différence est que **ntdsSchemaModRdn** ferait en sorte que LDIFDE ignore une opération de modification relative à un nom unique si l’objet est introuvable dans le schéma. (**LDAP \_ non \_ , cet \_ objet** n’est pas pris en compte.)<br/> |



 

## <a name="example"></a> Exemple

L’exemple de code suivant comprend :

-   Myschemaext. ldf est un script LDIF qui contient de nouveaux attributs et classes. Sachez que ce fichier est une version modifiée du fichier généré à partir de Lgetattcls.vbs. Sachez également que l’attribut **My-test-attribute-DN-FL** a été déplacé en avance de **My-test-attribute-DN-BL** , car le lien de retour (**My-test-attribute-DN-BL**) dépend du lien suivant (**My-test-attribute-DN-FL**). En outre, l’attribut opérationnel **schemaUpdateNow** est défini à deux emplacements pour déclencher les mises à jour du cache de schéma afin que les classes et attributs dépendants soient disponibles pour l’ajout des deux classes dans le script.
    > [!Note]  
    > Consultez la rubrique [obtention d’un ID de lien](obtaining-a-link-id.md) pour plus d’informations sur la source de l’ID dans les instructions LinkId :.

     

-   Lgetattcls.vbs est un fichier VBScript qui génère le script LDIF utilisé comme point de départ pour Myschemaext. ldf. N’oubliez pas que le chemin d’accès au schéma actuel est remplacé par CN = Schema, CN = Configuration, DC = myorg, DC = com. Vous pouvez remplacer DC = myorg, DC = com pour qu’il reflète le nom unique (DN) à publier dans le script LDIF, en vous assurant que LSETATTCLS.VBS reflète la modification apportée à son **sFromDN** de sorte que le nom de domaine correct soit remplacé lors de l’application du script LDIF. Sachez également que le script utilise un préfixe pour rechercher les classes et les attributs. vous devez également définir et utiliser un préfixe pour l’ensemble de vos classes et attributs. Pour plus d’informations, consultez [affectation de noms aux classes et attributs](naming-attributes-and-classes.md). En outre, le script génère uniquement les attributs nécessaires pour les objets **attributeSchema** et **classSchema** dans le fichier LDIF.
-   Lsetattcls.vbs est un fichier VBScript qui utilise le script Myschemaext. ldf pour ajouter les nouveaux attributs et classes du script. Assurez-vous que le contrôleur de schéma est en mesure d’écrire dans avant d’exécuter le script.

## <a name="myschemaextldf"></a>MYSCHEMAEXT. LDF

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a>LGETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a>LSETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





