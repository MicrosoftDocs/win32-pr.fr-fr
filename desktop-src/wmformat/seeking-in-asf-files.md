---
title: Recherche dans des fichiers ASF (kit de développement logiciel (SDK) Windows Media format 11)
description: Recherche dans des fichiers ASF
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK, recherche dans les fichiers ASF
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), recherche
- ASF (format avancé des systèmes), recherche
- DirectShow, recherche dans des fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18389ded80f0202564cba0ce6384b5ff02d26fdd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032185"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Recherche dans des fichiers ASF (kit de développement logiciel (SDK) Windows Media format 11)

Le [lecteur ASF WM](wm-asf-reader-filter.md), via son interface **IMediaSeeking** , peut effectuer des recherches temporelles très précises sur du contenu Windows Media avec un index temporel. (Tout le contenu indexé à l’image contient également un index temporel.) La recherche avec précision de trame garantie n’est pas directement prise en charge dans le lecteur ASF WM, mais il existe un moyen de le faire si vous avez besoin de cette fonctionnalité. Tout d’abord, utilisez le kit de développement logiciel (SDK) de format Windows Media directement pour créer une instance de l’objet lecteur synchrone, ouvrir le fichier, obtenir l’horodatage associé à un cadre spécifié, puis utiliser l’interface DirectShow **IMediaSeeking** pour effectuer une recherche à ce moment-là. L’interface DirectShow **IVideoFrameStep** ne prend pas en charge la recherche de contenu Windows Media avec précision de trame. L’exemple DSSeekFm dans le kit de développement logiciel (SDK) de format Windows Media montre comment effectuer une recherche avec une précision de trame à l’aide du lecteur ASF WM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Filtre de lecteur ASF WM**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




