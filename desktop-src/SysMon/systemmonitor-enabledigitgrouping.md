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
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384716"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>SystemMonitor. EnableDigitGrouping, propriété

Récupère ou définit une valeur qui détermine si SYSMON utilise le regroupement de chiffres lors de l’affichage de valeurs numériques.

## <a name="syntax"></a>Syntaxe


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est true, SYSMON groupe les chiffres lors de l’affichage des valeurs numériques, par exemple 1 214. Si la valeur est false, les valeurs numériques ne sont pas regroupées, par exemple, 1214. La valeur par défaut est true.

## <a name="remarks"></a>Notes

Le symbole de regroupement digits est localisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





