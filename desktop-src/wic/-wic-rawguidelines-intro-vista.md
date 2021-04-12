---
description: Formats d’images BRUTes dans Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formats d’images BRUTes dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204211"
---
# <a name="raw-image-formats-in-windows-vista"></a>Formats d’images BRUTes dans Windows Vista

L’Explorateur Windows Vista, la Galerie de photos Windows Vista, la Galerie de photos Windows Live et la visionneuse de photos Windows 7 utilisent tous Windows Imaging Component (WIC) et, par conséquent, prennent en charge les formats d’images BRUTes quand les codecs appropriés sont installés sur l’ordinateur.

Étant donné que WIC est une architecture d’imagerie extensible, toute application WIC peut consommer de nouveaux formats d’image dès que de nouveaux codecs sont installés sur le système. Le WIC est donc idéal comme solution de Plug-and-Play pour les formats d’images BRUTs produits par les appareils photo numériques. Grâce au WIC, les applications Windows peuvent prendre en charge de nouveaux modèles d’appareil photo chaque fois que des codecs mis à jour sont disponibles (dans l’idéal, avec de nouvelles caméras). Les auteurs de codec peuvent prendre en charge ces scénarios en implémentant des interfaces WIC communes à tous les types d’images, comme décrit plus en détail dans ce document.

Aujourd’hui, la plupart des applications grand public n’ont aucune connaissance particulière des formats d’images BRUTes et n’exposent pas d’interface utilisateur pour ajuster les paramètres de traitement brut.

Toutefois, pour prendre en charge des applications d’imagerie spécialisées, les auteurs de codec brut doivent également implémenter l’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Cette interface expose des fonctionnalités spéciales pour les images BRUTes, telles que la possibilité d’effectuer des réglages d’image courants et de traiter (développer) des images BRUTes dans des espaces de couleur rouge-vert-bleu (RVB) spécifiés.

Plusieurs autres interfaces WIC sont importantes pour les auteurs de codec brut à implémenter. Celles-ci sont décrites plus en détail dans cette série de rubriques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



