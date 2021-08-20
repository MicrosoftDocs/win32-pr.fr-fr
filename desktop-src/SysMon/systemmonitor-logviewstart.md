---
title: SystemMonitor. LogViewStart, propriété
description: Récupère ou définit la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Propriété LogViewStart SysMon
- Propriété LogViewStart SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété LogViewStart
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc1c7c4a46ac746582d62ee7ce08980b078eb8d972cb6b4d3ed787b49f2285f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955402"
---
# <a name="systemmonitorlogviewstart-property"></a>SystemMonitor. LogViewStart, propriété

Récupère ou définit la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a>Valeur de la propriété

Date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.

## <a name="remarks"></a>Remarques

SYSMON récupère les valeurs de compteur à partir des fichiers journaux qui se trouvent dans les dates Start et [**systemmonitor. LogViewStop**](systemmonitor-logviewstop.md) , inclus.

Si vous ne spécifiez pas de date de début ou si vous définissez cette propriété sur une valeur de date qui se trouve en dehors de la plage de valeurs de date trouvée dans les fichiers journaux, SYSMON remplace la valeur par la valeur de date la plus ancienne trouvée dans les fichiers journaux.

Si cette propriété est définie sur une valeur de date supérieure à [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON remplace la valeur par la valeur de **LogViewStop**.

Si vous spécifiez une date de début et de fin, vous devez spécifier les dates avant de définir [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> <dt>

[**SystemMonitor. LogFiles**](systemmonitor-logfiles.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





