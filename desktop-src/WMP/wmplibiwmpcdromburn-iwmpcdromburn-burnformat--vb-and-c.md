---
title: IWMPCdromBurn propriété burnFormat
description: La propriété burnFormat obtient une valeur qui indique le type de CD à graver.
ms.assetid: f60fcbd2-5d34-46f3-a2e2-29dac2ecf689
keywords:
- propriété burnFormat lecteur Windows Media
- propriété burnFormat lecteur Windows Media, interface IWMPCdromBurn
- Interface IWMPCdromBurn lecteur Windows Media, propriété burnFormat
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnFormat
- IWMPCdromBurn.get_burnFormat
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17e379727376b1ce272a95cd77c688fa611b291a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526549"
---
# <a name="iwmpcdromburnburnformat-property"></a>IWMPCdromBurn :: burnFormat, propriété

La propriété **burnFormat** obtient une valeur qui indique le type de CD à graver.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public WMPBurnFormat burnFormat {get;}
```


```VB

Public ReadOnly Property burnFormat As WMPBurnFormat
```





## <a name="property-value"></a>Valeur de la propriété

**Wmplib. WMPBurnFormat** qui est une valeur de l’énumération **WMPBurnFormat** qui indique le type de CD à graver.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11<br/>                                                                             |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                          |
| Assembly<br/>  | <dl> <dt>Interop. WMPLib (Interop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPBurnFormat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
</dt> </dl>

 

 





