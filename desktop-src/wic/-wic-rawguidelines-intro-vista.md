---
description: Formats d’images brutes dans Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formats d’images brutes dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88026e85780706ca2bd5f23f5ca43ec49ae614d4c65e42ec19367b01b3f43423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709857"
---
# <a name="raw-image-formats-in-windows-vista"></a>Formats d’images brutes dans Windows Vista

Windows l’explorateur vista, la galerie de photos Windows vista, la galerie de photos windows Live et la visionneuse de photos Windows 7 utilisent tous Windows composant de création d’images (WIC) et, par conséquent, prennent en charge les formats d’images brutes quand les codecs appropriés sont installés sur l’ordinateur.

Étant donné que WIC est une architecture d’imagerie extensible, toute application WIC peut consommer de nouveaux formats d’image dès que de nouveaux codecs sont installés sur le système. Le WIC est donc idéal comme solution de Plug-and-Play pour les formats d’images BRUTs produits par les appareils photo numériques. grâce au WIC, les applications de Windows peuvent prendre en charge de nouveaux modèles d’appareil photo chaque fois que des codecs mis à jour sont disponibles (dans l’idéal, avec de nouvelles caméras). Les auteurs de codec peuvent prendre en charge ces scénarios en implémentant des interfaces WIC communes à tous les types d’images, comme décrit plus en détail dans ce document.

Aujourd’hui, la plupart des applications grand public n’ont aucune connaissance particulière des formats d’images BRUTes et n’exposent pas d’interface utilisateur pour ajuster les paramètres de traitement brut.

Toutefois, pour prendre en charge des applications d’imagerie spécialisées, les auteurs de codec brut doivent également implémenter l’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Cette interface expose des fonctionnalités spéciales pour les images BRUTes, telles que la possibilité d’effectuer des réglages d’image courants et de traiter (développer) des images BRUTes dans des espaces de couleur rouge-vert-bleu (RVB) spécifiés.

Plusieurs autres interfaces WIC sont importantes pour les auteurs de codec brut à implémenter. Celles-ci sont décrites plus en détail dans cette série de rubriques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



