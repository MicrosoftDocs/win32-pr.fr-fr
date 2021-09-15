---
title: IWMPPlaylist insertItem, méthode
description: La méthode insertItem insère un élément multimédia à un emplacement spécifié dans une sélection.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- méthode insertItem Lecteur Windows Media
- insertItem, méthode Lecteur Windows Media, IWMPPlaylist, interface
- Lecteur Windows Media de l’interface IWMPPlaylist, méthode insertItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411300"
---
# <a name="iwmpplaylistinsertitem-method"></a>IWMPPlaylist :: insertItem, méthode

La méthode **InsertItem** insère un élément multimédia à un emplacement spécifié dans une sélection.

## <a name="syntax"></a>Syntaxe


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*Lindex* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index de base zéro au niveau duquel l’élément multimédia est inséré dans la sélection.

</dd> <dt>

*pIWMPMedia* \[ dans\]
</dt> <dd>

Interface **wmplib. IWMPMedia** qui représente l’élément multimédia à insérer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Tous les éléments multimédias après l’élément inséré auront leurs index augmentés d’une unité.

Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. removeItem (VB et C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





