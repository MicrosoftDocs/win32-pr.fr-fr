---
description: Transformations de Media Foundation
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Transformations de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61057831383c808a3e05cbe2e9cd779b46522a7a3d52d379b936f27c549d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268699"
---
# <a name="media-foundation-transforms"></a>Transformations de Media Foundation

Les transformations de Media Foundation (MFTs) fournissent un modèle générique pour le traitement des données multimédias. Les MFTs sont utilisés pour les décodeurs, les encodeurs et les processeurs de signal numérique (DSP). En bref, tout ce qui se trouve dans le pipeline de média entre la source du média et le récepteur multimédia est une table MFT.

Cette section décrit le modèle de programmation MFT et comment implémenter une table MFT, avec des recommandations pour des types spécifiques de MFTs, tels que les décodeurs.



| Rubrique                                                                    | Description                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos de MFTs](about-mfts.md)                                             | Fournit une brève vue d’ensemble de MFTs                                                                                                                                                                   |
| [Modèle de traitement MFT de base](basic-mft-processing-model.md)             | Décrit plus en détail le modèle de base pour le traitement des données avec une table MFT.                                                                                                                           |
| [MFTs asynchrone](asynchronous-mfts.md)                               | Décrit un modèle de traitement asynchrone qui est une alternative au modèle de base.<br/> le traitement asynchrone a été introduit dans Windows 7. Toutes les MFT ne prennent pas en charge ce modèle.<br/> |
| [Inscription et énumération de MFTs](registering-and-enumerating-mfts.md) | Comment inscrire une table MFT et comment énumérer les MFTs dans le registre.                                                                                                                                   |
| [Champ des restrictions d’utilisation](field-of-use-restrictions.md)               | Décrit le mécanisme de déverrouillage d’une table MFT qui a des restrictions de champ d’utilisation.                                                                                                                    |
| [Comparaison entre MFT et DMO](comparison-of-mfts-and-dmos.md)           | Résume les différences entre MFTs et DMOs.                                                                                                                                                   |
| [Écriture d’une table MFT personnalisée](writing-a-custom-mft.md)                         | Instructions pour l’écriture d’une table MFT personnalisée.                                                                                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Architecture Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




