---
title: Conception de l’interface
description: Conception de l’interface
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Windows Media Player Mobile Skins, interfaces utilisateur
- apparences, interfaces utilisateur
- création d’apparences, d’interfaces utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8070ef6fd4589f762624d7a0b5ee1d380a264066
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100773"
---
# <a name="designing-the-interface"></a>Conception de l’interface

Une fois les fonctions choisies, l’interface peut être conçue. Une interface simple a été choisie pour correspondre à la fonctionnalité. Les symboles des contrôles ont été choisis dans les contrôles de magnétoscope standard.

L’illustration suivante montre à quoi ressemblera l’interface.

![exemple d’interface](images/ceswmful.png)

-   **Bouton PlayPause ou PlayPauseStop.** L’utilisateur aura le plus de toucher, donc vous pouvez envisager un plus grand bouton. L’angle supérieur droit constitue un bon emplacement que l’utilisateur peut trouver rapidement. Une flèche pleine est utilisée pour indiquer que la lecture et les deux barres verticales (qui ne sont pas affichées ici) seront utilisées pour indiquer une pause.
    > [!Note]  
    > Le bouton PlayPauseStop peut uniquement être utilisé lors de la création d’une apparence pour le lecteur Windows Media 10 mobile ou version ultérieure.

     

-   **Bouton arrêter.** Pour faciliter la recherche, elle est placée dans l’angle supérieur gauche. Un carré est utilisé pour indiquer l’arrêt. Si vous créez une apparence pour Windows Media Player 10 mobile ou version ultérieure, le bouton PlayPauseStop fournit déjà cette fonctionnalité.
-   **Boutons suivant et préc.** Étant donné qu’elles ne seront pas utilisées aussi souvent, elles sont placées sur la gauche. Le suivant se trouve au-dessus du bouton précédent, car il est plus probable que les utilisateurs veulent avancer dans une sélection. Les symboles à deux flèches sont utilisés, car ils sont similaires en fonction d’un contrôle d’avance rapide.
-   **TrackBar du volume.** Il est placé en bas de l’écran et il s’agit d’une simple ligne avec un bouton Thumb.
-   **Zone de texte de texte défilant.** Elle est placée sous le bouton PlayPause ou PlayPauseStop pour qu’elle soit facile à voir.

Vous pouvez le faire tout d’abord et expérimenter le placement de chaque élément d’interface utilisateur. La conception présentée ici a été choisie pour des raisons de simplicité et de facilité d’utilisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Repère d’apparence**](skin-guide.md)
</dt> </dl>

 

 




