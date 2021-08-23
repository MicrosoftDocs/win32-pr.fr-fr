---
description: Active le mode faible latence dans un codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1466f7874fe743dbc865df251f077440885103853e3784af19624c4733a1e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606269"
---
# <a name="codecapi_avlowlatencymode-property"></a>CODECAPI \_ propriété AVLowLatencyMode

Active le mode faible latence dans un codec.

## <a name="data-type"></a>Type de données

**ULong** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVLowLatencyMode**

## <a name="property-value"></a>Valeur de la propriété

Si la valeur est différente de zéro, le mode faible latence est activé. Si la valeur est égale à zéro, le mode de latence faible est désactivé.

## <a name="remarks"></a>Remarques

Cette propriété s’applique aux encodeurs et aux décodeurs.

Le mode de faible latence est utile pour les communications en temps réel ou la capture en direct, lorsque la latence doit être réduite. Toutefois, le mode à faible latence peut également réduire la qualité du décodage ou du codage.

L’encodeur est supposé ne pas ajouter de délai d’échantillonnage en raison de la réorganisation des frames dans le processus d’encodage, et un exemple d’entrée produira un échantillon de sortie. Les secteurs/frames B peuvent être présents tant qu’ils n’introduisent pas de réordonnancement de frame dans l’encodeur.

> [!WARNING] 
> Dans l’implémentation actuelle, le Media Foundation décodeur H. 264 utilise le type **VT_UI4** pour cette propriété. Toutes les autres implémentations, y compris l’encodeur H. 264, utilisent le type **VT_BOOL**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

