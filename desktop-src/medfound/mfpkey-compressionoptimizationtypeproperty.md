---
description: spécifie les paramètres de qualité visuelle optimaux à utiliser pour l’encodeur de profil avancé Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e140a854999a5c634620d98958e40832acbe9439
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471725"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>MFPKEY \_ propriété COMPRESSIONOPTIMIZATIONTYPE

spécifie les paramètres de qualité visuelle optimaux à utiliser pour l’encodeur de profil avancé Windows Media Video 9.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCCompressionOptimizationType g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Remarques

Cette propriété offre un moyen rapide de configurer un certain nombre d’options d’encodage vidéo. Il peut être défini sur l’une des valeurs suivantes.




| Valeur | Description | 
|-------|-------------|
| 0 | Le codec ne force pas l’optimisation et utilise toutes les fonctionnalités spécifiées par d’autres propriétés. Dans de nombreux cas, le codec utilise la logique interne pour déterminer les paramètres s’ils ne sont pas spécifiés. Il s’agit de la valeur par défaut. | 
| 1 | Active les fonctionnalités qui produiront la meilleure qualité visuelle. L’utilisation de cette valeur configure le codec comme si vous aviez défini les propriétés suivantes :<br /><ul><li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li><li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li><li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li><li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</li><li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li><li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</li><li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li></ul>Si vous définissez l’une des propriétés de la liste précédente, la valeur que vous définissez remplace les valeurs associées à ce paramètre, à l’exception de <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br /> | 




 

Si vous affectez la valeur \_ 1 à la propriété MFPKEY COMPRESSIONOPTIMIZATIONTYPE, cela a également pour effet de définir le paramètre de Registre option DQuant sur 2 et le paramètre de Registre méthode de coût du vecteur de mouvement sur 1. pour plus d’informations, consultez l’article web [à l’aide de l’Paramètres avancé du Codec de profil avancé Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




