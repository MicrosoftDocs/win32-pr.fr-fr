---
title: SystemMonitor. UpdateInterval, propriété
description: Récupère ou définit la durée d’attente de l’exécution de SYSMON avant la prochaine collecte des données de compteur et met à jour le graphique ou le rapport.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Propriété UpdateInterval SysMon
- Propriété UpdateInterval SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété UpdateInterval
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193655"
---
# <a name="systemmonitorupdateinterval-property"></a>SystemMonitor. UpdateInterval, propriété

Récupère ou définit la durée d’attente de l’exécution de SYSMON avant la prochaine collecte des données de compteur et met à jour le graphique ou le rapport.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a>Valeur de la propriété

Durée, en secondes, pendant laquelle SYSMON attend la prochaine fois qu’il collecte des données de compteur et met à jour le graphique ou le rapport. L’intervalle minimal est de 1 seconde (il s’agit également de la valeur par défaut). La valeur maximale est 1 million.

## <a name="remarks"></a>Notes

Cette propriété s’applique uniquement lorsque [**systemmonitor. ManualUpdate**](systemmonitor-manualupdate.md) est défini sur false.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





