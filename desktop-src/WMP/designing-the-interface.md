---
title: Conception de l’interface
description: Conception de l’interface
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Lecteur Windows Media Skins mobiles, interfaces utilisateur
- apparences, interfaces utilisateur
- création d’apparences, d’interfaces utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b11dee2a6236f2a279756644a88d69e267c5da93240b5e12c19c32d86e30a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749859"
---
# <a name="designing-the-interface"></a>Conception de l’interface

Une fois les fonctions choisies, l’interface peut être conçue. Une interface simple a été choisie pour correspondre à la fonctionnalité. Les symboles des contrôles ont été choisis dans les contrôles de magnétoscope standard.

L’illustration suivante montre à quoi ressemblera l’interface.

![exemple d’interface](images/ceswmful.png)

-   **Bouton PlayPause ou PlayPauseStop.** L’utilisateur aura le plus de toucher, donc vous pouvez envisager un plus grand bouton. L’angle supérieur droit constitue un bon emplacement que l’utilisateur peut trouver rapidement. Une flèche pleine est utilisée pour indiquer que la lecture et les deux barres verticales (qui ne sont pas affichées ici) seront utilisées pour indiquer une pause.
    > [!Note]  
    > le bouton PlayPauseStop peut uniquement être utilisé lors de la création d’une apparence pour Lecteur Windows Media 10 Mobile ou version ultérieure.

     

-   **Bouton arrêter.** Pour faciliter la recherche, elle est placée dans l’angle supérieur gauche. Un carré est utilisé pour indiquer l’arrêt. si vous créez une apparence pour Lecteur Windows Media 10 Mobile ou version ultérieure, le bouton PlayPauseStop fournit déjà cette fonctionnalité.
-   **Boutons suivant et préc.** Étant donné qu’elles ne seront pas utilisées aussi souvent, elles sont placées sur la gauche. Le suivant se trouve au-dessus du bouton précédent, car il est plus probable que les utilisateurs veulent avancer dans une sélection. Les symboles à deux flèches sont utilisés, car ils sont similaires en fonction d’un contrôle d’avance rapide.
-   **TrackBar du volume.** Il est placé en bas de l’écran et il s’agit d’une simple ligne avec un bouton Thumb.
-   **Zone de texte de texte défilant.** Elle est placée sous le bouton PlayPause ou PlayPauseStop pour qu’elle soit facile à voir.

Vous pouvez le faire tout d’abord et expérimenter le placement de chaque élément d’interface utilisateur. La conception présentée ici a été choisie pour des raisons de simplicité et de facilité d’utilisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Repère d’apparence**](skin-guide.md)
</dt> </dl>

 

 




