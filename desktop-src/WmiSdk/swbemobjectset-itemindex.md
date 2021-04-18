---
description: Retourne l’SWbemObject associé à l’index spécifié dans la collection.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: SWbemObjectSet. ItemIndex, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519502"
---
# <a name="swbemobjectsetitemindex-method"></a>SWbemObjectSet. ItemIndex, méthode

La méthode **itemIndex** retourne l' [**SWbemObject**](swbemobject.md) associé à l’index spécifié dans la collection. L’index indique la position de l’élément dans la collection. La numérotation des collections commence à zéro.

## <a name="syntax"></a>Syntaxe


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lIndex* 
</dt> <dd>

Index de l’élément dans la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, l’objet [**SWbemObject**](swbemobject.md) demandé retourne.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode [**Item**](swbemobjectset-item.md) , l’objet **Err** peut contenir l’un des codes d’erreur ci-dessous.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié. Cette erreur est retournée si un numéro d’index négatif est fourni.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

L’élément demandé est introuvable.

</dd> </dl>

## <a name="remarks"></a>Notes

La méthode **itemIndex** permet aux clients WMI des scripts et des applications écrits dans n’importe quel langage de manipuler de manière uniforme une collection comme un tableau. Cette méthode peut être utilisée avec les collections [**SWbemObjectSet**](swbemobjectset.md) . Les requêtes, telles que [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md), [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md) retournent des collections **SWbemObjectSet** . La méthode **itemIndex** ne fonctionne pas avec les collections qui ne contiennent pas de [**SWbemObjects**](swbemobject.md), telles que [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md)et [**SWbemQualifierSet**](swbemqualifierset.md).

**ItemIndex** peut également être utilisé pour obtenir l’instance unique d’une classe singleton.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant recherche une collection de toutes les instances de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) , puis affiche les noms des trois premiers processus.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



Une seule instance de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) existe pour chaque installation du système d’exploitation. La création du chemin d’accès [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) pour obtenir l’instance unique est délicate, de sorte que les scripts énumèrent normalement le **\_ OperatingSystem Win32** , même si une seule instance est disponible. L’exemple de code VBScript suivant montre comment utiliser la méthode **itemIndex** pour accéder à un **\_ OperatingSystem Win32** , sans utiliser de boucle **for each** .


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



L’exemple de code VBScript suivant obtient les instances associées à [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), telles que [**Win32 \_ SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



L’exemple de code suivant affiche des instances associées à [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
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

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

