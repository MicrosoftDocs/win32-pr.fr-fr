---
title: CounterItem. Selected, propriété
description: Récupère ou définit une valeur qui indique si le compteur est sélectionné.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Propriété sélectionnée SysMon
- Propriété sélectionnée SysMon, objet CounterItem
- CounterItem objet SysMon, propriété sélectionnée
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942231"
---
# <a name="counteritemselected-property"></a>CounterItem. Selected, propriété

Récupère ou définit une valeur qui indique si le compteur est sélectionné.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

True si le compteur est sélectionné ; Sinon, false.

## <a name="remarks"></a>Notes

Vous pouvez sélectionner un ou plusieurs compteurs dans la collection de compteurs. En sélectionnant un compteur, sélectionne le compteur dans la légende, rend le compteur visible dans la légende et génère un événement [**OnCounterSelected**](-systemmonitor-oncounterselected.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





