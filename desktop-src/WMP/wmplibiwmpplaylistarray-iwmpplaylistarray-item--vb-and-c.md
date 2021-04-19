---
title: Méthode d’élément IWMPPlaylistArray
description: La méthode Item retourne une interface IWMPPlaylist représentant la sélection à l’index spécifié.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Méthode Item lecteur Windows Media
- Méthode Item lecteur Windows Media, interface IWMPPlaylistArray
- Interface IWMPPlaylistArray lecteur Windows Media, méthode d’élément
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
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539945"
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

## <a name="remarks"></a>Notes

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

 

 





