---
title: Propriété Count IWMPPlaylist
description: La propriété Count obtient le nombre d’éléments multimédias dans une sélection.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- propriété Count Windows Media Player
- propriété Count lecteur Windows Media, interface IWMPPlaylist
- IWMPPlaylist interface Windows Media Player, propriété Count
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d988fefc436b65652d2b0765320ca289417c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541355"
---
# <a name="iwmpplaylistcount-property"></a>IWMPPlaylist :: Count, propriété

La propriété **Count** obtient le nombre d’éléments multimédias dans une sélection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond au nombre d’éléments multimédias dans la sélection.

## <a name="remarks"></a>Notes

Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Consultez la propriété [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) pour obtenir un exemple de code qui utilise cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





