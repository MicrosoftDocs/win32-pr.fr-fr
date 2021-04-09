---
description: Spécifie le type de mécanisme de protection utilisé dans un fichier ASF (Advanced Systems Format).
ms.assetid: 91ceb610-6ff4-4133-beab-6debb94eec2c
title: Attribut MF_PD_ASF_CONTENTENCRYPTION_TYPE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9131b24138edf6e85fc0e264bdcdd028f2eb0538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862501"
---
# <a name="mf_pd_asf_contentencryption_type-attribute"></a>\_Attribut de \_ \_ type CONTENTENCRYPTION \_ pour MF PD ASF

Spécifie le type de mécanisme de protection utilisé dans un fichier ASF (Advanced Systems Format).

## <a name="data-type"></a>Type de données

Chaîne de caractères larges

## <a name="remarks"></a>Notes

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) récupère le champ type de protection, le convertit en une chaîne de caractères larges, puis remplit un tableau de **WCHAR** qui se termine par un caractère null. S’il est présent, la valeur doit être « DRM ». La taille du tableau est égale au champ de longueur du champ de type de protection de l’en-tête de chiffrement de contenu.

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

 

 




