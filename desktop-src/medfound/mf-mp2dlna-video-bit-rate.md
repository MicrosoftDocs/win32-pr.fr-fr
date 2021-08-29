---
description: Spécifie la vitesse de transmission vidéo maximale pour le récepteur multimédia DLNA (Digital vivant Network Alliance).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: Attribut MF_MP2DLNA_VIDEO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f1e518ded74435f88d823bebe90bde0c6f2355714c1d67c3238207a4a4565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104745"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a>\_Attribut de \_ \_ vitesse de transmission vidéo MP2DLNA MF \_

Spécifie la vitesse de transmission vidéo maximale pour le récepteur multimédia DLNA (Digital vivant Network Alliance).

## <a name="data-type"></a>Type de données

**UINT32**

La valeur est la vitesse de transmission maximale cible pour le flux vidéo encodé, en bits par seconde. La valeur maximale est 9,8 millions (9,8 Mbits/s), qui est également la valeur par défaut.

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur le récepteur multimédia DLNA, interrogez le récepteur multimédia pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Définissez l’attribut avant le début de la diffusion en continu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




