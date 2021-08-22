---
title: SystemMonitor. EnableDigitGrouping, propriété
description: Récupère ou définit une valeur qui détermine si SYSMON utilise le regroupement de chiffres lors de l’affichage de valeurs numériques.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Propriété EnableDigitGrouping SysMon
- Propriété EnableDigitGrouping SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété EnableDigitGrouping
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d910e479cc0a957ea5f1332d7fead0f93badd797bfe2d90b26f9914f0c3d863a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882604"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>SystemMonitor. EnableDigitGrouping, propriété

Récupère ou définit une valeur qui détermine si SYSMON utilise le regroupement de chiffres lors de l’affichage de valeurs numériques.

## <a name="syntax"></a>Syntaxe


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est true, SYSMON groupe les chiffres lors de l’affichage des valeurs numériques, par exemple 1 214. Si la valeur est false, les valeurs numériques ne sont pas regroupées, par exemple, 1214. La valeur par défaut est true.

## <a name="remarks"></a>Remarques

Le symbole de regroupement digits est localisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





