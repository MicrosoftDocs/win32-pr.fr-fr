---
title: SystemMonitor. Counters, propriété
description: Récupère les compteurs qui contiennent une collection d’objets CounterItem.
ms.assetid: eab21e1f-c8fb-474c-83e3-5ef56483d525
keywords:
- Propriétés des compteurs SysMon
- Compteurs propriété SysMon, SystemMonitor, classe
- Classe SystemMonitor SysMon, propriété Counters
topic_type:
- apiref
api_name:
- SystemMonitor.Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e09cc797c09033e90ba4d584ee63336a52cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103990"
---
# <a name="systemmonitorcounters-property"></a>SystemMonitor. Counters, propriété

Récupère les **compteurs** qui contiennent une collection d’objets [**CounterItem**](counteritem.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property Counters As ICounters
```



## <a name="property-value"></a>Valeur de la propriété

Objet de **compteurs** qui contient une collection d’objets [**CounterItem**](counteritem.md) .

## <a name="remarks"></a>Notes

Il s’agit de la propriété par défaut de l’objet [**systemmonitor**](systemmonitor.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





