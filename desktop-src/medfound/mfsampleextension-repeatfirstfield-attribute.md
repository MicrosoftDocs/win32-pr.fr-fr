---
description: Spécifie s’il faut répéter le premier champ dans un frame entrelacé. Cet attribut s’applique aux exemples de supports.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: Attribut MFSampleExtension_RepeatFirstField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0668e37e6a6958615c83f98c4b6b87eb170b115cf0549f3944a43b21c5b65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872419"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a>\_Attribut MFSampleExtension RepeatFirstField

Spécifie s’il faut répéter le premier champ dans un frame entrelacé. Cet attribut s’applique aux exemples de supports.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarques

Si la valeur est **false** ou si l’attribut n’est pas défini, le premier champ n’est pas répété. Si la valeur est **true**, le premier champ est répété. La valeur **true** est valide uniquement lorsque les conditions suivantes sont vraies :

-   Le type de média est mélangé entrelacé et progressif. (L’attribut d’attribut [**\_ \_ \_ mode entrelacé MF MT**](mf-mt-interlace-mode-attribute.md) sur le type de média est **MFVideoInterlace \_ MixedInterlaceOrProgressive**.)
-   Le frame est progressif et l’attribut [**\_ entrelacé MFSampleExtension**](mfsampleextension-interlaced-attribute.md) sur l’exemple est **true**.
-   L’attribut [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) est défini sur l’exemple. La valeur peut être **true** ou **false**. L’ordre des champs est déterminé par cet attribut.

Cet attribut est utilisé pour la conversion 3:2. Le tableau suivant indique l’ordre dans lequel les champs sont affichés.



| MFSampleExtension \_ RepeatFirstField | MFSampleExtension \_ BottomFieldFirst | Ordre des champs         |
|-------------------------------------|-------------------------------------|---------------------|
| **TRUE**                            | **TRUE**                            | Inférieur, supérieur, inférieur |
| **TRUE**                            | **FALSE**                           | Haut, bas, haut |
| **FALSE**                           | **TRUE**                            | Inférieur, supérieur        |
| **FALSE**                           | **FALSE**                           | Supérieur, inférieur        |



 

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> <dt>

[Entrelacement de vidéos](video-interlacing.md)
</dt> </dl>

 

 




