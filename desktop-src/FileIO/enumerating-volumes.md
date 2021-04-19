---
description: Pour obtenir une liste complète des volumes sur un ordinateur, ou pour manipuler chaque volume, vous pouvez énumérer les volumes.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Énumération des volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531716"
---
# <a name="enumerating-volumes"></a>Énumération des volumes

Pour obtenir une liste complète des volumes sur un ordinateur, ou pour manipuler chaque volume, vous pouvez énumérer les volumes. Au sein d’un volume, vous pouvez [Rechercher des dossiers montés](enumerating-volume-mount-points.md) ou d’autres objets sur le volume.

Trois fonctions permettent à une application d’énumérer des volumes sur un ordinateur :

-   [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

Ces trois fonctions fonctionnent de manière très similaire aux fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)et [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .

Commencez une recherche sur les volumes avec [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew). Si la recherche est réussie, traitez les résultats en fonction de la conception de votre application. Utilisez ensuite [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) dans une boucle pour localiser et traiter chaque volume suivant. Lorsque l’alimentation de volumes est épuisée, fermez la recherche avec [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).

Vous ne devez pas supposer une corrélation entre l’ordre des volumes retournés par ces fonctions et l’ordre des volumes retournés par d’autres fonctions ou outils. En particulier, ne supposez pas de corrélation entre l’ordre des volumes et les lettres de lecteur telles qu’elles sont affectées par le BIOS (le cas échéant) ou par l’administrateur de disque.

Pour obtenir un exemple d’énumération des volumes sur un ordinateur, consultez [exemples de dossiers montés](volume-mount-point-examples.md) .

 

 



