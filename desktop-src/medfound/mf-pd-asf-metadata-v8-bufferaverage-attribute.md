---
description: Spécifie la taille moyenne de la mémoire tampon nécessaire pour un fichier ASF (variable bit rate).
ms.assetid: 508d8670-5f5f-422b-9fa1-150115e2dbb8
title: Attribut MF_PD_ASF_METADATA_V8_BUFFERAVERAGE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac9328d0b176df23b103c49890ffa7646ae8c02e7205df95fecc5a64e5eebc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955409"
---
# <a name="mf_pd_asf_metadata_v8_bufferaverage-attribute"></a>\_ \_ Attribut BUFFERAVERAGE MF PD ASF \_ Metadata \_ V8 \_

Spécifie la taille moyenne de la mémoire tampon nécessaire pour un fichier ASF (variable bit rate).

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut qui s’applique au descripteur de présentation pour le contenu ASF.

> [!Note]  
> cet attribut s’applique uniquement aux fichiers créés par la version 8 du kit de développement logiciel (SDK) Windows Media Format. il correspond à l’attribut **BufferAverage** dans le kit de développement logiciel (SDK) de Format multimédia Windows.

 

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> <dt>

[Descripteurs de présentation](presentation-descriptors.md)
</dt> </dl>

 

 




