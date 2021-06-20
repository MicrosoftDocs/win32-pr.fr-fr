---
description: Découvrez comment le lecteur ASF WM peut effectuer une recherche temporelle très précise sur du contenu Windows Media avec un index temporel dans DirectShow.
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Recherche dans des fichiers ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ffc570536463b86a88e1f26be338bd748c790c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405582"
---
# <a name="seeking-in-asf-files-directshow"></a>Recherche dans des fichiers ASF (DirectShow)

Le [lecteur ASF WM](wm-asf-reader-filter.md), via son interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , peut effectuer des recherches temporelles très précises sur du contenu Windows Media avec un index temporel. (Tout le contenu indexé à l’image contient également un index temporel.) La recherche avec précision de trame garantie n’est pas directement prise en charge dans le lecteur ASF WM, mais il existe un moyen de le faire si vous avez besoin de cette fonctionnalité. Tout d’abord, utilisez le kit de développement logiciel (SDK) de format Windows Media directement pour créer une instance de l’objet lecteur synchrone, ouvrir le fichier, obtenir l’horodatage associé à un cadre spécifié, puis utiliser l’interface DirectShow **IMediaSeeking** pour effectuer une recherche à ce moment-là. L’interface [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) ne prend pas en charge la recherche de contenu Windows Media de manière précise.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture de fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



