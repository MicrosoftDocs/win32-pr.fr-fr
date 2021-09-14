---
title: SystemMonitor. EnableToolTips, propriété
description: Récupère ou définit une valeur qui détermine si une info-bulle est affichée lorsque la souris pointe sur un compteur dans l’une des vues de graphique (non prise en charge pour la vue rapport).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- Propriété EnableToolTips SysMon
- Propriété EnableToolTips SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété EnableToolTips
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324727"
---
# <a name="systemmonitorenabletooltips-property"></a>SystemMonitor. EnableToolTips, propriété

Récupère ou définit une valeur qui détermine si une info-bulle est affichée lorsque la souris pointe sur un compteur dans l’une des vues de graphique (non prise en charge pour la vue rapport).

## <a name="syntax"></a>Syntaxe


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

True affiche une info-bulle avec les informations de compteur. Sinon, false.

## <a name="remarks"></a>Notes

Pour les graphiques linéaires, l’info-bulle est ancrée au point de données le plus proche de la souris. Pour les graphiques à barres et les histogrammes, l’info-bulle représente la valeur totale des données de la barre, et non un point dans la barre.

L’info-bulle contient différentes informations basées sur la source de données. Pour les fichiers journaux, l’info-bulle contient le chemin de compteur, la valeur de compteur, l’horodatage, le nombre d’échantillons de données inclus dans le point de données, ainsi que les valeurs de données minimale et maximale.

Pour une activité en temps réel, l’info-bulle contient le chemin de compteur, la valeur de compteur et l’horodatage.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





