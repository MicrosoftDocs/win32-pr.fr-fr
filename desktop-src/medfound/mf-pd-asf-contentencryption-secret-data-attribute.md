---
description: Contient des données secrètes pour un fichier ASF (Advanced Systems Format) chiffré. Cet attribut correspond au champ de données secrètes de l’en-tête de chiffrement de contenu, défini dans la spécification ASF.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: Attribut MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e628bf52aa08074473f14a84ee1d1fe39fe91c130aa9848be687601b864393a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104365"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a>\_Attribut de \_ \_ données de \_ secret CONTENTENCRYPTION pour MF PD ASF \_

Contient des données secrètes pour un fichier ASF (Advanced Systems Format) chiffré. Cet attribut correspond au champ de données secrètes de l’en-tête de chiffrement de contenu, défini dans la spécification ASF.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) remplit un tableau d’octets avec le champ de données de secret. La taille du tableau est égale au champ de la longueur des données secrètes de l’en-tête de chiffrement du contenu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
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

 

 




