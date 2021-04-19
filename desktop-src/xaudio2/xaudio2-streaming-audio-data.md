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
# <a name="xaudio2-streaming-audio-data"></a>Données audio de diffusion en continu XAudio2

La diffusion en continu est le processus qui consiste à conserver uniquement une petite partie d’un fichier audio en cours de lecture en mémoire. Cela permet de lire des fichiers audio volumineux, tels que la musique de fond, et de ne pas occuper une grande quantité de mémoire.

Lorsqu’un fichier audio est diffusé en continu, ses données sont lues à partir du disque dans des blocs au lieu de charger le fichier entier en une seule fois. La diffusion en continu s’effectue en lisant de manière asynchrone les données audio dans une file d’attente de mémoires tampons de disque. Chaque tampon est rempli, puis soumis à une voix source. Une fois que la voix a terminé la lecture d’une mémoire tampon, la mémoire tampon redevient disponible pour la lecture. Le fait de parcourir les tampons de disque de cette manière permet de lire un fichier audio volumineux alors que seule une partie de ses données est chargée. Le code de diffusion en continu doit être placé dans un thread séparé, où il peut se mettre en veille en attendant la fin des opérations de lecture et d’exécution de disque de longue durée. Une classe de rappel est utilisée pour réveiller le thread en déclenchant des événements lorsque des opérations audio sont terminées.

Pour obtenir un exemple de la façon dont la diffusion en continu peut être effectuée avec XAudio2, consultez [Comment : diffuser un son à partir d’un disque](how-to--stream-a-sound-from-disk.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Diffusion en continu de données audio](streaming-audio-data.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> </dl>

 

 



