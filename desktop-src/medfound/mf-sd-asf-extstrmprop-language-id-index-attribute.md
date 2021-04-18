---
description: Spécifie la langue utilisée par un flux dans un fichier ASF (Advanced Systems Format).
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: Attribut MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2afcf2388d2c0641aede4ff0eaccac9178207fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536473"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a>MF \_ SD \_ ASF \_ EXTSTRMPROP \_ \_ ID d' \_ index de langue

Spécifie la langue utilisée par un flux dans un fichier ASF (Advanced Systems Format).

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique aux descripteurs de flux pour le contenu ASF. La valeur est un index dans la liste des langues contenues dans l’attribut [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) .

Cet attribut correspond au champ d’index de l’ID de langue du flux dans l’objet de propriétés de flux étendu. Pour plus d’informations, reportez-vous à la spécification ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF. L’application peut créer le descripteur de flux du flux à partir du descripteur de présentation en appelant [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

Vous pouvez également obtenir la balise de langue en interrogeant le descripteur de flux pour l’attribut de [**\_ \_ langage SD MF**](mf-sd-language-attribute.md) .

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

 

 




