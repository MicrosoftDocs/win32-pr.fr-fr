---
title: SystemMonitor. ShowTimeAxisLabels, propriété
description: Récupère ou définit une valeur qui détermine si l’axe horizontal (X) de la vue du graphique contient des étiquettes.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Propriété ShowTimeAxisLabels SysMon
- Propriété ShowTimeAxisLabels SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété ShowTimeAxisLabels
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538808"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a>SystemMonitor. ShowTimeAxisLabels, propriété

Récupère ou définit une valeur qui détermine si l’axe horizontal (X) de la vue du graphique contient des étiquettes.

## <a name="syntax"></a>Syntaxe


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

La valeur true applique des étiquettes à l’axe des x. La valeur false ne l’est pas. La valeur par défaut est False.

## <a name="remarks"></a>Notes

SYSMON ignore cette propriété pour les graphiques à barres, les rapports et les histogrammes.

Pour les graphiques linéaires, SYSMON utilise l’heure à laquelle la valeur de compteur a été échantillonnée comme étiquette.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





