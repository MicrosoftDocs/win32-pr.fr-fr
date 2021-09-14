---
title: Obtenir les meilleures performances de recherche de vidéos
description: Obtenir les meilleures performances de recherche de vidéos
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media Format SDK, meilleures performances de recherche de vidéos
- ASF (Advanced Systems Format), meilleures performances de recherche de vidéos
- ASF (format de systèmes avancés), meilleures performances de recherche de vidéos
- ASF (Advanced Systems Format), performances de recherche de vidéos
- ASF (format de systèmes avancés), performances de recherche de vidéos
- ASF (Advanced Systems Format), performances
- ASF (format des systèmes avancés), performances
- recherche de vidéos
- performances, recherche de vidéos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293147"
---
# <a name="getting-the-best-video-seeking-performance"></a>Obtenir les meilleures performances de recherche de vidéos

La recherche de contenu dans un fichier est une opération très courante qui est potentiellement un problème de performances. la vidéo encodée avec le codec Windows Media Video 9 est constituée principalement d’images delta, qui enregistrent uniquement les modifications par rapport au frame précédent. La reconstruction des frames Delta prend du temps, en particulier si les images clés sont éloignées. pour plus d’informations sur la configuration d’images clés pour une recherche efficace, consultez [configuration de la vidéo Flux pour la recherche de performances](configuring-video-streams-for-seeking-performance.md).

En plus de la configuration appropriée, vous pouvez améliorer les performances de recherche à l’aide de l’indexation des frames pour le flux vidéo. La recherche d’un numéro de trame est généralement plus rapide que la recherche d’une heure de présentation.

En cas de recherche dans un fichier contenant plusieurs flux, vous ne devez sélectionner que les flux nécessaires. Chaque flux de donnée configuré pour la lecture aura une incidence sur les performances de la recherche, car tous les flux sélectionnés sont synchronisés lorsque vous recherchez un point dans un fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> <dt>

[**Pour rechercher par numéro de frame à l’aide du lecteur asynchrone**](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[**Pour rechercher par numéro de frame à l’aide du lecteur synchrone**](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[**Pour effectuer une recherche par heure à l’aide du lecteur asynchrone**](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[**Pour effectuer une recherche par heure à l’aide du lecteur synchrone**](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




