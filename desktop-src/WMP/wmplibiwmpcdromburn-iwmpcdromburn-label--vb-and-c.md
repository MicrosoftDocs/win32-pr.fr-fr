---
title: Propriété d’étiquette IWMPCdromBurn
description: La propriété étiquette obtient la chaîne de nom du volume du CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- propriété d’étiquette lecteur Windows Media
- propriété étiquette lecteur Windows Media, interface IWMPCdromBurn
- Interface IWMPCdromBurn lecteur Windows Media, propriété label
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542633"
---
# <a name="iwmpcdromburnlabel-property"></a>IWMPCdromBurn :: label, propriété

La propriété *étiquette* obtient la chaîne de nom du volume du CD.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est la chaîne de nom de volume.

## <a name="remarks"></a>Notes

En raison de la façon dont les étiquettes de CD sont stockées, l’étiquette du CD peut être plus petite que la longueur de la chaîne de nom de volume spécifiée. Si la chaîne dépasse la longueur maximale d’une étiquette de CD, le texte est tronqué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





