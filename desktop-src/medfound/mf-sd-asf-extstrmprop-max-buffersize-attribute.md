---
description: Spécifie la taille maximale de la mémoire tampon, en octets, nécessaire pour un flux dans un fichier ASF (Advanced Systems Format).
ms.assetid: 1704a70a-a52b-4e7d-8a32-d0c4e97f8cc2
title: Attribut MF_SD_ASF_EXTSTRMPROP_MAX_BUFFERSIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399f6af425020a72caf6185da18f7747c037a71245b8e8d841d886d7b7eabd18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113729"
---
# <a name="mf_sd_asf_extstrmprop_max_buffersize-attribute"></a>MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ bufferSize attribut

Spécifie la taille maximale de la mémoire tampon, en octets, nécessaire pour un flux dans un fichier ASF (Advanced Systems Format).

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de flux pour le contenu ASF. Elle correspond au champ de la taille de la mémoire tampon de remplacement dans l’objet de propriétés de flux étendu. Pour plus d’informations, reportez-vous à la spécification ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF. L’application peut créer le descripteur de flux du flux à partir du descripteur de présentation en appelant [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

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

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributs du descripteur de flux](stream-descriptor-attributes.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> </dl>

 

 




