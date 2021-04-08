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
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941899"
---
# <a name="systemmonitordatapointcount-property"></a>SystemMonitor. DataPointCount, propriété

Récupère ou définit le nombre de points de données affichés dans un graphique linéaire.

## <a name="syntax"></a>Syntaxe


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Valeur de la propriété

Nombre de points de données affichés dans la vue pour un graphique linéaire. La valeur par défaut est 100 points de données. La plage de valeurs valide est comprise entre 2 et 1 000.

## <a name="remarks"></a>Notes

Cette propriété est utilisée uniquement si [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est **sysmonCurrentActivity**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





