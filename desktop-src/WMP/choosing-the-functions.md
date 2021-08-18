---
title: Choix des fonctions
description: Choix des fonctions
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Lecteur Windows Media Skins mobiles, fonctions pour l’audio
- Skins, fonctions pour l’audio
- création d’apparences, fonctions pour l’audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222a7a6b26b225b0c40e461833f731c477c84338c458f88074fd747c33a1e70e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119831"
---
# <a name="choosing-the-functions"></a>Choix des fonctions

L’objectif de cette apparence est de fournir des fonctionnalités de base pour la lecture audio. Les fonctions suivantes sont utilisées :



| Fonction                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PlayPause ou PlayPauseStop\* | Le démarrage de l’élément multimédia est de première importance. si vous créez une apparence pour Lecteur Windows Media 10 Mobile ou version ultérieure, vous devez utiliser PlayPauseStop. si vous utilisez une version antérieure de Lecteur Windows Media Mobile, vous devez utiliser PlayPause. Les deux fonctions vous offrent les fonctionnalités supplémentaires de pause, mais seules les PlayPauseStop vous permettent d’arrêter une diffusion en direct lorsque la fonctionnalité de pause n’est pas disponible. |
| Arrêter                         | Vous pouvez ajouter arrêter pour arrêter la diffusion de l’élément. si vous créez une apparence pour Lecteur Windows Media 10 Mobile ou version ultérieure, la fonction PlayPauseStop fournit déjà cette fonctionnalité.                                                                                                                                                                                                                                          |
| Suivant                         | Si vous avez une sélection, vous pouvez choisir l’élément suivant. Vous en avez besoin pour une navigation de base sur les médias numériques.                                                                                                                                                                                                                                                                                                       |
| Précédent                         | Si vous pouvez utiliser Next pour parcourir la sélection jusqu’au début, l’ajout de PREV permettra à l’utilisateur de revenir en arrière et de transférer facilement lors de la navigation dans la sélection.                                                                                                                                                                                                                                   |
| VolumeUp ou VolumeDown\*     | Vous pouvez fournir à l’utilisateur la possibilité d’activer ou de désactiver le volume.                                                                                                                                                                                                                                                                                                                                                    |



 

\*disponible pour Lecteur Windows Media 10 Mobile ou version ultérieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Repère d’apparence**](skin-guide.md)
</dt> </dl>

 

 




