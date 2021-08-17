---
title: CounterItem. Color, propriété
description: Récupère ou définit la couleur utilisée pour représenter sous forme de graphique la valeur de compteur.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Propriété de couleur SysMon
- Propriété Color SysMon, classe CounterItem
- Classe CounterItem SysMon, propriété Color
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcc51862c57312f9b923ea6a80f9814182bbc6aef707dab994b135ace9637754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883866"
---
# <a name="counteritemcolor-property"></a>CounterItem. Color, propriété

Récupère ou définit la couleur utilisée pour représenter sous forme de graphique la valeur de compteur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a>Valeur de la propriété

Couleur utilisée pour représenter sous forme graphique la valeur du compteur.

## <a name="remarks"></a>Remarques

Si vous ne spécifiez pas la couleur à utiliser, SYSMON sélectionne les couleurs des seize premiers compteurs. Si vous spécifiez plus de seize compteurs, SYSMON utilise les mêmes couleurs des seize premiers compteurs. Pour vous aider à distinguer les compteurs les uns des autres, SYSMON change le [**style de ligne**](counteritem-linestyle.md) utilisé pour chaque multiple de seize compteurs jusqu’aux 80 premiers compteurs. Par exemple, les seize premiers compteurs utilisent un style de ligne plein, les seize suivants utilisent un style de ligne de tirets, et ainsi de suite. SYSMON définit ensuite la [**largeur de ligne**](counteritem-width.md) sur 2 pour les compteurs 81-96 et sur 3 pour les compteurs 96-112. Si la collection contient plus de 112 compteurs, les compteurs contiendront des valeurs de couleur, de style de ligne et de largeur en double.

**avant Windows Vista :** Si vous ne spécifiez pas la couleur à utiliser, SYSMON sélectionne les couleurs des seize premiers compteurs. Si vous spécifiez plus de seize compteurs, SYSMON utilise les mêmes couleurs des seize premiers compteurs. Pour mieux distinguer les compteurs les uns des autres, SYSMON augmente la [**largeur de ligne**](counteritem-width.md) des trois premiers compteurs qui reçoivent la même affectation de couleur. Si plus de trois compteurs utilisent la même couleur, SYSMON choisit de façon aléatoire la largeur de ligne à utiliser pour le compteur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





