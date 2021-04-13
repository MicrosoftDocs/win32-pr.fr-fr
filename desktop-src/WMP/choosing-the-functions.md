---
title: Choix des fonctions
description: Choix des fonctions
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Windows Media Player Mobile Skins, fonctions pour l’audio
- Skins, fonctions pour l’audio
- création d’apparences, fonctions pour l’audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380295"
---
# <a name="choosing-the-functions"></a>Choix des fonctions

L’objectif de cette apparence est de fournir des fonctionnalités de base pour la lecture audio. Les fonctions suivantes sont utilisées :



| Fonction                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PlayPause ou PlayPauseStop\* | Le démarrage de l’élément multimédia est de première importance. Si vous créez une apparence pour Windows Media Player 10 mobile ou version ultérieure, vous devez utiliser PlayPauseStop. Si vous utilisez une version antérieure du lecteur Windows Media Mobile, vous devez utiliser PlayPause. Les deux fonctions vous offrent les fonctionnalités supplémentaires de pause, mais seules les PlayPauseStop vous permettent d’arrêter une diffusion en direct lorsque la fonctionnalité de pause n’est pas disponible. |
| Arrêter                         | Vous pouvez ajouter arrêter pour arrêter la diffusion de l’élément. Si vous créez une apparence pour Windows Media Player 10 mobile ou version ultérieure, la fonction PlayPauseStop fournit déjà cette fonctionnalité.                                                                                                                                                                                                                                          |
| Suivant                         | Si vous avez une sélection, vous pouvez choisir l’élément suivant. Vous en avez besoin pour une navigation de base sur les médias numériques.                                                                                                                                                                                                                                                                                                       |
| Précédent                         | Si vous pouvez utiliser Next pour parcourir la sélection jusqu’au début, l’ajout de PREV permettra à l’utilisateur de revenir en arrière et de transférer facilement lors de la navigation dans la sélection.                                                                                                                                                                                                                                   |
| VolumeUp ou VolumeDown\*     | Vous pouvez fournir à l’utilisateur la possibilité d’activer ou de désactiver le volume.                                                                                                                                                                                                                                                                                                                                                    |



 

\*Disponible pour Windows Media Player 10 mobile ou version ultérieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Repère d’apparence**](skin-guide.md)
</dt> </dl>

 

 




