---
description: Spécifie la date et l’heure de création d’un fichier ASF (Advanced Systems Format).
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: Attribut MF_PD_ASF_FILEPROPERTIES_CREATION_TIME (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1a015e251e04c706e2d36b7ab85cac4e8038ad2083c9e0089fbe847d835227a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104355"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a>\_Attribut de \_ \_ Date de \_ création \_ MF PD ASF

Spécifie la date et l’heure de création d’un fichier ASF (Advanced Systems Format).

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF. la valeur de l’attribut est une structure **FILETIME** , qui est documentée dans la SDK Windows.

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

 

 




