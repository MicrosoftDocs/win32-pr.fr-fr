---
title: À propos du gestionnaire de compression vidéo
description: À propos du gestionnaire de compression vidéo
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Windows multimédia, gestionnaire de compression vidéo (VCM)
- multimédia, gestionnaire de compression vidéo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364032"
---
# <a name="about-the-video-compression-manager"></a>À propos du gestionnaire de compression vidéo

En règle générale, les compresseurs installables utilisent des données d’image vidéo stockées dans des fichiers AVI (Audio-Video entrelacés). Cette vue d’ensemble explique les techniques de programmation utilisées pour accéder aux compresseurs installables par le biais de VCM et aborde les sujets suivants :

-   VCM et vidéo pour l’architecture Windows
-   Compression et décompression des données d’image de votre application
-   Utilisation de convertisseurs VCM pour dessiner des données à partir de votre application
-   Structures et fonctions VCM

Avant de lire cette vue d’ensemble, vous devez être familiarisé avec les services graphiques Microsoft Win32. En particulier, les bitmaps et les structures associées à la bitmap, telles que [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) et [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), sont largement utilisées par VCM. Pour plus d’informations sur les structures **BITMAPINFO,** et **BITMAPINFOHEADER** , consultez [bitmaps](/previous-versions//ms532349(v=vs.85)).

> [!Note]  
> Le gestionnaire de compression audio (ACM) fournit une prise en charge au niveau du système pour les pilotes de compression et de décompression audio. Pour obtenir une description des services de compression audio, consultez [Gestionnaire de compression audio](audio-compression-manager.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> </dl>

 

 