---
title: SystemMonitor. ShowValueBar, propriété
description: Récupère ou définit une valeur qui détermine si la barre de valeur (l’ensemble de valeurs statistiques sous le graphique) est affichée sur le contrôle.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Propriété ShowValueBar SysMon
- Propriété ShowValueBar SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété ShowValueBar
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740621"
---
# <a name="systemmonitorshowvaluebar-property"></a>SystemMonitor. ShowValueBar, propriété

Récupère ou définit une valeur qui détermine si la barre de valeur (l’ensemble de valeurs statistiques sous le graphique) est affichée sur le contrôle.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

True indique que la barre de valeurs est affichée sur le contrôle ; Sinon, false. La valeur par défaut de cette propriété est True.

## <a name="remarks"></a>Notes

Les statistiques affichées incluent la dernière valeur, la valeur moyenne et les valeurs minimale et maximale du compteur actuellement sélectionné sur l’intervalle de temps affiché. Pour sélectionner les valeurs de compteur à afficher, l’utilisateur doit sélectionner le compteur dans le volet légende du contrôle.

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

 

 





