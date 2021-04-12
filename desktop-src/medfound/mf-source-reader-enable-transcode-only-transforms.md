---
description: Permet au lecteur source d’utiliser des Media Foundation transformations (MFTs) optimisées pour le transcodage.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: Attribut MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525990"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a>L' \_ \_ attribut de \_ \_ transformation de transcodage \_ uniquement \_ des lecteurs source MF

Permet au [lecteur source](source-reader.md) d’utiliser des Media Foundation transformations (MFTS) optimisées pour le transcodage.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Certains MFTs, en particulier les décodeurs, sont optimisés pour le transcodage plutôt que pour la lecture. Par défaut, le lecteur source ne chargera pas ces transformations. Affectez la **valeur true** à cet attribut si vous souhaitez utiliser le transcodage MFTS avec le lecteur source.

Une application peut définir cet attribut s’il ne traite pas les données en temps réel (pour le transcodage ou des scénarios similaires). Dans le cas contraire, pour la lecture en temps réel, utilisez le comportement par défaut.

En interne, cet attribut oblige le lecteur source à inclure l’indicateur de **\_ \_ \_ transcodage \_ d’indicateur d’énumération MFT uniquement** lorsqu’il appelle [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lecteur source](source-reader.md)
</dt> </dl>

 

 




