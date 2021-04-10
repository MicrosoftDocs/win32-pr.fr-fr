---
description: Les terminaux de fichiers peuvent être utilisés de deux manières.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Utilisation des terminaux de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115810"
---
# <a name="using-file-terminals"></a>Utilisation des terminaux de fichiers

Les terminaux de fichiers peuvent être utilisés de deux manières. La méthode la plus simple consiste à utiliser [**ITBasicCallControl2 :: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) pour sélectionner un terminal de fichiers (lecture ou enregistrement) sur un objet d’appel TAPI. Dans ce cas, l’interface TAPI prend en charge la connexion des flux audio aux terminaux de suivi.

La deuxième méthode permet à une application d’avoir un contrôle plus fin sur le mappage des flux audio à des pistes. Dans ce scénario, l’application énumère les flux disponibles sur l’appel, sélectionne ceux qu’elle souhaite enregistrer (ou utiliser pour la lecture), crée (ou recherche) les pistes correspondantes sur le terminal de fichiers et sélectionne les pistes sur les flux d’appels.

Pour plus d'informations, voir les rubriques suivantes :

-   [Lecture simple](simple-playback.md)
-   [Lecture contrôlée par le suivi](track-controlled-playback.md)
-   [Enregistrement simple](simple-record.md)
-   [Enregistrement contrôlé par suivi](track-controlled-record.md)

 

 



