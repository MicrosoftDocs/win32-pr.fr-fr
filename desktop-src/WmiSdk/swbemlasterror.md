---
description: Les méthodes et les propriétés de l’objet SWbemLastError contiennent et manipulent des objets Error.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Objet SWbemLastError (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193040"
---
# <a name="swbemlasterror-object"></a>Objet SWbemLastError

Les méthodes et les propriétés de l’objet **SWbemLastError** contiennent et manipulent des objets Error. Les méthodes et les propriétés de cet objet sont exactement les mêmes que celles de l’objet [**SWbemObject**](swbemobject.md) , mais elles sont utilisées pour contenir les informations d’erreur au lieu des informations de classe WMI. Cet objet peut être créé par l’appel VBScript **CreateObject** .

Vous pouvez créer un objet d’erreur **SWbemLastError** pour inspecter les informations d’erreur étendues associées à un appel de méthode précédent. Si les informations sur l’erreur ne sont pas disponibles, une tentative de création d’un objet d’erreur échoue. Si l’appel a échoué et qu’un objet d’erreur retourne, l’état de l’objet est Reset. Toute tentative supplémentaire de récupération d’un objet d’erreur échouera jusqu’à ce qu’une nouvelle erreur se produise. Si vous effectuez un appel asynchrone qui échoue, un objet **SWbemLastError** peut être retourné par l’événement [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) dans le paramètre *objWbemErrorObject* .

## <a name="members"></a>Membres

L’objet **SWbemLastError** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemLastError** a ces méthodes.



| Méthode                                                   | Description                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| **Associateurs\_**                                        | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **AssociatorsAsync\_**                                   | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| [**Clone\_**](swbemlasterror-clone-.md)                 | Effectue une copie de l’objet en cours.<br/>                                               |
| [**CompareTo\_**](swbemlasterror-compareto-.md)         | Teste si deux objets sont égaux.<br/>                                                   |
| **Supprimer\_**                                             | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **DeleteAsync\_**                                        | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **ExecMethod\_**                                         | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **ExecMethodAsync\_**                                    | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| [**GetObjectText\_**](swbemlasterror-getobjecttext-.md) | Récupère la représentation textuelle de l’objet écrit avec la syntaxe MOF.<br/>       |
| **Instances\_**                                          | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **InstancesAsync\_**                                     | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **Posé\_**                                                | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **PutAsync\_**                                           | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **Références\_**                                         | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **ReferencesAsync\_**                                    | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **SpawnDerivedClass\_**                                  | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **SpawnInstance\_**                                      | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **Sous-classes\_**                                         | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |
| **SubclassesAsync\_**                                    | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemLastError** a ces propriétés.



| Propriété                                                      | Type d’accès          | Description                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dérivation\_**<br/>                                   | Lecture seule<br/> | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/>                                                                  |
| **Méthodes\_** <br/>                                     | Lecture seule<br/> | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/>                                                                  |
| [**Chemin d’accès\_**](swbemlasterror-path-.md)<br/>             | Lecture seule<br/> | Contient un objet [**SWbemObjectPath**](swbemobjectpath.md) qui représente le chemin d’accès de l’objet de la classe ou de l’instance actuelle.<br/>                    |
| [**Propriétés\_**](swbemlasterror-properties-.md)<br/> | Lecture seule<br/> | Représente la collection de propriétés de l’objet **SWbemLastError** . Cette propriété est un objet [**SWbemPropertySet**](swbempropertyset.md) .<br/> |
| **Qualificateurs\_**<br/>                                   | Lecture seule<br/> | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/>                                                                  |
| **Caution\_**<br/>                                     | Lecture seule<br/> | Non utilisé. L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.<br/>                                                                  |



 

## <a name="examples"></a>Exemples

L’exemple VBScript suivant montre comment inspecter les informations relatives aux objets Error et Error.


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



L’exemple perl suivant montre comment inspecter les informations relatives aux objets Error et Error.


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




