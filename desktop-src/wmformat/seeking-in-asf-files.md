---
title: recherche dans des fichiers ASF (kit de développement logiciel (SDK) Windows Media Format 11)
description: découvrez comment le lecteur ASF WM peut effectuer des recherches temporelles très précises sur Windows contenu basé sur des médias avec un index temporel dans Windows kit de développement logiciel (SDK) media Format 11.
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
ms.openlocfilehash: 6730f1535c9601cfd0697e374ddfa35b05250ed49fc4b575fa3458b69e389285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845894"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>recherche dans des fichiers ASF (kit de développement logiciel (SDK) Windows Media Format 11)

le [lecteur ASF WM](wm-asf-reader-filter.md), par le biais de son interface **IMediaSeeking** , peut effectuer des recherches temporelles très précises sur Windows contenu basé sur des médias avec un index temporel. (Tout le contenu indexé à l’image contient également un index temporel.) La recherche avec précision de trame garantie n’est pas directement prise en charge dans le lecteur ASF WM, mais il existe un moyen de le faire si vous avez besoin de cette fonctionnalité. tout d’abord, utilisez directement le kit de développement logiciel (SDK) de Format multimédia Windows pour créer une instance de l’objet lecteur synchrone, ouvrir le fichier, obtenir l’horodatage associé à un cadre spécifié, puis utiliser l’interface DirectShow **IMediaSeeking** pour effectuer une recherche à ce moment-là. l’interface DirectShow **IVideoFrameStep** ne prend pas en charge la recherche d’un contenu multimédia Windows. l’exemple DSSeekFm dans le kit de développement logiciel (SDK) de Format de média Windows montre comment effectuer une recherche à précision de trame à l’aide du lecteur ASF WM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Filtre de lecteur ASF WM**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




