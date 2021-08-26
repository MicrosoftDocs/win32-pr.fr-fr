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
ms.openlocfilehash: 7add8d31f1fd025327325256e56c9f38faa4c97fd7e2aa206cedfebcc84c1302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929655"
---
# <a name="rendering-content"></a>Rendu du contenu

le kit de développement logiciel (SDK) Windows Media Format ne fournit pas de routines pour le rendu du contenu fourni par l’objet lecteur. Si vous écrivez des applications pour lire le contenu dans des fichiers ASF, vous devez implémenter vos propres routines de rendu.

Vous devez être prudent lors du rendu du contenu pour vous assurer que les exemples sont rendus par ordre de présentation et que les exemples de flux différents sont synchronisés lors du rendu. La méthode que vous employez pour garantir la synchronisation des flux dépend de la technique de rendu que vous utilisez pour votre application. En général, si vous avez des flux audio et vidéo, vous devez effectuer une synchronisation avec le flux audio, car une incohérence dans le flux audio est plus perceptible que quelques images supprimées dans un flux vidéo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> <dt>

[**Pour récupérer des exemples de médias avec le lecteur asynchrone**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Pour récupérer des exemples de médias avec le lecteur synchrone**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




