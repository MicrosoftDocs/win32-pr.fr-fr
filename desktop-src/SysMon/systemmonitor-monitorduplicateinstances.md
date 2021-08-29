---
title: SystemMonitor. MonitorDuplicateInstances, propriété
description: Récupère ou définit une valeur qui détermine si plusieurs instances d’un compteur peuvent être surveillées.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Propriété MonitorDuplicateInstances SysMon
- Propriété MonitorDuplicateInstances SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété MonitorDuplicateInstances
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da6f8e9f85dcc865bb9a0733b7a1160582772754b5a2cabd1aa7b80452e6f42c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881781"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a>SystemMonitor. MonitorDuplicateInstances, propriété

Récupère ou définit une valeur qui détermine si plusieurs instances d’un compteur peuvent être surveillées.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

True indique que plusieurs instances d’un compteur peuvent être surveillées (true est la valeur par défaut). La valeur false indique qu’une seule instance d’un compteur peut être surveillée.

## <a name="remarks"></a>Remarques

Le moniteur système ajoute \# n à chaque nom d’instance, sauf le premier, si plusieurs instances existent. Le numéro de série, n, commence par un et est incrémenté d’une unité pour chaque nouvelle instance. Par exemple, si vous spécifiez « \\ Process ( \* ) \\ % Processor Time », la collection de compteurs doit contenir plusieurs instances de svchost. La première occurrence est svchost, l’occurrence suivante est svchost \# 1, et ainsi de suite.

Les instances dupliquées sont analysées uniquement si vous utilisez le caractère générique ( \* ) pour le nom de l’instance. Si vous avez spécifié « \\ Process (svchost) \\ % Processor Time », seule la première instance de svchost est surveillée, pas toutes les instances de svchost.

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

 

 





