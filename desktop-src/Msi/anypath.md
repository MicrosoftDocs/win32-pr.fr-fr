---
description: Le type de données AnyPath est une chaîne de texte contenant un chemin d’accès complet ou un chemin d’accès relatif.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab5d8e7aaf4e92c2b33379b92b00263df07366ff340346aa19518478f8f2394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045779"
---
# <a name="anypath"></a>AnyPath

Le type de données AnyPath est une chaîne de texte contenant un chemin d’accès complet ou un chemin d’accès relatif. Lorsque vous spécifiez un chemin d’accès relatif, vous pouvez inclure un nom de fichier long avec le nom de fichier Short en séparant les noms courts et longs par une barre verticale ( \| ). Notez que vous ne pouvez pas spécifier plusieurs niveaux d’un répertoire ou des chemins d’accès complets de cette façon. Le chemin d’accès peut contenir des propriétés placées entre crochets ( \[ \] ).

Exemples de données AnyPath valides :

-   \\\\fichier \\ temporaire de partage de serveur \\
-   c : \\ temp
-   \\modèle
-   project ~ 1 \| Project état

Exemples de données AnyPath non valides :

-   c : \\ temp \\ project ~ 1 \| c : \\ temp one \\ Project status
-   \\\\état temp project ~ 1 \| \\ temp \\ un Project

 

 



