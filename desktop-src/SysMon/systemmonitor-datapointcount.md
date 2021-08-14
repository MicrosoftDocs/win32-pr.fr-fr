---
title: SystemMonitor. DataPointCount, propriété
description: Récupère ou définit le nombre de points de données affichés dans un graphique linéaire.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Propriété DataPointCount SysMon
- Propriété DataPointCount SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété DataPointCount
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d7d1212f3f1467c0fb505e84dffdd9cc6bb381c19d8ccc34ad38ee46562ec6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882624"
---
# <a name="systemmonitordatapointcount-property"></a>SystemMonitor. DataPointCount, propriété

Récupère ou définit le nombre de points de données affichés dans un graphique linéaire.

## <a name="syntax"></a>Syntaxe


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Valeur de la propriété

Nombre de points de données affichés dans la vue pour un graphique linéaire. La valeur par défaut est 100 points de données. La plage de valeurs valide est comprise entre 2 et 1 000.

## <a name="remarks"></a>Remarques

Cette propriété est utilisée uniquement si [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est **sysmonCurrentActivity**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





