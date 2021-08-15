---
description: Spécifie la durée, en unités de 100 nanosecondes, nécessaire pour envoyer un fichier ASF (Advanced Systems Format). L’heure d’envoi d’un paquet est l’heure à laquelle le paquet doit être remis sur le réseau. Il ne s’agit pas de l’heure de présentation du paquet.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: Attribut MF_PD_ASF_FILEPROPERTIES_SEND_DURATION (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce635cd02766a3c9ca8b0a0d327db93a4bcaaca76bccd6ae54fda726684ec641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740941"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a>\_Attribut de \_ \_ durée d' \_ envoi \_ MF PD ASF

Spécifie la durée, en unités de 100 nanosecondes, nécessaire pour envoyer un fichier ASF (Advanced Systems Format). L’heure d' *envoi* d’un paquet est l’heure à laquelle le paquet doit être remis sur le réseau. Il ne s’agit pas de l’heure de présentation du paquet.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.

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

 

 




