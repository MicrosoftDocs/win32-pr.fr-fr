---
description: Spécifie la logique qui sera utilisée par le codec pour détecter la vidéo source entrelacée.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: MFPKEY_VTYPE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863441"
---
# <a name="mfpkey_vtype-property"></a>MFPKEY \_ propriété VTYPE

Spécifie la logique qui sera utilisée par le codec pour détecter la vidéo source entrelacée.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCVType g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

Cette propriété peut être définie sur l’une des valeurs suivantes.



| Valeur | Description                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Le codec utilise la logique standard de détection de type de trame.                                                                                 |
| 1     | Le codec traitera toutes les trames vidéo source en tant que trames entrelacées.                                                                          |
| 2     | Le codec traitera toutes les trames vidéo sources comme des champs de vidéo entrelacée.                                                                 |
| 3     | Le codec déterminera automatiquement si les images vidéo d’entrée sont des images entrelacées ou des champs de vidéo entrelacée.                      |
| 4     | Le codec déterminera automatiquement si les images vidéo d’entrée sont des images progressives, des images entrelacées ou des champs de vidéo entrelacée. |



 

Cette propriété détermine la méthode d’encodage d’image utilisée pour l’encodage vidéo progressif ou entrelacé.

Si aucun type de vidéo n’est spécifié, le codec utilise l’encodage de trame progressif pour les sessions de codage progressive et l’encodage entrelacé de champ pour les sessions d’encodage entrelacées. Le type de session d’encodage vidéo (progressif ou entrelacé) est défini à l’aide de la propriété [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) .

> [!Note]  
> La propriété [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) doit avoir la valeur variant \_ true pour produire une sortie entrelacée ; sinon, la définition de la propriété MPFKEY VTYPE n’aura \_ aucun effet.

 

Quand la vidéo entrelacée est encodée, il est possible de spécifier plusieurs méthodes d’encodage d’image. En général, la méthode la plus efficace pour encoder une vidéo entrelacée consiste à utiliser la méthode entrelacée de champ (2). Si la vidéo source contient très peu de mouvement, la méthode entrelacée de cadre (1) ou la méthode de trame/champ automatique (2) peut être plus appropriée.

Lors de l’encodage de contenu mixte (contenant à la fois des frames progressifs et entrelacés), il est préférable d’utiliser la valeur de la trame automatique/de champ/progressive (4).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




