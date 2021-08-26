---
description: Spécifie la dominante de champ pour une image vidéo entrelacée.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: Attribut MFSampleExtension_BottomFieldFirst (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ab0a9847977ea25d93190911bbf2280629f0219eba3d4c4ddfb492e9fdcd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113069"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a>\_Attribut MFSampleExtension BottomFieldFirst

Spécifie la dominante de champ pour une image vidéo entrelacée. Cet attribut s’applique aux exemples de supports.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarques

Si la trame vidéo est entrelacée et que l’échantillon contient deux champs entrelacés, cet attribut indique quel champ est affiché en premier. Si la **valeur est true**, le champ inférieur est tout d’abord dans le temps. Si la **valeur est false**, le champ supérieur est tout d’abord.

Si le frame est entrelacé et que l’exemple contient un champ unique, cet attribut indique le champ contenu dans l’exemple. Si la **valeur est true**, l’exemple contient le champ du bas. Si la **valeur est false**, l’exemple contient le champ supérieur.

Si le frame est progressif, cet attribut décrit comment les champs doivent être triés lorsque la sortie est entrelacée. Si la **valeur est true**, le champ du bas doit être généré en premier. Si la **valeur est false**, le champ supérieur doit être généré en premier.

Si cet attribut n’est pas défini, le type de média décrit la zone de texte dominante.

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

 

 




