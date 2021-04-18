---
description: Spécifie le modèle de conformité de périphérique pour un flux dans un fichier ASF (Advanced Systems Format).
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: Attribut MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519931"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a>Attribut de modèle de conformité de l' \_ \_ \_ appareil de métadonnées SD SD ASF \_ \_ \_

Spécifie le modèle de conformité de périphérique pour un flux dans un fichier ASF (Advanced Systems Format).

## <a name="data-type"></a>Type de données

Chaîne de caractères larges

## <a name="remarks"></a>Notes

Cet attribut s’applique aux descripteurs de flux pour le contenu ASF. Pour plus d’informations sur les modèles de conformité des appareils, consultez la rubrique « paramètres du modèle de conformité des appareils » dans le kit de développement logiciel (SDK) du format Windows Media.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.

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

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributs du descripteur de flux](stream-descriptor-attributes.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> </dl>

 

 




