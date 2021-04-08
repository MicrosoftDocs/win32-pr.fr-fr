---
description: Représente un élément unique dans un objet SWbemRefresher.
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: Objet SWbemRefreshableItem (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem
- ISWbemRefreshableItem
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bc4f85145926aba2bd050052c33eb5669dfee8a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761413"
---
# <a name="swbemrefreshableitem-object"></a>Objet SWbemRefreshableItem

L’objet **SWbemRefreshableItem** représente un élément unique dans un objet [**SWbemRefresher**](swbemrefresher.md) . Un objet **SWbemRefreshableItem** est obtenu par le biais des méthodes [**Add**](swbemrefresher-add.md) et [**AddEnum**](swbemrefresher-addenum.md) de [**SWbemRefresher**](swbemrefresher.md). Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](creating-an-object-using-vbscript.md) .

## <a name="members"></a>Membres

L’objet **SWbemRefreshableItem** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemRefreshableItem** a ces méthodes.



| Méthode                                        | Description                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Installez**](swbemrefreshableitem-remove.md) | Supprime l’objet **SWbemRefreshableItem** de l’objet [**SWbemRefresher**](swbemrefresher.md) parent.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemRefreshableItem** a ces propriétés.



| Propriété                                                       | Type d’accès           | Description                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [**Évaluer**](swbemrefreshableitem-index.md)<br/>         | Lecture/écriture<br/> | Index de l’élément dans son objet [**SWbemRefresher**](swbemrefresher.md) parent.<br/>                                          |
| [**IsSet**](swbemrefreshableitem-isset.md)<br/>         | Lecture/écriture<br/> | Indique si l’objet **SWbemRefreshableItem** représente un objet unique ou un jeu d’objets.<br/>                        |
| [**Dessin**](swbemrefreshableitem-object.md)<br/>       | Lecture/écriture<br/> | Représente un objet [**SWbemObject**](swbemobject.md) unique qui est actualisé.<br/>                                          |
| [**ObjectSet**](swbemrefreshableitem-objectset.md)<br/> | Lecture/écriture<br/> | Représente le jeu d’objets à actualiser.<br/>                                                                                |
| [**Actualisateur**](swbemrefreshableitem-refresher.md)<br/> | Lecture seule<br/>  | Représente l’objet [**SWbemRefresher**](swbemrefresher.md) parent qui contient l’objet **SWbemRefreshableItem** .<br/> |



 

## <a name="remarks"></a>Notes

La méthode VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) ne peut pas être utilisée pour créer des objets **SWbemRefreshableItem** directement.

## <a name="examples"></a>Exemples

Le script suivant illustre la création d’un objet [**SWbemRefresher**](swbemrefresher.md) et l’ajout d’un objet unique et d’un énumérateur **SWbemRefreshableItem** .


```VB
' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " & I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " & process.Name & _
           " Page Faults " & process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    & refresher.Count
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | IID \_ ISWbemRefreshableItem<br/>                                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




