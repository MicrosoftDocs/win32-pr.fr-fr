---
title: Utilisation des index
description: Utilisation des index
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media Format SDK, index
- ASF (Advanced Systems Format), index
- ASF (format avancé des systèmes), index
- index, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839649"
---
# <a name="working-with-indexes"></a>Utilisation des index

Le kit de développement logiciel (SDK) Windows Media format prend en charge la recherche et la striding de contenu. La recherche vous permet de spécifier un emplacement dans la chronologie du fichier pour commencer la lecture. Striding vous permet d’avancer rapidement et de rembobiner la sortie d’un fichier. Les fichiers doivent être indexés pour tirer parti de ces fonctionnalités. Un index est une série de valeurs représentant des positions dans le fichier (heures de présentation, numéros de trame ou codes de temps SMTP) avec des décalages correspondants dans la section de données du fichier pour chaque. L’indexation est plus importante pour les flux vidéo, car l’heure de présentation du flux audio peut être facilement estimée. Toutefois, certains flux audio peuvent également nécessiter des index. Par défaut, le writer indexe chaque nouveau fichier ASF. Si des modifications sont apportées au contenu d’un fichier, vous devez actualiser vous-même l’index à l’aide de l’objet indexeur.

L’indexeur prend en charge l’indexation temporelle et l’indexation basée sur les trames, ainsi que l’indexation basée sur les codes temporels SMPTE (le cas échéant). L’enregistreur crée un index temporel par défaut pour chaque nouveau flux vidéo encodé dans un fichier. Vous devez explicitement configurer et appeler l’indexeur pour créer un index de code de temps basé sur des trames ou SMPTE.

Lorsque des modifications sont apportées au contenu d’un fichier ASF, elles doivent être réindexées.

Les sections suivantes présentent un exemple de code pour l’exécution de tâches d’indexation courantes.

-   [Pour désactiver l’indexation automatique](to-disable-automatic-indexing.md)
-   [Pour configurer l’indexeur](to-configure-the-indexer.md)
-   [Pour indexer un fichier ASF](to-index-an-asf-file.md)
-   [Pour arrêter l’indexation en cours](to-stop-indexing-in-progress.md)

En outre, l’exemple d’application DSCopy illustre l’utilisation de l’indexeur. Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).

 

 




