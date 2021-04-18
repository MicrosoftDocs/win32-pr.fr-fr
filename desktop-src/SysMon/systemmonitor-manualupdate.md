---
title: SystemMonitor. ManualUpdate, propriété
description: Récupère ou définit une valeur indiquant si le contenu du moniteur système est mis à jour manuellement ou automatiquement à des intervalles spécifiés.
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- Propriété ManualUpdate SysMon
- Propriété ManualUpdate SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété ManualUpdate
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512388"
---
# <a name="systemmonitormanualupdate-property"></a>SystemMonitor. ManualUpdate, propriété

Récupère ou définit une valeur indiquant si le contenu du moniteur système est mis à jour manuellement ou automatiquement à des intervalles spécifiés.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

La valeur true indique que le graphique est mis à jour manuellement. False indique que le graphique est mis à jour automatiquement en fonction de l’intervalle de mise à jour spécifié dans [**systemmonitor. UpdateInterval**](systemmonitor-updateinterval.md).

## <a name="remarks"></a>Notes

Par défaut, le graphique est mis à jour automatiquement.

Pour mettre à jour le graphique manuellement, appelez la méthode [**systemmonitor. CollectSample**](systemmonitor-collectsample.md) .

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

[**SystemMonitor.CollectSample**](systemmonitor-collectsample.md)
</dt> <dt>

[**SystemMonitor.UpdateGraph**](systemmonitor-updategraph.md)
</dt> </dl>

 

 





