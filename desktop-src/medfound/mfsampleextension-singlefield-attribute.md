---
description: Spécifie si un exemple de vidéo contient un champ unique ou deux champs entrelacés. Cet attribut s’applique aux exemples de supports.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: Attribut MFSampleExtension_SingleField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747dbeebb9bcc8e773b59467f460b12645ed50ebfbddf5bbf6845119c2bba81d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462899"
---
# <a name="mfsampleextension_singlefield-attribute"></a>\_Attribut MFSampleExtension SingleField

Spécifie si un exemple de vidéo contient un champ unique ou deux champs entrelacés. Cet attribut s’applique aux exemples de supports.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarques

Si la valeur est **true**, l’exemple contient un champ. Si la valeur est **false** ou si l’attribut n’est pas défini, l’exemple contient une image complète. (Deux champs si entrelacé ou une image progressive.)

Si le type de média est une trame progressive ou des champs entrelacés, cet attribut doit avoir la **valeur false** ou n’est pas défini.

Si le type de média est un champ unique, cet attribut doit avoir la **valeur true**. Définissez l’attribut [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) sur l’exemple pour indiquer s’il s’agit du champ supérieur ou du champ inférieur.

Actuellement, le convertisseur vidéo amélioré (EVR) ne prend pas en charge le contenu qui bascule entre les trames entrelacées et les champs uniques.

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

 

 




