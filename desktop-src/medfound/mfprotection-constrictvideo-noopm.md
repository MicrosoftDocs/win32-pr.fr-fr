---
description: Cet attribut spécifie une protection supplémentaire offerte par une autorité d’approbation de sortie vidéo (OTA) lorsqu’un connecteur n’offre pas de protection de sortie.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: Attribut MFPROTECTION_CONSTRICTVIDEO_NOOPM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72d1d7cd858ec9cf254cca1dffc5fef4e24fbb5a3a288975a9f70c9ae118dde3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713739"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a>MFPROTECTION \_ CONSTRICTVIDEO \_ NOOPM, attribut

Cet attribut spécifie une protection supplémentaire offerte par une autorité d’approbation de sortie vidéo (OTA) lorsqu’un connecteur n’offre pas de protection de sortie.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Remarques

Il s’agit d’une protection supplémentaire offerte par une autorité d’approbation de sortie vidéo (OTA) lorsqu’un connecteur n’offre pas de protection de sortie (voir [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)). Dans ce cas, le OTA peut proposer cette protection dont l’effet est identique à la protection [MFPROTECTION \_ CONSTRICTVIDEO](mfprotection-constrictvideo.md) . Cela est défini pour éviter toute confusion avec les appels précédents à [**IMFOutputPolicy :: GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interactions où la présence de la \_ protection MFPROTECTION CONSTRICTVIDEO a été utilisée pour aider à identifier le Pseudo-connecteur du gestionnaire de fenêtrage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




