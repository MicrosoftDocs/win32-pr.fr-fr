---
description: La diffusion en continu est le processus qui consiste à conserver uniquement une petite partie d’un fichier audio en cours de lecture en mémoire. Cela permet de lire des fichiers audio volumineux, tels que la musique de fond, et de ne pas occuper une grande quantité de mémoire.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: Données audio de diffusion en continu XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1766b20f539f8bbe4d11204b681b7eddca58578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541980"
---
# <a name="xaudio2-streaming-audio-data"></a><span data-ttu-id="77645-104">Données audio de diffusion en continu XAudio2</span><span class="sxs-lookup"><span data-stu-id="77645-104">XAudio2 Streaming Audio Data</span></span>

<span data-ttu-id="77645-105">La diffusion en continu est le processus qui consiste à conserver uniquement une petite partie d’un fichier audio en cours de lecture en mémoire.</span><span class="sxs-lookup"><span data-stu-id="77645-105">Streaming is the process of maintaining only a small portion of a playing audio file in memory.</span></span> <span data-ttu-id="77645-106">Cela permet de lire des fichiers audio volumineux, tels que la musique de fond, et de ne pas occuper une grande quantité de mémoire.</span><span class="sxs-lookup"><span data-stu-id="77645-106">This allows large audio files such as background music to be played, and not take up a large amount of memory.</span></span>

<span data-ttu-id="77645-107">Lorsqu’un fichier audio est diffusé en continu, ses données sont lues à partir du disque dans des blocs au lieu de charger le fichier entier en une seule fois.</span><span class="sxs-lookup"><span data-stu-id="77645-107">When an audio file is streamed, its data is read from disk in chunks rather than loading the entire file at once.</span></span> <span data-ttu-id="77645-108">La diffusion en continu s’effectue en lisant de manière asynchrone les données audio dans une file d’attente de mémoires tampons de disque.</span><span class="sxs-lookup"><span data-stu-id="77645-108">Streaming is accomplished by asynchronously reading audio data into a queue of disk buffers.</span></span> <span data-ttu-id="77645-109">Chaque tampon est rempli, puis soumis à une voix source.</span><span class="sxs-lookup"><span data-stu-id="77645-109">Each buffer is filled, and then submitted to a source voice.</span></span> <span data-ttu-id="77645-110">Une fois que la voix a terminé la lecture d’une mémoire tampon, la mémoire tampon redevient disponible pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="77645-110">After the voice finishes playing a buffer, the buffer becomes available for reading again.</span></span> <span data-ttu-id="77645-111">Le fait de parcourir les tampons de disque de cette manière permet de lire un fichier audio volumineux alors que seule une partie de ses données est chargée.</span><span class="sxs-lookup"><span data-stu-id="77645-111">Looping through the disk buffers in this manner allows a large audio file to be played while only a portion of its data is loaded.</span></span> <span data-ttu-id="77645-112">Le code de diffusion en continu doit être placé dans un thread séparé, où il peut se mettre en veille en attendant la fin des opérations de lecture et d’exécution de disque de longue durée.</span><span class="sxs-lookup"><span data-stu-id="77645-112">The streaming code should be placed in a separate thread, where it can sleep while waiting for long-running disk and audio operations to finish.</span></span> <span data-ttu-id="77645-113">Une classe de rappel est utilisée pour réveiller le thread en déclenchant des événements lorsque des opérations audio sont terminées.</span><span class="sxs-lookup"><span data-stu-id="77645-113">A callback class is used to wake the thread by triggering events when audio operations have finished.</span></span>

<span data-ttu-id="77645-114">Pour obtenir un exemple de la façon dont la diffusion en continu peut être effectuée avec XAudio2, consultez [Comment : diffuser un son à partir d’un disque](how-to--stream-a-sound-from-disk.md).</span><span class="sxs-lookup"><span data-stu-id="77645-114">For an example of how streaming can be accomplished with XAudio2, see [How to: Stream a Sound from Disk](how-to--stream-a-sound-from-disk.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77645-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77645-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77645-116">Diffusion en continu de données audio</span><span class="sxs-lookup"><span data-stu-id="77645-116">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="77645-117">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="77645-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



