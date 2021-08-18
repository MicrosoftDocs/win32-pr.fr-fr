---
description: un objet SWbemPrivilegeSet est une collection d’objets SWbemPrivilege dans un objet SWbemSecurity qui demande des privilèges spécifiques pour un objet Windows Management Instrumentation (WMI).
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Objet SWbemPrivilegeSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2117aec6fada67bddce9f07a6c985c73a3dcd93ef217ed7fe77dc46cc5659d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991949"
---
# <a name="swbemprivilegeset-object"></a>Objet SWbemPrivilegeSet

un objet **SWbemPrivilegeSet** est une collection d’objets [**SWbemPrivilege**](swbemprivilege.md) dans un objet [**SWbemSecurity**](swbemsecurity.md) qui demande des privilèges spécifiques pour un objet Windows Management Instrumentation (WMI). Consultez la liste des privilèges dans [**constantes de privilège**](privilege-constants.md). Les éléments sont ajoutés à la collection à l’aide des méthodes [**Add**](swbemprivilegeset-add.md) et [**AddAsString**](swbemprivilegeset-addasstring.md) . Les éléments sont récupérés à partir de la collection à l’aide de la méthode [**Item**](swbemprivilegeset-item.md) et supprimés à l’aide de la méthode [**Remove**](swbemprivilegeset-remove.md) . Cet objet ne peut pas être créé par l’appel de méthode VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) . Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).

Un objet **SWbemPrivilegeSet** est un ensemble de demandes de remplacement de privilège pour un objet spécifique. Lorsqu’un appel d’API est effectué à l’aide de cet objet, les demandes de remplacement de privilège sont tentées. L’objet **SWbemPrivilegeSet** ne définit pas les privilèges disponibles pour l’utilisateur ou le processus actuel. En d’autres termes, l’obtention des privilèges pour n’importe quel objet WMI n’identifie pas les paramètres de privilège établis sur la connexion à WMI, ou les privilèges en vigueur lorsqu’un objet est remis à un récepteur.

## <a name="members"></a>Membres

L’objet **SWbemPrivilegeSet** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemPrivilegeSet** a ces méthodes.



| Méthode                                               | Description                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Complémentaires**](swbemprivilegeset-add.md)                 | Ajoute un objet [**SWbemPrivilege**](swbemprivilege.md) à la collection **SWbemPrivilegeSet** à l’aide d’une constante [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .<br/> |
| [**AddAsString**](swbemprivilegeset-addasstring.md) | Ajoute un objet [**SWbemPrivilege**](swbemprivilege.md) à la collection **SWbemPrivilegeSet** à l’aide d’une chaîne de privilèges.<br/>                                    |
| [**DeleteAll**](swbemprivilegeset-deleteall.md)     | Supprime tous les privilèges de la collection.<br/>                                                                                                              |
| [**Élément**](swbemprivilegeset-item.md)               | Récupère un objet [**SWbemPrivilege**](swbemprivilege.md) de la collection. Il s’agit de la méthode par défaut de cet objet.<br/>                                 |
| [**Installez**](swbemprivilegeset-remove.md)           | Supprime un objet [**SWbemPrivilege**](swbemprivilege.md) de la collection.<br/>                                                                              |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemPrivilegeSet** a ces propriétés.



| Propriété                                            | Type d’accès          | Description                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Count**](swbemprivilegeset-count.md)<br/> | Lecture seule<br/> | Nombre d’éléments dans la collection<br/> |



 

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant obtient un objet SWbemPrivileges et ajoute tous les privilèges disponibles à la collection par valeur de privilège, comme défini dans [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



L’exemple de code VBScript suivant montre comment ajouter des privilèges à l’aide de l’objet **SWbemPrivilegeSet** .


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



L’exemple de code perl suivant montre comment ajouter des privilèges à l’aide de l’objet **SWbemPrivilegeSet** .


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
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
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Exécution des opérations privilégiées](executing-privileged-operations.md)
</dt> <dt>

[Exécution d’opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> <dt>

[**Constantes de privilège**](privilege-constants.md)
</dt> </dl>

 

