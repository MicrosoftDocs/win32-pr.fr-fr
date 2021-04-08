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
# <a name="rendering-content"></a>Rendu du contenu

Le kit de développement logiciel (SDK) Windows Media format ne fournit pas de routines pour le rendu du contenu fourni par l’objet lecteur. Si vous écrivez des applications pour lire le contenu dans des fichiers ASF, vous devez implémenter vos propres routines de rendu.

Vous devez être prudent lors du rendu du contenu pour vous assurer que les exemples sont rendus par ordre de présentation et que les exemples de flux différents sont synchronisés lors du rendu. La méthode que vous employez pour garantir la synchronisation des flux dépend de la technique de rendu que vous utilisez pour votre application. En général, si vous avez des flux audio et vidéo, vous devez effectuer une synchronisation avec le flux audio, car une incohérence dans le flux audio est plus perceptible que quelques images supprimées dans un flux vidéo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> <dt>

[**Pour récupérer des exemples de médias avec le lecteur asynchrone**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Pour récupérer des exemples de médias avec le lecteur synchrone**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




