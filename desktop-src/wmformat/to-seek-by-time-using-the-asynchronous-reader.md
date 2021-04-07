---
title: Pour effectuer une recherche par heure à l’aide du lecteur asynchrone
description: Pour effectuer une recherche par heure à l’aide du lecteur asynchrone
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- ASF (Advanced Systems Format), recherche par heure
- ASF (format de systèmes avancés), recherche par heure
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- lecteurs asynchrones, recherche par heure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723563"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a><span data-ttu-id="d0c67-108">Pour effectuer une recherche par heure à l’aide du lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="d0c67-108">To Seek By Time Using the Asynchronous Reader</span></span>

<span data-ttu-id="d0c67-109">Si vous souhaitez rechercher une heure de présentation spécifique dans un fichier ASF, le fichier doit être correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="d0c67-109">If you want to seek to a specific presentation time in an ASF file, the file must be properly configured.</span></span> <span data-ttu-id="d0c67-110">Vous pouvez rechercher des fichiers audio uniquement par défaut, mais les fichiers vidéo doivent être indexés avant la recherche.</span><span class="sxs-lookup"><span data-stu-id="d0c67-110">You can seek in audio only files by default, but video files need to be indexed before seeking.</span></span> <span data-ttu-id="d0c67-111">Si vous n’êtes pas sûr de la façon dont un fichier a été créé, vous pouvez vérifier l' \_ attribut g wszWMSeekable dans l’en-tête du fichier en appelant [**IWMHeaderInfo :: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="d0c67-111">If you are not sure about how a file has been created, you can check the g\_wszWMSeekable attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="d0c67-112">Pour rechercher des données dans un fichier ASF par heure de présentation à l’aide du lecteur asynchrone, appelez [**IWMReader :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), en passant la durée souhaitée et la durée de la partie du fichier que vous souhaitez lire en tant que *cnsStart* et *cnsDuration* , respectivement.</span><span class="sxs-lookup"><span data-stu-id="d0c67-112">To seek to data in an ASF file by presentation time using the asynchronous reader, call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passing the desired time and duration of the part of the file you want to read as *cnsStart* and *cnsDuration* respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0c67-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d0c67-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0c67-114">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="d0c67-114">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="d0c67-115">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="d0c67-115">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="d0c67-116">**Lecture des métadonnées lors de la lecture**</span><span class="sxs-lookup"><span data-stu-id="d0c67-116">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="d0c67-117">**Utilisation des index**</span><span class="sxs-lookup"><span data-stu-id="d0c67-117">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




