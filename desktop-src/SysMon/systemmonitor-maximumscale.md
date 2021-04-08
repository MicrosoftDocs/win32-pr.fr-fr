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
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941995"
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

[**SystemMonitor. MinimumScale**](systemmonitor-minimumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





