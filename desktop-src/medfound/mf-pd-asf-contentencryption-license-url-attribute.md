---
description: Spécifie l’URL d’acquisition de licence pour un fichier ASF (Advanced Systems Format) chiffré. Cet attribut correspond au champ URL de licence de l’en-tête de chiffrement de contenu, défini dans la spécification ASF.
ms.assetid: fe431c38-8227-4385-ac6f-72b9982cde62
title: Attribut MF_PD_ASF_CONTENTENCRYPTION_LICENSE_URL (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5245ebbc5bfeac8b363898b4913c82b94990fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484817"
---
# <a name="mf_pd_asf_contentencryption_license_url-attribute"></a>\_Attribut d' \_ \_ URL de \_ licence CONTENTENCRYPTION pour MF PD ASF \_

Spécifie l’URL d’acquisition de licence pour un fichier ASF (Advanced Systems Format) chiffré. Cet attribut correspond au champ URL de licence de l’en-tête de chiffrement de contenu, défini dans la spécification ASF.

## <a name="data-type"></a>Type de données

Chaîne de caractères larges

## <a name="remarks"></a>Notes

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) récupère le champ URL de licence, le convertit en une chaîne de caractères larges, puis remplit un tableau de **WCHAR** qui se termine par un caractère null. La taille du tableau est égale au champ longueur de l’URL de licence de l’en-tête de chiffrement de contenu.

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

[**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> <dt>

[Descripteurs de présentation](presentation-descriptors.md)
</dt> </dl>

 

 




