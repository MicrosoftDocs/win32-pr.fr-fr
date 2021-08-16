---
description: Spécifie l’identificateur de clé pour un fichier ASF (Advanced Systems Format) chiffré. Cet attribut correspond au champ ID de clé de l’en-tête de chiffrement de contenu, défini dans la spécification ASF.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: Attribut MF_PD_ASF_CONTENTENCRYPTION_KEYID (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edae0f324e7ab4889b21ae69714da16bfa88803db1d3aef808e4ba715522f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876432"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a>MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID (attribut)

Spécifie l’identificateur de clé pour un fichier ASF (Advanced Systems Format) chiffré. Cet attribut correspond au champ ID de clé de l’en-tête de chiffrement de contenu, défini dans la spécification ASF.

## <a name="data-type"></a>Type de données

Chaîne de caractères larges

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) récupère le champ ID de clé, le convertit en une chaîne de caractères larges, puis remplit un tableau de **WCHAR** qui se termine par un caractère null. La taille du tableau est égale au champ de la longueur de l’ID de clé de l’en-tête de chiffrement du contenu.

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

 

 




