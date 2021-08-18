---
description: Contient les propriétés de configuration d’un encodeur.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: Attribut MFT_PREFERRED_ENCODER_PROFILE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85acf742e518d91c6512b2b887cca910c3b19d21180500bd1180e6972255e54f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722504"
---
# <a name="mft_preferred_encoder_profile-attribute"></a>\_Attribut de \_ profil d’encodeur préféré MFT \_

Contient les propriétés de configuration d’un encodeur.

## <a name="data-type"></a>Type de données

**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \* *_ stocké sous la forme _* IUnknown\***

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>S’applique à

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Remarques

Cet attribut peut être défini sur l’objet d’activation renvoyé par la fonction [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) . L’attribut s’applique uniquement lorsque l’objet d’activation est configuré pour créer un encodeur. La valeur de l’attribut est un pointeur vers un magasin d’attributs, qui contient lui-même des propriétés à définir sur l’encodeur.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




