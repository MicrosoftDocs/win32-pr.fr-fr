---
description: suppression de Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: suppression de Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538032d589439ccc0966bc151568813eed3d1946cd2cb8ea7d9314246edb19ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098519"
---
# <a name="removal-of-windows-movie-maker"></a>suppression de Windows Movie Maker

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -haute  
**Fréquence** -moyenne  


## <a name="description"></a>Description

Microsoft déprécie et supprime l’utilitaire Windows Movie Maker. notamment :

-   tous les points d’entrée pour Windows Movie Maker (par exemple, Menu démarrer, démarrer > exécuter)
-   tous les fichiers binaires qui ont été utilisés par Windows movie maker (tout ce qui se trouvait dans% ProgramFiles% \\ Movie maker)

Toutefois, les fichiers projet Movie Maker d’un utilisateur restent sur le système et sont accessibles aux autres applications qui prennent en charge ce format de fichier.

## <a name="manifestation"></a>Manifestation

la suppression de Windows Movie Maker produit les résultats suivants :

-   toute tentative de lancement d’Windows Movie Maker avec ses arguments de ligne de commande échoue
-   Tous les plug-ins installés pour activer les nouvelles transformations et les animations restent installés, mais ne sont pas exposés à l’utilisateur final.

## <a name="solution"></a>Solution

Pour que ces fonctionnalités soient à l’avenir, l’utilisateur doit installer une application similaire à partir de Microsoft ou d’un autre fournisseur de logiciels.

 

 



