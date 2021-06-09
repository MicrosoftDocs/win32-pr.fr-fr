---
description: Active le mode faible latence dans un codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826903"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

