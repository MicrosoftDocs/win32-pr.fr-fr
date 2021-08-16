---
title: Méthode d’élément IWMPPlaylistArray
description: La méthode Item retourne une interface IWMPPlaylist représentant la sélection à l’index spécifié.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- méthode Item Lecteur Windows Media
- méthode Item Lecteur Windows Media, interface IWMPPlaylistArray
- Lecteur Windows Media de l’interface IWMPPlaylistArray, méthode Item
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e73614e1ef00f29d6b09d3d49e2c7e514bae807245f00f30f4d3382d8f1a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331158"
---
# <a name="iwmpplaylistarrayitem-method"></a>IWMPPlaylistArray :: Item, méthode

La méthode **Item** retourne une interface **IWMPPlaylist** représentant la sélection à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*Lindex* \[ dans\]
</dt> <dd>

**System. Int32** contenant l’index qui identifie la sélection que la méthode doit récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface **wmplib. IWMPPlaylist** pour la sélection récupérée.

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

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

[**Interface IWMPPlaylistArray (VB et C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





