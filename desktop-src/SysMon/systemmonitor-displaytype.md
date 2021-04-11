---
title: SystemMonitor. DisplayType, propriété
description: Récupère ou définit le type de graphique utilisé pour représenter graphiquement les données du compteur de performance.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- Propriété DisplayType SysMon
- Propriété DisplayType SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété DisplayType
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103834"
---
# <a name="systemmonitordisplaytype-property"></a>SystemMonitor. DisplayType, propriété

Récupère ou définit le type de graphique utilisé pour représenter graphiquement les données du compteur de performance.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a>Valeur de la propriété

Type de graphique utilisé pour représenter graphiquement les données du compteur de performance. Pour connaître les valeurs possibles, consultez [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="exceptions"></a>Exceptions



| Type d'exception               | Condition                                         |
|------------------------------|---------------------------------------------------|
| **System.ArgumentException** | Le graphique ou la valeur de rapport spécifié n’est pas valide. |



 

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

 

 





