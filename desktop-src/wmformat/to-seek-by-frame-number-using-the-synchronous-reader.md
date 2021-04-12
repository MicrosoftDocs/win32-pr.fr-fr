---
title: Pour rechercher par numéro de frame à l’aide du lecteur synchrone
description: Pour rechercher par numéro de frame à l’aide du lecteur synchrone
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- ASF (Advanced Systems Format), recherche par numéro de trame
- ASF (format avancé des systèmes), recherche par numéro de trame
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- lecteurs synchrones, recherche par numéros de frame
- flux vidéo, recherche par numéros de frame
- flux vidéo, lecteurs synchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314269"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a><span data-ttu-id="86c71-110">Pour rechercher par numéro de frame à l’aide du lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="86c71-110">To Seek By Frame Number Using the Synchronous Reader</span></span>

<span data-ttu-id="86c71-111">Pour rechercher des données par numéro de trame à l’aide du lecteur synchrone, vous spécifiez une plage pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="86c71-111">To seek for data by frame number using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="86c71-112">Une plage est définie par un numéro de frame de début dans un flux vidéo spécifique et un nombre de frames à lire.</span><span class="sxs-lookup"><span data-stu-id="86c71-112">A range is defined by a starting frame number in a specific video stream and a number of frames to play.</span></span>

<span data-ttu-id="86c71-113">Pour rechercher des données dans un fichier ASF par numéro de trame à l’aide du lecteur synchrone, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="86c71-113">To seek data in an ASF file by frame number using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="86c71-114">Définissez le nombre de frames de départ et le nombre d’images à lire pour l’exemple de remise en appelant [**IWMSyncReader :: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span><span class="sxs-lookup"><span data-stu-id="86c71-114">Set the starting frame number and number of frames to read for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="86c71-115">Vous devez spécifier le numéro de flux d’un flux vidéo indexé par une image.</span><span class="sxs-lookup"><span data-stu-id="86c71-115">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="86c71-116">Le lecteur synchronise le reste des sorties avec l’heure de présentation du frame spécifié du flux spécifié et commence à fournir des exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="86c71-116">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
2.  <span data-ttu-id="86c71-117">Commencez la récupération des exemples avec des appels à [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="86c71-117">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="86c71-118">Procédez comme vous le feriez normalement avec le lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="86c71-118">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86c71-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86c71-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86c71-120">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="86c71-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="86c71-121">**Lecture des fichiers avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="86c71-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




