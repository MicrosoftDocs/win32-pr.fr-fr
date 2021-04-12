---
description: Introduction (recommandations de WIC pour les formats d’image RAW Camera)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introduction (recommandations de WIC pour les formats d’image RAW Camera)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204210"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>Introduction (recommandations de WIC pour les formats d’image RAW Camera)

Le composant WIC (Windows Imaging Component) fournit une infrastructure extensible pour l’utilisation des images et des métadonnées d’image. Le WIC permet aux fournisseurs de logiciels et de matériel de développer des codecs afin que leurs propres formats d’image puissent obtenir la même prise en charge de plate-forme que les formats d’images natifs tels que TIFF (Tagged Image File Format), JPEG (Joint Photographic Experts Group) ou photo HD.

WIC fournit un ensemble unique et cohérent d’interfaces pour le traitement de tous les images, quel que soit le format d’image. Par conséquent, toute application qui utilise WIC reçoit la prise en charge automatique des nouveaux formats d’image dès l’installation du codec. WIC fournit également une infrastructure de métadonnées extensible qui permet aux applications de lire et d’écrire leurs propres métadonnées propriétaires directement dans des fichiers image, de sorte que les métadonnées ne sont jamais perdues ou séparées de l’image.

WIC est inclus avec Windows Presentation Foundation (WPF) et est intégré à Windows Vista et versions ultérieures de Windows. Il est également disponible en tant que composant redistribuable autonome pour Windows XP.

Ces instructions sont conçues pour aider les fabricants de format RAW dans le développement de codecs WIC.

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

 

 



