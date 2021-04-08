---
title: Rendu du contenu
description: Rendu du contenu
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows Media Format SDK, rendu du contenu
- ASF (Advanced Systems Format), rendu du contenu
- ASF (format des systèmes avancés), rendu du contenu
- ASF (Advanced Systems Format), rendu du contenu
- ASF (format des systèmes avancés), rendu du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840733"
---
# <a name="rendering-content"></a><span data-ttu-id="872d8-108">Rendu du contenu</span><span class="sxs-lookup"><span data-stu-id="872d8-108">Rendering Content</span></span>

<span data-ttu-id="872d8-109">Le kit de développement logiciel (SDK) Windows Media format ne fournit pas de routines pour le rendu du contenu fourni par l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="872d8-109">The Windows Media Format SDK does not provide any routines for rendering content delivered by the reader object.</span></span> <span data-ttu-id="872d8-110">Si vous écrivez des applications pour lire le contenu dans des fichiers ASF, vous devez implémenter vos propres routines de rendu.</span><span class="sxs-lookup"><span data-stu-id="872d8-110">If you write applications to play back the content in ASF files, you must implement your own rendering routines.</span></span>

<span data-ttu-id="872d8-111">Vous devez être prudent lors du rendu du contenu pour vous assurer que les exemples sont rendus par ordre de présentation et que les exemples de flux différents sont synchronisés lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="872d8-111">You must be careful when rendering content to ensure that samples are rendered in order of presentation time and that samples from different streams are synchronized when rendering.</span></span> <span data-ttu-id="872d8-112">La méthode que vous employez pour garantir la synchronisation des flux dépend de la technique de rendu que vous utilisez pour votre application.</span><span class="sxs-lookup"><span data-stu-id="872d8-112">The method you employ to ensure stream synchronization will depend upon the rendering technique you use for your application.</span></span> <span data-ttu-id="872d8-113">En général, si vous avez des flux audio et vidéo, vous devez effectuer une synchronisation avec le flux audio, car une incohérence dans le flux audio est plus perceptible que quelques images supprimées dans un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="872d8-113">In general, if you have audio and video streams, you should synchronize to the audio stream, because inconsistency in the audio stream is more noticeable than a few dropped frames in a video stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="872d8-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="872d8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="872d8-115">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="872d8-115">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="872d8-116">**Pour récupérer des exemples de médias avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="872d8-116">**To Retrieve Media Samples with the Asynchronous Reader**</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="872d8-117">**Pour récupérer des exemples de médias avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="872d8-117">**To Retrieve Media Samples with the Synchronous Reader**</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




