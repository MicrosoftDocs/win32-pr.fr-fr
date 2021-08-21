---
description: Spécifie le type MIME du contenu.
ms.assetid: bbcfb3e6-a86a-4621-b8d9-92ace60e8c10
title: Attribut MF_PD_MIME_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb68e9b45d51b9fe4732957ef60a4496ca57df5be0185f46a7e28204217b4ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059639"
---
# <a name="mf_pd_mime_type-attribute"></a>\_Attribut de \_ type MIME MF PD \_

Spécifie le type MIME du contenu.

## <a name="data-type"></a>Type de données

Chaîne de caractères larges

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation.

Le type MIME exposé via [System. MIMEType](../properties/props-system-mimetype.md) pour les fichiers multimédias peut avoir un écart pour choisir des types MIME appropriés pour DLNA (Digital vivant Network Alliance).

Le \_ \_ type MIME MF PD \_ et [System. MIMEType](../properties/props-system-mimetype.md) ne correspondent peut-être pas toujours.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
