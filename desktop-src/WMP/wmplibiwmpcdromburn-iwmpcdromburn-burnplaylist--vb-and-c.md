---
title: IWMPCdromBurn propriété burnPlaylist
description: La propriété burnPlaylist obtient la sélection actuelle à graver sur le CD.
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- propriété burnPlaylist lecteur Windows Media
- propriété burnPlaylist lecteur Windows Media, interface IWMPCdromBurn
- Interface IWMPCdromBurn lecteur Windows Media, propriété burnPlaylist
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnPlaylist
- IWMPCdromBurn.get_burnPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae095696b9c106926fb7f363430574b2eb87cea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526746"
---
# <a name="iwmpcdromburnburnplaylist-property"></a>IWMPCdromBurn :: burnPlaylist, propriété

La propriété **burnPlaylist** obtient la sélection actuelle à graver sur le CD.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist burnPlaylist {get;}
```


```VB

Public ReadOnly Property burnPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valeur de la propriété

Interface **wmplib. IWMPPlaylist** de la sélection à graver.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11<br/>                                                                                     |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





