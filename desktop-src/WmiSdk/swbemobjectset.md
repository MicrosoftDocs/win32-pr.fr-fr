---
description: Un objet SWbemObjectSet est une collection d’objets SWbemObject. Pour plus d’informations, consultez accès à une collection. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Objet SWbemObjectSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 33cefd39dc0e860906bc99b1f591a87dae845d6a9317410ce4850fb1a54ea708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857099"
---
# <a name="swbemobjectset-object"></a>Objet SWbemObjectSet

Un objet **SWbemObjectSet** est une collection d’objets [**SWbemObject**](swbemobject.md) . Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md). Cet objet ne peut pas être créé par l’appel VBScript **CreateObject** .

Vous pouvez récupérer un objet **SWbemObjectSet** en appelant l’une des méthodes suivantes ou leurs équivalents asynchrones :

-   [**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)
-   [**SWbemObject. instances\_**](swbemobject-instances-.md)
-   [**SWbemObject. References\_**](swbemobject-references-.md)
-   [**SWbemObject. Subclasses\_**](swbemobject-subclasses-.md)
-   [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)

> [!Note]  
> L’objet **SWbemObjectSet** ne prend pas en charge les méthodes facultatives **Add** et **Remove** collection.

 

> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser la fonction semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

## <a name="members"></a>Membres

L’objet **SWbemObjectSet** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemObjectSet** possède ces méthodes.



| Méthode                              | Description                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**Élément**](swbemobjectset-item.md) | Récupère un objet [**SWbemObject**](swbemobject.md) à partir de la collection. Il s’agit de la méthode par défaut de l’objet.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemObjectSet** possède ces propriétés.



| Propriété                                                  | Type d’accès          | Description                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Count**](swbemobjectset-count.md)<br/>          | Lecture seule<br/> | Nombre d’éléments dans la collection<br/>        |
| [**Sécurité\_**](swbemobjectset-security-.md)<br/> | Lecture seule<br/> | Utilisé pour lire ou modifier les paramètres de sécurité.<br/> |



 

## <a name="remarks"></a>Remarques

Une collection **SWbemObjectSet** est une collection de zéro ou plusieurs objets [**SWbemObject**](swbemobject.md) . Chaque **SWbemObject** dans une **SWbemObjectSet** peut représenter l’un des deux éléments suivants :

-   Instance d’une ressource managée par WMI.
-   Instance d’une définition de classe.

L’utilisation la plus courante de cette classe dans WMI est la valeur de retour pour un appel [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) ou [**InstancesOf**](swbemservices-instancesof.md) , comme décrit dans l’exemple de code suivant :


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



Pour l’essentiel, la seule chose que vous feriez avec une **SWbemObjectSet** est d’énumérer tous les objets contenus dans la collection elle-même. Toutefois, **SWbemObjectSet** inclut un nombre de propriétés qui peut être utile dans les scripts d’administration de système. Comme son nom l’indique, count indique le nombre d’éléments dans la collection. Par exemple, ce script récupère une collection de tous les services installés sur un ordinateur, puis renvoie le nombre total de services trouvés :

Pour plus d’informations sur l’utilisation de cette classe, consultez [énumération de WMI](enumerating-wmi.md).

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant illustre la manière dont les collections **SWbemObjectSet** sont manipulées.


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



L’exemple de code perl suivant illustre la manière dont les collections **SWbemObjectSet** sont manipulées.


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
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
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




