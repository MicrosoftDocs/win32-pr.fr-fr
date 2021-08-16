---
description: Spécifie la complexité de l’algorithme d’encodage.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: MFPKEY_ENCCOMPLEXITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93abe02b50f862fec706f75449e00643228a3917bc22ca9dafa9285d9d46be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690124"
---
# <a name="mfpkey_enccomplexity-property"></a>MFPKEY \_ propriété ENCCOMPLEXITY

Spécifie la complexité de l’algorithme d’encodage. La valeur est un entier compris entre 0 et 100, où 0 spécifie l’algorithme le moins complexe et 100 spécifie l’algorithme le plus complexe.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ UI4**

## <a name="default-value"></a>Valeur par défaut

100 pour Windows Media Audio 10 et Windows Media Audio 10 Professional

100 pour la version Windows Vista de Windows Media Audio 10 sans perte

0 pour la version Windows 7 Windows Media Audio 10 sans perte

## <a name="remarks"></a>Remarques

Si la propriété [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) a la valeur **Variant \_ true**, l’encodeur ajuste la complexité de son algorithme en fonction de la valeur de cette propriété.

pour l’encodeur Windows Media Audio 10 et l’encodeur Windows Media Audio 10 Professional, si la valeur de cette propriété est 100, l’encodeur place une demande élevée sur le processeur et produit une sortie de qualité supérieure. À mesure que la valeur de cette propriété diminue, la demande sur le processeur diminue, mais la qualité de la sortie diminue également.

pour l’encodeur Windows Media Audio 10 sans perte, si la valeur de cette propriété est 0, l’encodeur place une faible demande sur le processeur. À mesure que la valeur de cette propriété augmente, la demande sur le processeur augmente, et la taille de la sortie de l’encodeur diminue légèrement. La sortie est sans perte, quelle que soit la valeur de cette propriété.

Si vous laissez cette propriété à sa valeur par défaut **Variant \_ false**, l’encodeur utilise son algorithme par défaut. l’algorithme par défaut dépend de l’encodeur que vous utilisez et de la version de Windows qui est en cours d’exécution. Le tableau suivant décrit le comportement par défaut pour les différentes combinaisons.



| Système d’exploitation | Comportement par défaut                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | les Windows Media Audio 10, Windows Media Audio 10 Professional et Windows Media Audio 10 encodeurs sans perte utilisent tous l’algorithme le plus complexe par défaut.                                                    |
| Windows 7        | les encodeurs Windows Media Audio 10 et Windows Media Audio 10 Professional utilisent l’algorithme le plus complexe par défaut. l’encodeur Windows Media Audio 10 Lossless utilise l’algorithme le moins complexe par défaut. |



 

Si la propriété [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) a la valeur **Variant \_ false**, l’encodeur ignore cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
