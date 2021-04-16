---
description: Recherche dans des fichiers ASF
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Recherche dans des fichiers ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e957fbdf7ed7df1a9cb38b14e39d384b15ab25b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521287"
---
# <a name="seeking-in-asf-files-directshow"></a><span data-ttu-id="20445-103">Recherche dans des fichiers ASF (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="20445-103">Seeking in ASF Files (DirectShow)</span></span>

<span data-ttu-id="20445-104">Le [lecteur ASF WM](wm-asf-reader-filter.md), via son interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , peut effectuer des recherches temporelles très précises sur du contenu Windows Media avec un index temporel.</span><span class="sxs-lookup"><span data-stu-id="20445-104">The [WM ASF Reader](wm-asf-reader-filter.md), through its [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="20445-105">(Tout le contenu indexé à l’image contient également un index temporel.) La recherche avec précision de trame garantie n’est pas directement prise en charge dans le lecteur ASF WM, mais il existe un moyen de le faire si vous avez besoin de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="20445-105">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="20445-106">Tout d’abord, utilisez le kit de développement logiciel (SDK) de format Windows Media directement pour créer une instance de l’objet lecteur synchrone, ouvrir le fichier, obtenir l’horodatage associé à un cadre spécifié, puis utiliser l’interface DirectShow **IMediaSeeking** pour effectuer une recherche à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="20445-106">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="20445-107">L’interface [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) ne prend pas en charge la recherche de contenu Windows Media de manière précise.</span><span class="sxs-lookup"><span data-stu-id="20445-107">The [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface does not support frame-accurate seeking of Windows Media–based content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20445-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20445-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20445-109">Lecture de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="20445-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



