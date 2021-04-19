---
description: Utilisez les méthodes et les propriétés de l’objet SWbemObjectPath pour construire et valider un chemin d’accès à un objet. Cet objet peut être créé par l’appel VBScript CreateObject.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Objet SWbemObjectPath (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518609"
---
# <a name="swbemobjectpath-object"></a>Objet SWbemObjectPath

Utilisez les méthodes et les propriétés de l’objet **SWbemObjectPath** pour construire et valider un chemin d’accès à un objet. Cet objet peut être créé par l’appel VBScript **CreateObject** .

## <a name="members"></a>Membres

L’objet **SWbemObjectPath** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemObjectPath** a ces méthodes.



| Méthode                                                   | Description                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [**SetAsClass**](swbemobjectpath-setasclass.md)         | Force le chemin d’accès à l’adresse d’une classe WMI.<br/>              |
| [**SetAsSingleton**](swbemobjectpath-setassingleton.md) | Force le chemin d’accès à l’adresse d’une instance WMI Singleton.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemObjectPath** a ces propriétés.



| Propriété                                                              | Type d’accès           | Description                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Authority**](swbemobjectpath-authority.md)<br/>             | Lecture/écriture<br/> | Chaîne qui définit le composant d’autorité du chemin d’accès de l’objet.<br/>                                                                                                           |
| [**Classe**](swbemobjectpath-class.md)<br/>                     | Lecture/écriture<br/> | Nom de la classe qui fait partie du chemin d’accès de l’objet.<br/>                                                                                                                        |
| [**NomComplet**](swbemobjectpath-displayname.md)<br/>         | Lecture/écriture<br/> | Chaîne qui contient le chemin d’accès dans un formulaire qui peut être utilisé comme nom d’affichage du moniker. Consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).<br/> |
| [**IsClass**](swbemobjectpath-isclass.md)<br/>                 | Lecture seule<br/>  | Valeur booléenne qui indique si ce chemin d’accès représente une classe. Cela est analogue à la propriété [ \_ \_ genre](wmi-system-properties.md) de l’API com.<br/>                    |
| [**IsSingleton**](swbemobjectpath-issingleton.md)<br/>         | Lecture seule<br/>  | Valeur booléenne qui indique si ce chemin d’accès représente une instance singleton.<br/>                                                                                                |
| [**Keys**](swbemobjectpath-keys.md)<br/>                       | Lecture seule<br/>  | Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui contient les liaisons de valeur de clé.<br/>                                                                          |
| [**Paramètres régionaux**](swbemobjectpath-locale.md)<br/>                   | Lecture/écriture<br/> | Chaîne qui contient les paramètres régionaux pour le chemin d’accès de cet objet.<br/>                                                                                                                     |
| [**Espace de noms**](swbemobjectpath-namespace.md)<br/>             | Lecture/écriture<br/> | Nom de l’espace de noms qui fait partie du chemin d’accès de l’objet. Il s’agit de la même propriété d' [ \_ \_ espace de noms](wmi-system-properties.md) dans l’API com.<br/>                        |
| [**ParentNamespace**](swbemobjectpath-parentnamespace.md)<br/> | Lecture seule<br/>  | Nom du parent de l’espace de noms qui fait partie du chemin d’accès de l’objet.<br/>                                                                                                      |
| [**D**](swbemobjectpath-path.md)<br/>                       | Lecture/écriture<br/> | Contient le chemin d’accès absolu. Il est identique à la propriété système [ \_ \_ path](wmi-system-properties.md) dans l’API com. Il s’agit de la propriété par défaut de cet objet.<br/>    |
| [**Constitue**](swbemobjectpath-relpath.md)<br/>                 | Lecture/écriture<br/> | Contient le chemin d’accès relatif. Il est identique à la propriété système [ \_ \_ RelPath](wmi-system-properties.md) dans l’API com.<br/>                                              |
| [**Sécurité\_**](swbemobjectpath-security-.md)<br/>            | Lecture seule<br/>  | Utilisé pour lire ou modifier les paramètres de sécurité.<br/>                                                                                                                             |
| [**Serveur**](swbemobjectpath-server.md)<br/>                   | Lecture/écriture<br/> | Nom du serveur. C’est la même chose que la propriété système du [ \_ \_ serveur](wmi-system-properties.md) dans l’API com.<br/>                                                       |



 

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant montre comment générer des chemins d’accès aux objets.


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



L’exemple de code perl suivant montre comment générer des chemins d’accès aux objets.


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
  }
  else
  {
   print STDERR Win32::OLE->LastError, "\n";
  }
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




