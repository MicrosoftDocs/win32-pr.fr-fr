---
description: Spécifie si une Media Foundation transformation (MFT) prend en charge la vidéo stéréoscopique 3D.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: Attribut MFT_SUPPORT_3DVIDEO (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da60bac92d1274f9d9a6624e247fc24d122ec26eabc103ad2d43477ae8f6b64b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776989"
---
# <a name="mft_support_3dvideo-attribute"></a>\_Attribut 3DVIDEO de la prise en charge de MFT \_

Spécifie si une Media Foundation transformation (MFT) prend en charge la vidéo stéréoscopique 3D.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Remarques

Pour interroger cet attribut, appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour obtenir le magasin d’attributs global de la table MFT. Si la condition **GetAttributes** est établie, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

La valeur par défaut de cet attribut est **false**. Traiter cet attribut comme étant en lecture seule. Ne modifiez pas la valeur ; la table MFT ignore toute modification apportée à la valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




