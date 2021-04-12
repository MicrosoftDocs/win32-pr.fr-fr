---
title: SystemMonitor. MinimumScale, propriété
description: Récupère ou définit la valeur minimale de l’axe vertical (Y) du graphique.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- Propriété MinimumScale SysMon
- MinimumScale, propriété SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété MinimumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465214"
---
# <a name="systemmonitorminimumscale-property"></a>SystemMonitor. MinimumScale, propriété

Récupère ou définit la valeur minimale de l’axe vertical (Y) du graphique.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a>Valeur de la propriété

Valeur minimale positive de l’axe vertical du graphique. La valeur minimale par défaut de l’échelle verticale est 0. La valeur la plus élevée que vous pouvez affecter à la valeur minimale est égale à une valeur inférieure à [**MaximumScale**](systemmonitor-maximumscale.md) .

## <a name="remarks"></a>Notes

Le contrôle ajuste automatiquement la position des nombres d’échelle affichés sur l’échelle verticale en fonction de la taille du contrôle affiché.

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

[**SystemMonitor. MaximumScale**](systemmonitor-maximumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





