---
title: Effet de teinte
description: Cet effet colore l’image source en multipliant l’image source par la couleur spécifiée. Il a une seule entrée.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61734e9e060da4609927c9db46eee50dab1bef1e6328f304fdfb2436529289cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384909"
---
# <a name="tint-effect"></a>Effet de teinte

Cet effet colore l’image source en multipliant l’image source par la couleur spécifiée. Il a une seule entrée.

Le CLSID de cet effet est CLSID \_ D2D1Tint.

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                    | Type et valeur par défaut                              | Description                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| Couleur de la ColorD2D1 de \_ teinte \_ \_<br/>               | D2D1 \_ Vector \_ 4F (1.0 f, 1.0 f, 1.0 f, 1.0 f)<br/> | Les couleurs de l’image source sont multipliées par cette valeur.       |
| Sortie de la bride de \_ teinte ClampOutputD2D1 \_ \_ \_<br/> | BOOLFALSE<br/>                                | Indique s’il faut ou non fixer les valeurs de sortie à la plage \[ 0, 1 \] . |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| Serveur minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |



 ## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
