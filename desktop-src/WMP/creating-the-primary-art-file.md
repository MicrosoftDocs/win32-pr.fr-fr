---
title: Création du fichier art principal
description: Création du fichier art principal
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- création d’apparences, de fichiers art primaires
- Apparences du lecteur Windows Media, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, images principales
- Apparences du lecteur Windows Media, images principales
- apparences, images principales
- images principales dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104568893"
---
# <a name="creating-the-primary-art-file"></a>Création du fichier art principal

Le fichier art principal contiendra l’illustration que l’utilisateur de votre Skin voit d’abord. Dans ce cas, vous allez créer des images dans différentes couches de votre programme art. La raison de l’utilisation des couches est que vous copierez ultérieurement des couches spécifiques pour créer des fichiers de mappage et des fichiers d’art alternatifs.

Pour créer le fichier art principal, vous allez créer les couches suivantes dans l’ordre suivant :

Couche d’arrière-plan de l’apparence

Il s’agit de la couleur qui sera transparente lorsque l’apparence sera affichée. Créez d’abord une couche pour cette couche, mais choisissez la couleur finale de cette couche après avoir choisi une couleur pour la couche de conteneur d’apparences. Cette couleur doit être semblable à, mais pas à la couche du conteneur d’apparences, pour masquer les effets d’anticrénelage.

Couche de conteneur d’apparence

Il s’agit de l’image qui formera le contour de votre apparence et sera ce que l’utilisateur voit. Il s’agit également du conteneur pour les deux boutons de cet exemple. Imaginez votre apparence comme un conteneur pour les contrôles d’interface utilisateur, tels que les boutons, les curseurs, etc. Dans cet exemple, le conteneur est une ellipse jaune.

Calques de bouton lire et fermer

Il s’agit des deux contrôles d’interface utilisateur que cet exemple utilise. Vous allez les placer dans des couches distinctes afin de pouvoir les ajuster facilement ou les copier ultérieurement.

Avant de créer vos couches, vous devez créer le fichier qui contiendra vos couches. Démarrez Photoshop et créez un nouveau fichier de 100 pixels de haut et 200 pixels de large. Le fichier utilisé pour créer l’illustration de cet exemple est appelé tiny.psd et est inclus dans le kit de développement logiciel (SDK).

Toutes les instructions sont fournies en termes de Photoshop, mais tout autre programme artistique peut être utilisé pour créer des apparences tant que vous pouvez les enregistrer dans l’un des formats de fichier pris en charge par le lecteur Windows Media (BMP, GIF, JPG et PNG). La création d’apparences est plus facile si vous utilisez un programme artistique avec des couches, comme Adobe Photoshop, Jasc Paint Shop Pro ou Jedor VISCOSITE. Les couches sont extrêmement utiles, car les images doivent être alignées correctement pour le mappage d’images et l’affichage d’autres images.

## <a name="skin-background-layer"></a>Couche d’arrière-plan de l’apparence

Créez une nouvelle couche et nommez-la « Skin background ». Celle-ci devient la couleur de transparence que vous allez définir dans le fichier de définition d’apparence. Attendez que la couleur du conteneur d’apparence soit choisie avant de remplir la couche d’arrière-plan de l’apparence avec une couleur spécifique.

## <a name="skin-container-layer"></a>Couche de conteneur d’apparence

Créez ensuite une nouvelle couche et nommez-la « conteneur d’apparence ». Cela va définir les bords de votre apparence et sera le conteneur pour les boutons.

Choisissez une couleur de premier plan pour la forme, à l’aide des curseurs de couleur Web. Dans cet exemple, la couleur « \# DBDD11 » a été choisie.

Créez ensuite une forme ovale. Le moyen le plus simple consiste à utiliser l’outil Eliptical Marquee et à créer une sélection ovale. Une fois que vous avez créé une sélection ovale qui correspond à la taille et à la forme souhaitées, remplissez la sélection avec la couleur de premier plan et annulez la sélection.

Enfin, pour que cet aspect soit un peu plus intéressant, appliquez l’effet de couche de biseau et le relief avec les valeurs par défaut.

Votre couche de conteneur d’apparences doit ressembler à l’illustration suivante.

![couche de conteneur d’apparence](images/g01cont.png)

## <a name="background-skin-color"></a>Couleur de l’apparence d’arrière-plan

Maintenant que vous avez choisi une couleur de premier plan pour votre forme de conteneur d’apparences, vous pouvez choisir une couleur similaire pour votre couche d’arrière-plan d’apparence. Vous ne souhaitez pas avoir la même couleur, ou votre conteneur d’apparences sera également transparent. En fait, veillez à ne pas utiliser cette couleur exacte dans votre peau, même dans les photographies, car partout où cette couleur apparaît, l’image de bureau s’affiche à la place.

Vous souhaitez une couleur proche de la couleur du conteneur d’apparences pour éviter les effets d’anticrénelage. Par exemple, si vous avez un arrière-plan noir, certains éléments noirs peuvent s’afficher autour du bord de l’apparence. En choisissant une couleur proche de la couleur du conteneur d’apparences, les pixels isolés qui s’affichent dans le processus d’anticrénelage ne seront pas remarqués.

L’anticrénelage est le processus de lissage des bords des formes inclinées ou courbes. L’anticrénelage crée de nouvelles couleurs, pour les pixels situés le long des bords d’une forme, qui sont une fusion de la couleur de premier plan et la couleur d’arrière-plan. Certaines de ces couleurs entre elles peuvent provoquer l’absence de pixels lorsque la couleur d’arrière-plan est rendue transparente.

Votre couche d’arrière-plan d’apparence doit ressembler à l’illustration suivante.

![couche d’apparence d’arrière-plan](images/g01backg.png)

## <a name="play-and-close-button-layers"></a>Calques de bouton lire et fermer

Créez une nouvelle couche et nommez-la « bouton Fermer ». À l’aide de l’outil Eliptical palissade Selection, créez un cercle et positionnez-le sur le côté gauche de l’image globale. Activez la visibilité du fichier conteneur d’apparence pour vous aider à placer la sélection.

Lorsque vous êtes satisfait du positionnement, remplissez la sélection avec n’importe quelle couleur (à l’exception de la couleur du conteneur d’apparences ou de l’arrière-plan de l’apparence). Dans cet exemple, une couleur violette a été choisie. Vous n’avez pas besoin de vous souvenir du numéro de la couleur. Puis, annulez la sélection et appliquez un autre effet de couche de biseau et de relief par défaut. Si vous souhaitez appliquer des effets non-couche à votre bouton, faites une copie de l’original pour une utilisation ultérieure dans le mappage.

Votre bouton Fermer doit ressembler à l’illustration suivante.

![bouton de fermeture](images/g01qbut.png)

Créez une nouvelle couche et nommez-la « bouton de lecture ». Utilisez les mêmes techniques que celles que vous avez effectuées pour le bouton Fermer, mais donnez-lui une couleur différente. Dans ce cas, une couleur de bouton rose a été choisie, mais toute couleur peut être utilisée tant qu’elle n’est pas de la même couleur que le conteneur d’habillage (car elle se mélange dans le conteneur) ou la couleur d’arrière-plan de l’apparence (car elle devient transparente).

Votre bouton de lecture doit ressembler à l’illustration suivante.

![bouton de lecture](images/g01pbut.png)

## <a name="combine-layers-and-save"></a>Combiner des couches et enregistrer

Vous êtes maintenant prêt à créer le fichier art principal. Masquer toutes les couches, puis afficher uniquement les couches suivantes, dans cet ordre (de haut en bas) :

Bouton de lecture

Bouton Fermer

Conteneur d’apparences

Arrière-plan de la peau

Enregistrez dans un nouveau fichier à l’aide de la commande Enregistrer une copie du menu fichier. Sélectionnez l’option BMP dans la partie enregistrer sous de la boîte de dialogue Enregistrer une copie et tapez un nom de fichier auquel vous allez vous référer ultérieurement dans votre fichier de définition d’apparence. Dans l’idéal, vous devez enregistrer ce fichier dans le même répertoire que votre fichier de définition d’apparence. Par exemple, vous pouvez appeler cette background.bmp. Choisissez les paramètres par défaut et enregistrez le fichier.

Votre fichier art principal doit se présenter comme suit :

![fichier art principal](images/g01prime.png)

Vous utiliserez ce nom de fichier comme valeur pour l’attribut **BackgroundImage** de l’élément **View** dans votre fichier de définition d’apparence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de votre première apparence**](building-your-first-skin.md)
</dt> </dl>

 

 




