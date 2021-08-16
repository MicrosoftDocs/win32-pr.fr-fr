---
description: Commandes de DVD
ms.assetid: 1204c73e-c3de-4488-8ee3-e76edbf72da0
title: Commandes de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02f9c0b6a50b6d7eb67832286ee980b0faf69460621a46caf98089efc24b19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820583"
---
# <a name="dvd-commands"></a>Commandes de DVD

les commandes de navigation et de lecture de dvd sont définies dans une section de la spécification de dvd nommée annexe J, ce qui explique pourquoi la documentation DirectShow fait souvent référence à « l’annexe j commands ». toutefois, les noms fournis à l’annexe J ne sont pas toujours très intuitifs, DirectShow utilise donc des noms qui peuvent être plus faciles à comprendre.

le tableau suivant répertorie les commandes de l’annexe J et leurs DirectShow équivalents.



| Commande Annexe J                                                                           | Description                                                                  | Méthode IDvdControl2                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Lecture du titre \_                                                                               | Lire un titre.                                                                | [**PlayTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| PTT \_ Play                                                                                 | Lire un chapitre dans un titre.                                                   | [**PlayChapterInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| Durée de \_ lecture                                                                                | Lire un titre à partir d’une heure spécifiée.                                 | [**PlayAtTimeInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| Arrêter                                                                                      | Arrêter la lecture.                                                               | [**Erreur**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| GoUp                                                                                      | Revenir d’un sous-menu au menu parent.                                    | [**ReturnFromSubmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| Recherche de temps \_                                                                              | Lire à une heure spécifiée dans le titre actuel.                           | [**PlayAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| \_Recherche PTT                                                                               | Lisez un chapitre dans le titre actuel.                                     | [**PlayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| \_Recherche PrevPG                                                                            | Accédez au début du chapitre précédent et reprenez la lecture.                 | [**PlayPrevChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| \_Recherche TopPG                                                                             | Accédez au début du chapitre actuel et reprenez la lecture.                  | [**ReplayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| \_Recherche NextPG                                                                            | Accédez au début du chapitre suivant et reprenez la lecture.                     | [**PlayNextChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| Analyser vers l’avant \_                                                                             | Lire vers l’avant à un taux de lecture spécifié. La vitesse de lecture par défaut est 1,0. | [**PlayForwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| Analyse vers l’arrière \_                                                                            | Lire vers l’arrière à un taux de lecture spécifié.                                  | [**PlayBackwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| Appel de menu \_                                                                                | Afficher un menu.                                                                 | [**ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| Reprendre                                                                                    | Revenir à partir d’un menu et reprendre la lecture.                                      | [**Reprendre**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| Bouton supérieur, sélectionner, bouton \_ \_ inférieur, sélectionner, \_ \_ \_ bouton gauche, sélectionner le bouton \_ droit \_ \_ | Sélectionnez un bouton dont la position est relative au bouton actuellement sélectionné. | [**SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| Bouton \_ activer                                                                          | Activez le bouton sélectionné.                                                | [**ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| \_Sélectionner \_ et \_ activer le bouton                                                             | Sélectionnez et activez un bouton.                                                | [**SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| Toujours \_ désactivé                                                                                | Reprendre la lecture lors de l’affichage d’une image continue.                               | [**StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| Suspendre \_ le                                                                                 | Suspendre la lecture.                                                              | [**Suspendre**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Suspendre \_                                                                                | Reprendre la lecture à partir de l’état suspendu.                                       | [**Suspendre**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Sélection de la langue du menu \_ \_                                                                    | Sélectionnez la langue des menus.                                               | [**SelectDefaultMenuLanguage**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| \_Modification du flux audio \_                                                                     | Définit le flux audio.                                                        | [**SelectAudioStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| Modification du flux de sous-image \_ \_                                                               | Définir le flux de sous-image ; activez ou désactivez l’affichage des sous-images.             | [**SelectSubpictureStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| Changement d’angle \_                                                                             | Définissez l’angle de la caméra.                                                        | [**SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| \_Sélection du niveau parental \_                                                                   | Définissez le niveau parental.                                                      | [**SelectParentalLevel**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| \_Sélection du pays parental \_                                                                 | Définissez le pays ou la région pour la gestion parentale.                              | [**SelectParentalCountry**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| \_Modification du \_ mode de présentation audio \_ karaoké \_                                                | Définissez le mode de mixage audio pour Karaoke.                                       | [**SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| \_Changement du \_ mode de présentation vidéo \_                                                         | Définissez le mode proportions sur grand écran, bandes noires ou analyse panoramique.             | [**SelectVideoModePreference**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



