---
description: Spécifie si le codec doit utiliser l’optimisation de perception conservatrice lors de l’encodage.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: MFPKEY_PERCEPTUALOPTLEVEL, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202342"
---
# <a name="mfpkey_perceptualoptlevel-property"></a>MFPKEY \_ propriété PERCEPTUALOPTLEVEL

Spécifie si le codec doit utiliser l’optimisation de perception conservatrice lors de l’encodage.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCPerceptualOptLevel g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

L’optimisation de perception conservatrice est un processus par lequel le codec tente d’identifier les régions « importantes » et « sans importance » dans la trame vidéo. Après avoir identifié ces régions du cadre, le codec offre une priorité plus élevée à la qualité des régions importantes, au détriment de la qualité des régions inimportants.

L’optimisation de la perception insiste sur le fait que l’image semble correcte à l’oeil humain au lieu d’insister sur une précision mathématique stricte.

Les résultats de l’optimisation varient considérablement en fonction du type de vidéo encodé. Cette fonctionnalité peut être parfaitement adaptée aux encodages à faible débit et à faible résolution (par exemple, la diffusion Web), mais elle doit probablement être évitée pour la qualité vidéo d’archivage.

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

 

 




