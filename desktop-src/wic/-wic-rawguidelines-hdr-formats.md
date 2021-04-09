---
description: Formats de pixel à plage dynamique élevée
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Formats de pixel à plage dynamique élevée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867322"
---
# <a name="high-dynamic-range-pixel-formats"></a>Formats de pixel à plage dynamique élevée

Les codecs doivent utiliser des formats de pixel WIC (Windows Imaging Component) qui conservent l’ensemble de la plage dynamique des données de capteur sous-jacentes. GUID \_ WICPixelFormat48bppRGB est un format de 16 bits à virgule fixe standard qui peut être utilisé. D’autres formats de précision plus élevée peuvent également être utilisés. Pour activer la prise en charge complète du pipeline de rendu accéléré par l’unité de traitement graphique (GPU) Windows Presentation Foundation, Microsoft encourage fortement la prise en charge d’un format de pixel à virgule flottante 32 bits.

Formats de pixel de couleur élevée : avec Windows 7, deux nouveaux formats de pixel WIC ont été ajoutés pour prendre en charge les nouveaux formats d’affichage 65536 couleurs. Il s’agit des éléments suivants : GUID \_ WICPixelFormat32bppRGBA1010102 et GUID \_ WICPixelFormat32bppRGBA1010102XR.

Le format haute couleur flottant (BPC) de 16 bits par canal est pris en charge par le \_ format de pixel WICPIXELFORMAT64BPPRGBAHALF GUID existant.

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

 

 



