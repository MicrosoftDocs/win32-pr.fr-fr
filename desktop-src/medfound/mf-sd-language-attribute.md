---
description: Spécifie la langue d’un flux.
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: Attribut MF_SD_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209788"
---
# <a name="mf_sd_language-attribute"></a>\_Attribut de \_ langage SD MF

Spécifie la langue d’un flux.

## <a name="data-type"></a>Type de données

Chaîne de caractères larges

## <a name="remarks"></a>Notes

La valeur de cet attribut est une balise de langue conforme à la norme RFC 1766. Cet attribut s’applique aux descripteurs de flux.

Une source de média (ou tout objet qui crée un descripteur de flux) peut définir cet attribut si le flux a un langage spécifié. Les applications peuvent interroger cet attribut pour obtenir la langue. Si l’attribut n’est pas défini, le flux n’a pas de langue spécifiée.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



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
</dt> </dl>

 

 




