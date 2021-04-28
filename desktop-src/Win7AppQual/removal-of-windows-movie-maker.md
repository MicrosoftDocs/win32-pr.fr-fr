---
description: Suppression de Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Suppression de Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116267"
---
# <a name="removal-of-windows-movie-maker"></a>Suppression de Windows Movie Maker

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**Serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -haute  
**Fréquence** -moyenne  


## <a name="description"></a>Description

Microsoft déprécie et supprime l’utilitaire Windows Movie Maker. notamment :

-   Tous les points d’entrée vers Windows Movie Maker (par exemple, menu Démarrer, démarrer > exécuter)
-   Tous les fichiers binaires qui ont été utilisés par Windows Movie Maker (tout ce qui se trouvait dans% ProgramFiles% \\ Movie Maker)

Toutefois, les fichiers projet Movie Maker d’un utilisateur restent sur le système et sont accessibles aux autres applications qui prennent en charge ce format de fichier.

## <a name="manifestation"></a>Manifestation

Les résultats de la suppression de Windows Movie Maker sont les suivants :

-   Toute tentative de lancement de Windows Movie Maker avec ses arguments de ligne de commande échoue
-   Tous les plug-ins installés pour activer les nouvelles transformations et les animations restent installés, mais ne sont pas exposés à l’utilisateur final.

## <a name="solution"></a>Solution

Pour que ces fonctionnalités soient à l’avenir, l’utilisateur doit installer une application similaire à partir de Microsoft ou d’un autre fournisseur de logiciels.

 

 



