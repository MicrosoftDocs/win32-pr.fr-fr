---
title: IWMPCdromBurn propriété burnProgress
description: La propriété burnProgress obtient la progression de la gravure de CD comme pourcentage d’achèvement.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- Lecteur Windows Media de la propriété burnProgress
- Lecteur Windows Media de la propriété burnProgress, interface IWMPCdromBurn
- Lecteur Windows Media de l’interface IWMPCdromBurn, propriété burnProgress
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519885"
---
# <a name="iwmpcdromburnburnprogress-property"></a>IWMPCdromBurn :: burnProgress, propriété

La propriété **burnProgress** obtient la progression de la gravure de CD comme pourcentage d’achèvement.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est la valeur de progression. Les valeurs de progression sont comprises entre 0 et 100.

## <a name="remarks"></a>Notes

La valeur de progression représente le pourcentage terminé de l’ensemble du processus de gravure, y compris les opérations intermédiaires.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11<br/>                                                                                     |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





