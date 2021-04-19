---
description: Le type de données AnyPath est une chaîne de texte contenant un chemin d’accès complet ou un chemin d’accès relatif.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527634"
---
# <a name="anypath"></a>AnyPath

Le type de données AnyPath est une chaîne de texte contenant un chemin d’accès complet ou un chemin d’accès relatif. Lorsque vous spécifiez un chemin d’accès relatif, vous pouvez inclure un nom de fichier long avec le nom de fichier Short en séparant les noms courts et longs par une barre verticale ( \| ). Notez que vous ne pouvez pas spécifier plusieurs niveaux d’un répertoire ou des chemins d’accès complets de cette façon. Le chemin d’accès peut contenir des propriétés placées entre crochets ( \[ \] ).

Exemples de données AnyPath valides :

-   \\\\fichier \\ temporaire de partage de serveur \\
-   c : \\ temp
-   \\modèle
-   Project ~ 1 \| État du projet

Exemples de données AnyPath non valides :

-   c : \\ temp \\ Project ~ 1 \| c : \\ État du \\ projet Temp One
-   \\\\État du projet Temp Project ~ 1 \| \\ temp \\

 

 



