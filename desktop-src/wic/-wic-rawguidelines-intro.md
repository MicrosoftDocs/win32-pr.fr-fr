---
description: Introduction (recommandations de WIC pour les formats d’image RAW Camera)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introduction (recommandations de WIC pour les formats d’image RAW Camera)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96da37d36fed6af0aef271471eb2a0e5dae44bef71dfe14a4da37eba3f658c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086862"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>Introduction (recommandations de WIC pour les formats d’image RAW Camera)

le composant WIC (Windows Imaging Component) fournit une infrastructure extensible pour l’utilisation des images et des métadonnées d’image. Le WIC permet aux fournisseurs de logiciels et de matériel de développer des codecs afin que leurs propres formats d’image puissent obtenir la même prise en charge de plate-forme que les formats d’images natifs tels que TIFF (Tagged Image File Format), JPEG (Joint Photographic Experts Group) ou photo HD.

WIC fournit un ensemble unique et cohérent d’interfaces pour le traitement de tous les images, quel que soit le format d’image. Par conséquent, toute application qui utilise WIC reçoit la prise en charge automatique des nouveaux formats d’image dès l’installation du codec. WIC fournit également une infrastructure de métadonnées extensible qui permet aux applications de lire et d’écrire leurs propres métadonnées propriétaires directement dans des fichiers image, de sorte que les métadonnées ne sont jamais perdues ou séparées de l’image.

WIC est inclus avec Windows Presentation Foundation (WPF) et est intégré à Windows Vista et versions ultérieures Windows. il est également disponible en tant que composant redistribuable autonome pour Windows XP.

Ces instructions sont conçues pour aider les fabricants de format RAW dans le développement de codecs WIC.

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

 

 



