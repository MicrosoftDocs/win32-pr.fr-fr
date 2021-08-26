---
description: Spécifie la manière dont une transformation de Media Foundation (MFT) doit générer un flux vidéo stéréoscopique 3D.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: Attribut MF_ENABLE_3DVIDEO_OUTPUT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed361ef53d628e0970ffa35f9920750c9d3b0f7efbe81a0ef8759e8ba00a45ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013169"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>\_Activer l' \_ attribut de \_ sortie 3DVIDEO MF

Spécifie la manière dont une transformation de Media Foundation (MFT) doit générer un flux vidéo stéréoscopique 3D.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

La valeur de l’attribut est un membre de l’énumération [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .

Cet attribut s’applique uniquement si la table MFT retourne la **valeur true** pour l’attribut [ \_ \_ 3DVIDEO de prise en charge MFT](mft-support-3dvideo.md) .

Pour récupérer ou définir cet attribut, appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour récupérer le magasin d’attributs global de la table MFT.

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

 

 




