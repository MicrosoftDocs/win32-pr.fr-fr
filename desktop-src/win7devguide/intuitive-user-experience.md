---
title: Expérience utilisateur intuitive
description: pour la première fois, Windows 7 permet aux développeurs et à leurs utilisateurs finaux de contrôler leurs ordinateurs en touchant l’écran.
ms.assetid: cf5be4d6-4284-43e3-86ba-293c4513b477
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76576883186a77c53256dad7f011b75a7e260ae2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219897"
---
# <a name="intuitive-user-experience"></a>Expérience utilisateur intuitive

pour la première fois, Windows 7 permet aux développeurs et à leurs utilisateurs finaux de contrôler leurs ordinateurs en touchant l’écran. Les fonctionnalités tactiles et tactiles multiples offrent un moyen logique et intuitif aux utilisateurs d’interagir avec les PC. La plateforme de développement comprend des API de mouvement de haut niveau, ainsi que des messages tactiles de bas niveau et des API d’entrée tactile. les éléments d’interface utilisateur de niveau supérieur, tels que le menu *démarrer* et la *barre des tâches*, ont des cibles plus importantes que les versions précédentes de Windows, ce qui les rend plus faciles à sélectionner avec un doigt au lieu d’une souris. Des commentaires visuels sont fournis pour TAP et double tap. Windows explorer et Windows Internet explorer 8 sont conviviaux et facilement intégrés aux applications Windows 7.

## <a name="multi-touch-gestures-and-manipulation-and-inertia-apis"></a>Entrées tactiles multiples et API de manipulation et d’inertie

Windows 7 offre une prise en charge améliorée des fonctions tactiles et des gestes, permettant aux développeurs de créer rapidement et facilement des expériences d’application uniques qui vont au-delà du simple pointage de la souris, du clic et du glissement. Les nouvelles API multipoint prennent en charge les gestes riches, tels que le panoramique, le zoom et la rotation. Tous les gestes fournissent des commentaires visuels directs et interagissent avec le contenu sous-jacent de manière naturelle et intuitive. Par exemple, un mouvement de zoom Centre la vue à l’emplacement du mouvement. Les API de saisie tactile de niveau inférieur sont également disponibles pour la définition de mouvements personnalisés et les expériences tactiles avancées. Windows 7 fournit une plateforme de développement qui offre aux développeurs les outils dont ils ont besoin pour développer des applications créatives pour les périphériques d’entrée multipoint, en traitant l’entrée d’utilisateur à partir d’appareils multipoint et en améliorant l’interface utilisateur. Il en résulte des environnements plus intuitifs, qui permettent des innovations en matière d’interaction avec les PC.

Windows 7 fournit également la prise en charge de la plateforme pour le traitement des objets et de l’inertie. Un ensemble complet de fonctions de manipulation vous permet d’étirer, de redimensionner ou de faire pivoter plusieurs objets simultanément et en toute granularité. Par exemple, plusieurs photographies numériques peuvent être rognées, redimensionnées et pivotées dans une seule session à l’aide de gestes tactiles.

Windows 7 comprend des api d’inertie qui simulent l’inertie lorsque les objets sont déplacés, en travaillant à la main avec les api de manipulation. Par exemple, dans une application photo, vous pouvez utiliser les API de manipulation pour permettre aux utilisateurs de faire pivoter, redimensionner et déplacer des photos. De même, si un utilisateur « rejette » une photo, les API d’inertie fournissent une interaction naturelle et permettent à la photo de s’arrêter ou de rebondir sur les bordures de la fenêtre de l’application. (consultez [Windows Guide de programmation tactile](../wintouch/programming-guide.md) et [Windows touch : ressources de développeur](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch).)

## <a name="single-finger-panning"></a>Panoramique Single-Finger

Dans de nombreuses applications courantes, les fonctionnalités tactiles sont plus utiles pour la navigation que pour la sélection de texte. Avec les API tactiles étendues, l’application d’un développeur peut choisir d’activer le panoramique plutôt que de le faire glisser. Par exemple, si vous avez créé une application qui utilise des gestes multipoint pour les utilisateurs qui lisent de la musique, vous pouvez autoriser ces utilisateurs à faire glisser un doigt vers le haut ou vers le haut pour ajuster le volume, changer des chansons ou télécharger un fichier. Aucun défilement n’est requis.

Windows 7 offre des opportunités sans fin aux développeurs désireux de créer des applications pour les pc de nouvelle génération. Mieux encore, il effectue le travail difficile de vérification des barres de défilement et d’implémentation de la sémantique de panoramique. Les applications reçoivent également un ensemble plus riche d’événements et de commentaires pour le contrôle personnalisé des gestes que dans les versions précédentes de Windows. (Voir [amélioration de l’expérience de panoramique Single-Finger](../wintouch/improving-the-single-finger-panning-experience.md).)

## <a name="raw-touch-input-data"></a>Données d’entrée tactile brutes

dans Windows 7, les nouvelles expériences tactiles sont activées par les modèles d’interaction qui accèdent aux messages d’entrée tactile de niveau inférieur et fournissent des réponses personnalisées aux combinaisons de messages tactiles. La plateforme prend en charge la réception de données d’entrée tactile brutes pour des scénarios tels que les applications de peinture multipoint et les gestes personnalisés au sein d’une application. Vous pouvez utiliser la prise en charge des plateformes tactiles ou créer vos propres expériences tactiles originales. (Consultez [ \_ message WM Touch](../wintouch/wm-touchdown.md).)

 

 