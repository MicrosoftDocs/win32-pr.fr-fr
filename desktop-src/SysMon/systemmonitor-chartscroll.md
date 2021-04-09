---
title: SystemMonitor. ChartScroll, propriété
description: Récupère ou définit une valeur qui détermine si le graphique linéaire défile dans la vue.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Propriété ChartScroll SysMon
- Propriété ChartScroll SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété ChartScroll
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942230"
---
# <a name="systemmonitorchartscroll-property"></a>SystemMonitor. ChartScroll, propriété

Récupère ou définit une valeur qui détermine si le graphique linéaire défile dans la vue.

## <a name="syntax"></a>Syntaxe


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

True si le graphique en courbes fait défiler en continu de droite à gauche ; Sinon, false si le graphique en courbes est dessiné de gauche à droite et s’ajuste à lui-même dans la vue. False représente la valeur par défaut.

## <a name="remarks"></a>Notes

Cette valeur est ignorée si [**systemmonitor. DisplayType**](systemmonitor-displaytype.md) n’est pas [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





