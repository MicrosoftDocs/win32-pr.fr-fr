---
description: Spécifie s’il faut répéter le premier champ dans un frame entrelacé. Cet attribut s’applique aux exemples de supports.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: Attribut MFSampleExtension_RepeatFirstField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114403"
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

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
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

 

 




