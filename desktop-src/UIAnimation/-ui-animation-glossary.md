---
title: Glossaire Windows animation
description: Ce glossaire contient des termes et des acronymes intéressants pour les développeurs qui utilisent le gestionnaire d’animations Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Animation Windows Animation Windows, Glossaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b7f276b0f20efc35057a9ee7c006c3cf170ac3
ms.sourcegitcommit: fdd00b445ee88366e9cdd1eed0cb3e42e2a73eca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104507762"
---
# <a name="windows-animation-glossary"></a>Glossaire Windows animation

Ce glossaire contient des termes et des acronymes intéressants pour les développeurs qui utilisent le gestionnaire d’animations Windows.

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**animation** 
</dt> <dd>

Séquence de synthèse, images continues consécutives qui produisent une illusion de mouvement lors de la lecture.

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**Gestionnaire d’animations** 
</dt> <dd>

Composant principal de Windows animation et interface de programmation centrale pour la gestion (création, planification et contrôle) d’animations.

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**minuteur d’animation**
</dt> <dd>

Composant permettant de fournir des services de minutage qui peuvent être utilisés conjointement avec le gestionnaire d’animations. Il limite de manière dynamique la fréquence d’images en fonction de la charge de l’application et du système ou en mode de faible alimentation. Voir aussi : limitation.

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**variable d’animation** 
</dt> <dd>

Valeur qui peut être animée. Les variables d’animation peuvent être utilisées pour représenter la position, la taille, la rotation, la transparence et d’autres qualités d’objets visibles.

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**Ference**
</dt> <dd>

Processus de suppression d’une table de montage séquentiel de la planification avant son démarrage.

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**compressé**
</dt> <dd>

Déviation du temps d’une table de montage séquentiel. Le système augmente la vitesse à laquelle le Storyboard progresse en passant les valeurs d’heure d’entrée qui augmentent plus rapidement que l’horloge système.

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**achèvement**
</dt> <dd>

Processus de direction d’une table de montage séquentiel pour quitter toutes les boucles indéfinies. Si la boucle a commencé, l’itération en cours se termine et le reste de la table de montage séquentiel est alors lu. Dans le cas contraire, la partie en boucle de la table de montage séquentiel sera ignorée entièrement.

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**Frame** 
</dt> <dd>

Image unique dans un film ou une animation.

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**fréquence d’images** 
</dt> <dd>

Nombre de frames affichés par seconde. Des fréquences d’images supérieures produisent généralement un mouvement plus lisse dans l’image.

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolateur**
</dt> <dd>

Objet de programmation qui effectue l’interpolation mathématique de la valeur et de la vélocité d’une variable pour une transition.

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**image clé**
</dt> <dd>

Un moment dans le temps dans un Storyboard, qui peut être spécifié par rapport au début de la table de montage séquentiel, par rapport à une autre image clé, ou à l’heure de fin d’une transition, et utilisé pour spécifier l’heure de début et de fin d’autres transitions ou d’un cycle dans le Storyboard.

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**circuit**
</dt> <dd>

Section d’un Storyboard entre deux images clés qui est jouée à plusieurs reprises. Une boucle peut jouer un nombre fini de fois ou indéfiniment.

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**comparaison des priorités** 
</dt> <dd>

Code défini par le client qui compare deux storyboards, un qui est déjà planifié et l’autre sur le lieu d’être planifié, pour déterminer leur priorité relative. Une table de montage séquentiel planifiée peut être tronquée, compressée, annulée ou conclue pour permettre la planification de la table de montage séquentiel avec une priorité plus élevée.

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**Storyboard** 
</dt> <dd>

Groupe de transitions d’animation synchronisées les unes par rapport aux autres.

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**balise** 
</dt> <dd>

Paire composée d’un ID d’entier et d’un objet COM utilisé par une application pour identifier des variables d’animation et des storyboards au sein de l’étendue d’un gestionnaire d’animations spécifique.

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**limitation** 
</dt> <dd>

Ajustement dynamique de la fréquence d’images d’une animation pour répondre à certaines exigences. La limitation permet de s’assurer que les animations sont rendues à une fréquence d’images cohérente tout en minimisant l’utilisation des ressources système pour le rendu à une vitesse supérieure à ce qui est nécessaire ou utile.

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**cycle** 
</dt> <dd>

Événement de minuterie qui déclenche généralement le rendu d’un frame unique.

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**transition** 
</dt> <dd>

Construction qui définit des mises à jour progressifs pour une variable d’animation sur une période donnée.

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**limitation**
</dt> <dd>

Préemption du contrôle d’une table de montage séquentiel d’une variable d’animation avec un Storyboard de priorité plus élevée. Si la suppression d’une table de montage séquentiel sur une ou plusieurs variables entraîne la fin prématurée de la table de montage séquentiel, elle est considérée comme tronquée. Voir aussi : troncation.

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**troncation**
</dt> <dd>

Fin prématurée d’une table de montage séquentiel en préemption le contrôle d’une ou plusieurs des variables qu’elle anime avec une ou plusieurs storyboards de priorité supérieure. Voir aussi : suppression.

</dd> </dl>

 

 




