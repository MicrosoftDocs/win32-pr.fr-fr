---
title: SystemMonitor. ReportValueType, propriété
description: Récupère ou définit une valeur qui détermine si les vues de l’histogramme et du rapport graphiquent la dernière valeur échantillonnée pendant l’intervalle d’échantillonnage ou une valeur calculée de l’échantillonnage, telle que la valeur de compteur moyenne ou minimale.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Propriété ReportValueType SysMon
- Propriété ReportValueType SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété ReportValueType
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942086"
---
# <a name="systemmonitorreportvaluetype-property"></a>SystemMonitor. ReportValueType, propriété

Récupère ou définit une valeur qui détermine si les vues de l’histogramme et du rapport graphiquent la dernière valeur échantillonnée pendant l’intervalle d’échantillonnage ou une valeur calculée de l’échantillonnage, telle que la valeur de compteur moyenne ou minimale.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a>Valeur de la propriété

Détermine si l’histogramme et les vues de rapport graphiquent la dernière valeur échantillonnée pendant l’intervalle d’échantillonnage ou une valeur calculée à partir de l’intervalle d’échantillonnage. Pour connaître les valeurs possibles, consultez [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).

## <a name="remarks"></a>Notes

SYSMON ignore cette valeur et utilise [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) si [**systemmonitor. DisplayType**](systemmonitor-displaytype.md) n’est pas [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) ou **DisplayTypeConstants.sysmonReport**.

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

 

 





