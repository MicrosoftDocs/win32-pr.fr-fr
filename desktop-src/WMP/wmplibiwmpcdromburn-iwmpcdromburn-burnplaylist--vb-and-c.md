---
title: IWMPCdromBurn propriété burnPlaylist
description: La propriété burnPlaylist obtient la sélection actuelle à graver sur le CD.
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- Lecteur Windows Media de la propriété burnPlaylist
- Lecteur Windows Media de la propriété burnPlaylist, interface IWMPCdromBurn
- Lecteur Windows Media de l’interface IWMPCdromBurn, propriété burnPlaylist
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
ms.openlocfilehash: 186996632a5b25c89019f9bbb692d9804ae33130650d4b0a29c0cb51e30d0792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116592"
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

 

 





