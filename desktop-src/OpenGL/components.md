---
title: Components
description: Composants
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL sur Windows, composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11c8d23130393102f39b716e16c0a6433a40122ad176a525b40e2e1a21b0360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868779"
---
# <a name="components"></a>Composants

l’implémentation de OpenGL par Microsoft dans Windows comprend les composants suivants :

-   Ensemble complet des commandes OpenGL actuelles

    OpenGL contient une bibliothèque de fonctions principales pour les opérations de graphiques 3D. Ces fonctions de base sont utilisées pour gérer la description de la forme de l’objet, la transformation de matrice, l’éclairage, la coloration, la texture, le découpage, les bitmaps, le brouillard et l’anticrénelage. Les noms de ces fonctions principales ont un préfixe « GL ».

    La plupart des commandes OpenGL ont plusieurs variantes, qui diffèrent du nombre et du type de leurs paramètres. En comptant toutes les variantes, il y a plus de 300 commandes OpenGL.

-   La bibliothèque OpenGL Utility (GLU)

    Cette bibliothèque de fonctions auxiliaires complète les fonctions OpenGL principales. Les commandes gèrent la prise en charge de la texture, la transformation des coordonnées, le pavage polygonal, les sphères de rendu, les cylindres et les disques, les courbes et les surfaces NURBS (non-uniform rational B-spline) et la gestion des erreurs.

-   Bibliothèque auxiliaire du Guide de programmation OpenGL

    Il s’agit d’une bibliothèque simple, indépendante de la plate-forme, de fonctions pour gérer Windows, gérer des événements d’entrée, dessiner des objets 3D classiques, gérer un processus en arrière-plan et exécuter un programme. Les routines de gestion et d’entrée des fenêtres fournissent un niveau de base de fonctionnalité qui vous permet de commencer rapidement la programmation dans OpenGL.

    Toutefois, ne les utilisez pas dans une application de production. Voici quelques raisons pour cet avertissement :

    -   La boucle de message se trouve dans le code de la bibliothèque.
    -   Il n’existe aucun moyen d’ajouter des gestionnaires pour des \* messages WM supplémentaires.
    -   Il y a très peu de prise en charge des palettes logiques.

    La bibliothèque est décrite et utilisée dans le *Guide de programmation OpenGL*.

-   Fonctions WGL

    cet ensemble de fonctions connecte OpenGL au système de fenêtrage Windows. Les fonctions gèrent les contextes de rendu, les listes d’affichage, les fonctions d’extension et les bitmaps de police. Les fonctions WGL sont analogues aux extensions GLX qui connectent OpenGL au système de fenêtres X. Les noms de ces fonctions ont un préfixe « WGL ».

-   nouvelles fonctions de Windows pour les formats de pixel et la double mise en mémoire tampon

    Ces fonctions prennent en charge les formats de pixel par fenêtre et la double mise en mémoire tampon (pour les modifications d’images lisses) de Windows. Ces nouvelles fonctions s’appliquent uniquement aux fenêtres graphiques OpenGL.

 

 




