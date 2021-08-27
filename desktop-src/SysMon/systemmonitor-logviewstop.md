---
title: SystemMonitor. LogViewStop, propriété
description: Récupère ou définit la date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Propriété LogViewStop SysMon
- Propriété LogViewStop SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété LogViewStop
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c30305f99e0d9bf66dd0f00dccc7674073e0f7058bca4284411c9d24426b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882073"
---
# <a name="systemmonitorlogviewstop-property"></a>SystemMonitor. LogViewStop, propriété

Récupère ou définit la date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a>Valeur de la propriété

Date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.

## <a name="remarks"></a>Remarques

SYSMON récupère les valeurs de compteur à partir des fichiers journaux qui se trouvent dans les dates [**systemmonitor. LogViewStart**](systemmonitor-logviewstart.md) et Stop, inclus.

Si vous ne spécifiez pas de valeur d’arrêt ou si vous affectez à cette propriété une valeur de date postérieure à la dernière date contenue dans le fichier journal, SYSMON remplace la valeur par la valeur de date la plus récente trouvée dans les fichiers journaux.

Si cette propriété est définie sur une valeur de date inférieure à [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON remplace la valeur par la valeur de **LogViewStart**.

Vous devez définir la date de début avant de définir la date d’arrêt. Sinon, les deux valeurs sont définies sur date. MinValue et, si vous définissez les dates après le paramètre [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md), seule la première valeur de compteur est récupérée à partir du fichier journal.

## <a name="requirements"></a>Configuration requise



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

[**SystemMonitor.LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





