---
description: Contient des données de chiffrement pour un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de chiffrement de contenu étendu dans l’en-tête ASF, défini dans la spécification ASF.
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: Attribut MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550e75f50a7f09556cd9dd89239b3f33fb74d289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318801"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a>\_Attribut de \_ \_ données de \_ chiffrement CONTENTENCRYPTIONEX \_ pour MF PD ASF

Contient des données de chiffrement pour un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de chiffrement de contenu étendu dans l’en-tête ASF, défini dans la spécification ASF.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crée le descripteur de présentation et génère cet attribut à partir de l’en-tête d’objet de chiffrement de contenu étendu. La taille de l’objet blob est égale au champ de la taille des données. Le tableau d’octets contenu dans l’objet blob est égal au champ de données de l’objet de chiffrement de contenu étendu de l’en-tête ASF.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> <dt>

[Descripteurs de présentation](presentation-descriptors.md)
</dt> </dl>

 

 




