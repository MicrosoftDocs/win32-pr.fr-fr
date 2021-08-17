---
title: SystemMonitor. MaximumScale, propriété
description: Récupère ou définit la valeur maximale de l’axe vertical (Y) du graphique.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- Propriété MaximumScale SysMon
- Propriété MaximumScale SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété MaximumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 176ebab3b2879b3d158310ec61fa9e65df45f8b502029ede1c58c2c1dd33f225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882028"
---
# <a name="systemmonitormaximumscale-property"></a>SystemMonitor. MaximumScale, propriété

Récupère ou définit la valeur maximale de l’axe vertical (Y) du graphique.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a>Valeur de la propriété

Valeur maximale positive de l’axe vertical du graphique. La valeur maximale par défaut de l’échelle verticale est 100. La valeur la plus basse que vous pouvez affecter à la valeur maximale est supérieure d’une unité à la valeur [**MinimumScale**](systemmonitor-minimumscale.md) . La valeur la plus élevée que vous pouvez affecter à la valeur maximale est 999 999 999.

## <a name="remarks"></a>Remarques

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

[**SystemMonitor. MinimumScale**](systemmonitor-minimumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





