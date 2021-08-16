---
description: Formats de pixel à plage dynamique élevée
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Formats de pixel à plage dynamique élevée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a544d2331cc32943e3bc74400e1751111aac69e0a1448103e7651cb51da9353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086912"
---
# <a name="high-dynamic-range-pixel-formats"></a>Formats de pixel à plage dynamique élevée

les codecs doivent utiliser des formats de pixel du composant de création d’images Windows (WIC) qui conservent l’ensemble de la plage dynamique des données de capteur sous-jacentes. GUID \_ WICPixelFormat48bppRGB est un format de 16 bits à virgule fixe standard qui peut être utilisé. D’autres formats de précision plus élevée peuvent également être utilisés. pour activer la prise en charge complète du pipeline de rendu accéléré par l’unité de traitement graphique (GPU) Windows Presentation Foundation, Microsoft encourage fortement la prise en charge d’un format de pixel à virgule flottante 32 bits.

formats de pixel de couleur élevée : avec Windows 7, deux nouveaux formats de pixel WIC ont été ajoutés pour prendre en charge les nouveaux formats d’affichage haute couleur. Il s’agit des éléments suivants : GUID \_ WICPixelFormat32bppRGBA1010102 et GUID \_ WICPixelFormat32bppRGBA1010102XR.

Le format haute couleur flottant (BPC) de 16 bits par canal est pris en charge par le \_ format de pixel WICPIXELFORMAT64BPPRGBAHALF GUID existant.

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

 

 



