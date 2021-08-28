---
description: La résilience est la capacité d’une application à effectuer une récupération normale à partir de situations dans lesquelles un composant vital est manquant ou a été remplacée par une version incompatible.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Résilience
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73565a129c25b19e0fb362e5363626f1acfee0387b2d4e4826f79222e7425b96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810779"
---
# <a name="resiliency"></a>Résilience

La résilience est la capacité d’une application à effectuer une récupération normale à partir de situations dans lesquelles un composant vital est manquant ou a été remplacée par une version incompatible. en créant un package d’installation et en utilisant les [fonctions du programme](installer-functions.md)d’installation, les développeurs peuvent utiliser le Windows Installer pour produire des applications résilientes capables de récupérer à partir de ces situations.

-   Utilisez la liste source du programme d’installation pour augmenter la résilience des applications qui reposent sur les ressources réseau. Pour plus d’informations, consultez [résilience source](source-resiliency.md).
-   Utilisez l’API du programme d’installation pour vérifier si une fonctionnalité, un composant, un fichier ou une version de fichier critique est installé.
-   Utilisez l’API du programme d’installation pour vérifier le chemin d’accès à un composant au moment de l’exécution. Cela réduit la dépendance de votre application vis-à-vis des chemins d’accès de fichiers statiques, qui sont souvent différents entre les ordinateurs.
-   Utilisez le programme d’installation pour réinstaller des raccourcis endommagés, des entrées de Registre et d’autres composants sans avoir à réexécuter l’installation.
-   Augmentez la résilience de l’installation de votre produit en laissant la fonctionnalité d’annulation du programme d’installation activée. Pour plus d’informations, consultez [restauration de l’installation](rollback-installation.md).

 

 



