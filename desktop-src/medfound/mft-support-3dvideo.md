---
description: Spécifie si une Media Foundation transformation (MFT) prend en charge la vidéo stéréoscopique 3D.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: Attribut MFT_SUPPORT_3DVIDEO (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517740"
---
# <a name="mft_support_3dvideo-attribute"></a>\_Attribut 3DVIDEO de la prise en charge de MFT \_

Spécifie si une Media Foundation transformation (MFT) prend en charge la vidéo stéréoscopique 3D.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Pour interroger cet attribut, appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour obtenir le magasin d’attributs global de la table MFT. Si la condition **GetAttributes** est établie, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

La valeur par défaut de cet attribut est **false**. Traiter cet attribut comme étant en lecture seule. Ne modifiez pas la valeur ; la table MFT ignore toute modification apportée à la valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




