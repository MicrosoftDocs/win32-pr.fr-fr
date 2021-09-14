---
title: CounterItem. ScaleFactor, propriété
description: Récupère ou définit le facteur d’échelle utilisé pour représenter sous forme de graphique la valeur de compteur.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Propriété ScaleFactor SysMon
- Propriété ScaleFactor SysMon, classe CounterItem
- CounterItem classe SysMon, propriété ScaleFactor
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008880"
---
# <a name="counteritemscalefactor-property"></a>CounterItem. ScaleFactor, propriété

Récupère ou définit le facteur d’échelle utilisé pour représenter sous forme de graphique la valeur de compteur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a>Valeur de la propriété

Facteur d’échelle utilisé pour afficher les valeurs de compteur sous forme de graphique. Les valeurs valides sont comprises entre-9 et 9 (les valeurs correspondent à 0,000000001-100000000,0).

**avant Windows Vista :** Les valeurs valides sont comprises entre-7 et 7 (les valeurs correspondent à 0,0000001-1000000,0).

## <a name="remarks"></a>Notes

Définissez cette propriété uniquement si vous souhaitez modifier le facteur d’échelle par défaut du compteur (chaque compteur définit son propre facteur d’échelle). La valeur de cette propriété est définie sur Integer. MaxValue si le compteur utilise son facteur d’échelle par défaut pour représenter les valeurs dans un graphique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**SystemMonitor.ScaleToFit**](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





