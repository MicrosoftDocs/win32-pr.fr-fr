---
description: Contient les propriétés de configuration d’un encodeur.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: Attribut MFT_PREFERRED_ENCODER_PROFILE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfdc85ead0fe813215b3edaea14833400df5445d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951486"
---
# <a name="mft_preferred_encoder_profile-attribute"></a>\_Attribut de \_ profil d’encodeur préféré MFT \_

Contient les propriétés de configuration d’un encodeur.

## <a name="data-type"></a>Type de données

**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ stocké en tant que _*IUnknown \**_

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>S’applique à

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Notes

Cet attribut peut être défini sur l’objet d’activation renvoyé par la fonction [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) . L’attribut s’applique uniquement lorsque l’objet d’activation est configuré pour créer un encodeur. La valeur de l’attribut est un pointeur vers un magasin d’attributs, qui contient lui-même des propriétés à définir sur l’encodeur.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




