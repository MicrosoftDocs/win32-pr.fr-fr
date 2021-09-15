---
title: Propriété d’étiquette IWMPCdromBurn
description: La propriété étiquette obtient la chaîne de nom du volume du CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- propriété étiquette Lecteur Windows Media
- label, propriété Lecteur Windows Media, IWMPCdromBurn, interface
- Lecteur Windows Media de l’interface IWMPCdromBurn, propriété label
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519861"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





