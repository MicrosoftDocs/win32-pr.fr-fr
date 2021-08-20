---
description: L’objet SWbemRefresher est un objet conteneur qui peut actualiser les données pour tous les objets qui y sont ajoutés. Ensemble d’objets ajoutés, chaque élément représenté par une instance SWbemRefreshableItem peut être traité comme une collection et être énuméré.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Objet SWbemRefresher (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 94e29b7795f113467152b2708aba8b7c3d80b438b8e55b679bddbec4d5107f26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921583"
---
# <a name="swbemrefresher-object"></a>Objet SWbemRefresher

L’objet **SWbemRefresher** est un objet conteneur qui peut actualiser les données de tous les objets qui y sont ajoutés. Les instances uniques et les énumérateurs d’instance peuvent être ajoutés ou supprimés du conteneur. Le jeu d’objets ajoutés, chaque élément représenté par une instance [**SWbemRefreshableItem**](swbemrefreshableitem.md) , peut être traité comme une collection et être énuméré. Les instances WMI de toute classe peuvent être ajoutées à l’objet **SWbemRefresher** . Même si le fournisseur des données d’instance n’est pas un fournisseur à hautes performances, l’objet [**actualisateur**](swbemrefresher-refresh.md) peut toujours mettre à jour les données lors de l’appel d’actualisation. Si les données sont fournies par le biais d’un fournisseur de haute performance et que la propriété [**reconnexion automatique**](swbemrefresher-autoreconnect.md) a la **valeur true**, l’objet **SWbemRefresher** tente de rétablir une connexion rompue au fournisseur de données. Cet objet peut être créé par l’appel VBScript **CreateObject** .

L’opération d’actualisation peut être effectuée en appelant la méthode [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) ou la méthode [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) .

## <a name="members"></a>Membres

L’objet **SWbemRefresher** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemRefresher** a ces méthodes.



| Méthode                                        | Description                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Complémentaires**](swbemrefresher-add.md)             | Ajoute un nouvel objet actualisable à la collection dans l’objet actualisateur.<br/>                   |
| [**AddEnum**](swbemrefresher-addenum.md)     | Ajoute un nouvel énumérateur à l’objet actualisateur.<br/>                                             |
| [**DeleteAll**](swbemrefresher-deleteall.md) | Supprime tous les éléments de la collection dans l’objet actualisateur.<br/>                             |
| [**Élément**](swbemrefresher-item.md)           | Retourne un élément d’actualisation spécifié à partir de la collection.<br/>                                    |
| [**Générer**](swbemrefresher-refresh.md)     | Met à jour tous les éléments contenus dans l’objet actualisateur.<br/>                          |
| [**Installez**](swbemrefresher-remove.md)       | Supprime l’objet d’élément d’actualisation ou le jeu d’objets avec un index spécifié de l’actualisateur.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemRefresher** a ces propriétés.



| Propriété                                                         | Type d’accès          | Description                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Reconnexion automatique**](swbemrefresher-autoreconnect.md)<br/> | Lecture seule<br/> | Indique si l’actualisateur se reconnecte automatiquement à un fournisseur distant si la connexion est interrompue.<br/> |
| [**Count**](swbemrefresher-count.md)<br/>                 | Lecture seule<br/> | Contient le nombre d’éléments dans l’objet actualisateur.<br/>                                                      |



 

## <a name="examples"></a>Exemples

L’exemple suivant illustre la création d’un objet **SWbemRefresher** à l’aide des méthodes [**Add**](swbemrefresher-add.md) et [**AddEnum**](swbemrefresher-addenum.md) pour stocker une instance unique et une instance d’énumération, l’actualisation des données et l’utilisation de la propriété Item pour obtenir les objets [**SWbemRefreshableItem**](swbemrefreshableitem.md) .


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




