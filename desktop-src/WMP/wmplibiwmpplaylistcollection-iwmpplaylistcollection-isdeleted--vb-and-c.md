---
title: IWMPPlaylistCollection isDeleted, méthode
description: La méthode isDeleted retourne une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- isDeleted, méthode Lecteur Windows Media
- isDeleted, méthode Lecteur Windows Media, interface IWMPPlaylistCollection
- Lecteur Windows Media de l’interface IWMPPlaylistCollection, méthode isDeleted
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c332a524b334933d587929cdd0e5b5fa61bc15d9110260af8af8e472d7c05fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568476"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a>IWMPPlaylistCollection :: isDeleted, méthode

La méthode **IsDeleted** retourne une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*pItem* \[ dans\]
</dt> <dd>

Interface **wmplib. IWMPPlaylist** pour la sélection interrogée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. Boolean** qui spécifie si la sélection a été supprimée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                                                     |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB et C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





