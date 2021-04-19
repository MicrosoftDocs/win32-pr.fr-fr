---
title: Entrée de la souris (prise en main de Win32 et C++)
description: Entrée de la souris
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509483"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>Entrée de la souris (prise en main de Win32 et C++)

Windows prend en charge la souris avec un maximum de cinq boutons : gauche, milieu et droite, ainsi que deux autres boutons appelés le bouton XButton1 et XBUTTON2.

![illustration qui montre les boutons gauche (1), droite (2), milieu (3) et le bouton XButton1 (4).](images/mouse.png)

La plupart des souris pour Windows ont au moins les boutons gauche et droit. Le bouton gauche de la souris est utilisé pour le pointage, la sélection, le glissement, etc. Le bouton droit de la souris affiche généralement un menu contextuel. Certaines souris disposent d’une roulette de défilement située entre les boutons gauche et droit. Selon la souris, la roulette de défilement peut également être cliquable, ce qui en fait le bouton central.

Les boutons le bouton XButton1 et XBUTTON2 sont souvent situés sur les côtés de la souris, près de la base. Ces boutons supplémentaires ne sont pas présents sur toutes les souris. S’il est présent, les boutons le bouton XButton1 et XBUTTON2 sont souvent mappés à une fonction d’application, telle que la navigation vers l’avant et vers l’arrière dans un navigateur Web.

Les utilisateurs de gauche trouvent souvent plus à l’aise pour échanger les fonctions des boutons gauche et droit, en utilisant le bouton droit comme pointeur et le bouton gauche pour afficher le menu contextuel. Pour cette raison, la documentation d’aide de Windows utilise le *bouton principal* termes et le *bouton secondaire*, qui font référence à la fonction logique plutôt qu’à l’emplacement physique. Dans le paramètre par défaut (droitier), le bouton gauche est le bouton principal et la droite est le bouton secondaire. Toutefois, les conditions de clic droit et de *clic* *droit* font référence aux actions logiques. *Cliquez avec le bouton droit* sur le bouton principal, que ce bouton se trouve physiquement à droite ou à gauche de la souris.

Quelle que soit la façon dont l’utilisateur configure la souris, Windows convertit automatiquement les messages de la souris afin qu’ils soient cohérents. L’utilisateur peut échanger les boutons principal et secondaire au milieu de l’utilisation de votre programme, et il n’a aucune incidence sur le comportement de votre programme.

La documentation MSDN utilise le bouton *droit* et le bouton *gauche* pour signifier les boutons *principal* et *secondaire* . Cette terminologie est cohérente avec les noms des messages de fenêtre pour l’entrée de la souris. Rappelez-vous simplement que les boutons physiques gauche et droit peuvent être permutés.

## <a name="next"></a>Suivant

[Réponse aux clics de souris](mouse-clicks.md)

 

 




