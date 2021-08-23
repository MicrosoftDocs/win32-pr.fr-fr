---
title: remplacement de l’Application de visionneuse d’images et de télécopies Windows à l’aide du verbe Preview
description: à partir de Windows XP, les utilisateurs peuvent afficher, faire pivoter, imprimer et zoomer des images.
ms.assetid: cb08756b-6a5d-424d-ab6d-2e34d180ec4e
keywords:
- Windows Visionneuse d’images et de télécopies
- Verbe d’aperçu
- meilleures pratiques, Windows visionneuse d’images et de télécopies
- meilleures pratiques, verbe preview
- performances, Windows visionneuse d’images et de télécopies
- performances, verbe preview
- inscrire, verbe preview
- inscrire, verbe de diaporama
- Verbe de diaporama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518e32f7b7bf33db26e534c92cfe2fb46c9a51bc444f04f4881f18fb1fe6c738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608519"
---
# <a name="replacing-the-windows-picture-and-fax-viewer-application-using-the-preview-verb"></a>remplacement de l’Application de visionneuse d’images et de télécopies Windows à l’aide du verbe Preview

\[la fonctionnalité visionneuse d’images et de télécopies est prise en charge uniquement sous Windows XP. \]

à partir de Windows XP, les utilisateurs peuvent afficher, faire pivoter, imprimer et zoomer des images. certaines de ces fonctionnalités sont fournies via l’interpréteur de commandes Windows, et d’autres par le biais de l’application de visionneuse d’images et de télécopies Windows. bien que Windows visionneuse d’images et de télécopies offre une excellente base des fonctionnalités et constitue une partie essentielle de l’expérience d’acquisition d’images, si vous le souhaitez, vous pouvez facilement la remplacer par une autre application. ce document est conçu pour vous aider à remplacer efficacement l’Windows application de visionneuse d’images et de télécopies sans perdre les fonctionnalités importantes ou dégrader l’expérience utilisateur.

-   [Bonnes pratiques](#best-practices)
    -   [Performances](#performance)
    -   [Caractéristiques](#features)
    -   [Prise en charge du format](#format-support)
-   [Inscription pour le verbe preview](#registering-for-the-preview-verb)
-   [Inscription pour le verbe Edit](#registering-for-the-edit-verb)
-   [Inscription pour le verbe de diaporama](#registering-for-the-slideshow-verb)
-   [Rubriques connexes](#related-topics)

## <a name="best-practices"></a>Meilleures pratiques

dans Windows XP et versions ultérieures, l’interpréteur de commandes comprend un verbe que vous pouvez utiliser pour permettre aux utilisateurs d’afficher un aperçu des images. Elle est appelée *Aperçu*. Ce verbe met en surbrillance la tâche principale de l’utilisateur pour les images, qui affiche. pour que cette expérience fonctionne bien, le Windows application de visionneuse d’images et de télécopies est propriétaire de l’association d’aperçu par défaut.

la Windows visionneuse d’images et de télécopies, ou toute application qui possède une association de fichiers, comprend un élément qui lance l’application de modification de l’utilisateur. Étant donné que le verbe Preview est utilisé uniquement pour afficher un aperçu des images au lieu de les modifier, votre application doit faire attention à suivre les recommandations de ce document lors de la revendication de cette association.

Vous voulez vous assurer qu’une application qui modifie des images peut toujours prendre le verbe Edit. Par exemple, si un utilisateur dispose de Microsoft Picture It ! installé, lorsqu’ils double-cliquent sur un fichier .jpg l’ordinateur doit lancer l’application de visionneuse d’images et de télécopies Windows. Toutefois, lorsqu’ils cliquent sur **modifier** dans la barre d’outils, l’ordinateur doit lancer Picture It ! avec ce .jpg fichier.

il y a trois considérations à prendre en compte lorsque vous remplacez la Windows visionneuse d’images et de télécopies. Les voici :

-   [Performances](#performance)
-   [Caractéristiques](#features)
-   [Prise en charge du format](#format-support)

### <a name="performance"></a>Performances

Le principal facteur à prendre en compte en matière de performances est la vitesse à laquelle les images sont chargées. bien qu’aucune mesure de performance ne soit fournie ici, vous devez essayer de remplacer Windows visionneuse d’images et de télécopies par une application qui correspond ou augmente les performances.

L’application elle-même doit se charger rapidement. L’un des principaux problèmes rencontrés par les utilisateurs avec les applications qui prennent les associations d’images est le temps d’attente pendant le chargement de l’application. Il s’agit souvent d’une charge d’application de modification puissante lorsqu’ils double-cliquent sur un fichier image, même lorsque l’utilisateur souhaite simplement afficher le fichier. Il vaut mieux pour l’utilisateur si vous fournissez des options qui l’emportent rapidement dans une application où il peut modifier l’image uniquement quand c’est le cas.

### <a name="features"></a>Fonctionnalités

il existe un ensemble minimal de fonctionnalités que votre application doit fournir lorsque vous remplacez l’Windows application visionneuse d’images et de télécopies. Les voici :



| Caractéristique                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Afficher l’image au mieux             | Cela donne à l’utilisateur la possibilité de voir la totalité de l’image mise à l’échelle jusqu’à la taille la plus adaptée à l’espace affichable dans la fenêtre de l’application. De cette façon, ils peuvent voir l’image entière, même si elle est légèrement détériorée par un zoom arrière. Il doit s’agir du paramètre par défaut chaque fois qu’un chargement d’image est plus grand que l’espace affichable. Dans le cas contraire, l’image doit apparaître dans sa taille réelle. Par exemple, une image 64 x 64 pixels ne doit pas être mise à l’échelle vers une taille de 600 x 600, simplement parce qu’il s’agit de la taille de la fenêtre de l’application. |
| Afficher l’image à la taille réelle          | Cela donne à l’utilisateur la possibilité de voir la totalité de l’image à sa résolution réelle. Cela leur permet de les afficher à la taille et au panoramique appropriés sur l’image. Il ne doit pas s’agir de l’affichage par défaut, sauf si l’image est plus petite que l’espace affichable dans l’application.                                                                                                                                                                                                                                                              |
| Zoom sur l’image                    | Cela permet à l’utilisateur d’effectuer un zoom sur une partie de l’image pour examiner plus précisément les détails ou simplement agrandir une petite image. Cela est similaire à l’affichage de la taille réelle de l’image, mais permet à l’utilisateur de contrôler le degré d’affichage de l’image.                                                                                                                                                                                                                                                                                            |
| Zoom arrière sur l’image                  | Cela permet à l’utilisateur d’effectuer un zoom arrière et d’obtenir une vue plus large. Cela est similaire à l’affichage de l’image au mieux, mais elle permet à l’utilisateur de contrôler à quel moment ils affichent l’image.                                                                                                                                                                                                                                                                                                                                                          |
| Image suivante                         | Cela permet à l’utilisateur de voir l’image suivante dans la liste. Cette liste peut être toutes les images dans le dossier actif ou toutes les images que l’utilisateur sélectionne dans le cadre d’une opération de multisélection ; autrement dit, lorsqu’il clique dessus et le fait glisser pour mettre en surbrillance des images ou maintient le bouton de contrôle enfoncé et clique sur des fichiers individuels.                                                                                                                                                                                                                       |
| Image précédente                     | Cela permet à l’utilisateur d’afficher l’image précédente dans la liste.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Rotation dans le sens des aiguilles d’une montre 90 degrés        | Cela permet à l’utilisateur de faire pivoter l’image dans le sens des aiguilles d’une montre. Windows XP enregistre automatiquement l’image lorsqu’il la fait pivoter pour réduire la perte de qualité d’image. L’application peut également faire pivoter des incréments plus petits, mais 90 degrés est la norme de rotation la plus courante pour les images numériques.                                                                                                                                                                                                                                 |
| Faire pivoter à gauche de 90 degrés | Cela permet à l’utilisateur de faire pivoter l’image dans le sens inverse des quarts.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Imprimer                              | Cela permet à l’utilisateur d’imprimer l’image qui s’affiche actuellement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Enregistrer sous                            | Cela permet à l’utilisateur d’enregistrer l’image dans un dossier spécifié.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Supprimer l’image                       | Cela permet à l’utilisateur de supprimer l’image.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Aide                               | Cela permet à l’utilisateur de fournir une documentation d’aide en ce qui concerne l’utilisation de l’application de visualisation.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Propriétés                         | Cela permet à l’utilisateur d’afficher ou de modifier les propriétés de l’image, en général les informations EXIF (Exchangeable Image File) stockées dans chaque image.                                                                                                                                                                                                                                                                                                                                                                                      |
| Modifier                               | Cela permet à l’utilisateur de lancer son programme d’édition préféré inscrit pour le verbe Edit sur l’image.                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="format-support"></a>Prise en charge du format

étant donné qu’il est difficile pour une application de prendre en charge toutes les différentes images, il est recommandé que l’application utilise Windows GDI+ pour prendre en charge les formats d’image. toutefois, si vous choisissez de ne pas utiliser GDI+, votre application ne doit prendre en charge que les associations de fichiers pour lesquelles elle a été testée et est connue pour fonctionner. ensuite, si l’utilisateur doit afficher un format que vous ne gérez pas, Windows visionneuse d’images et de télécopies peut toujours fournir l’accès.

par exemple, Windows visionneuse d’images et de télécopies fournit un certain nombre d’outils permettant de modifier des annotations dans des images. tiff. À moins que cette fonctionnalité ne soit dupliquée dans votre application, vous ne devez pas inscrire votre application pour gérer les images. TIFF. Le principe de conduite doit être de s’assurer que l’utilisateur ne perd aucune fonctionnalité.

## <a name="registering-for-the-preview-verb"></a>Inscription pour le verbe preview

L’inscription d’une application pour gérer le verbe Preview est relativement simple. Localisez la valeur suivante de l’application dans le registre, où application. jpeg représente le nom de la clé d’association de fichiers de l’application (pour plus d’informations, consultez [programmes par défaut](/windows/desktop/shell/default-programs) ) :

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         open
            command
               (Default) = app.exe %1
```

Remplacez le nom de la sous-clé **ouverte** par « Preview », comme illustré ici.

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         preview
            command
               (Default) = app.exe %1
```

Cette opération inscrit l’application et en fait l’application par défaut pour le verbe de préversion d’un fichier .jpg. Les éléments suivants sont également requis.

**HKEY \_ CLASSES \_ racine** \\ **.jpg** \( par défaut) = application. jpeg

## <a name="registering-for-the-edit-verb"></a>Inscription pour le verbe Edit

Cela enregistre une application pour le verbe Edit et en fait la nouvelle application par défaut pour la modification d’une image. L’application inscrite doit prendre en charge la fonctionnalité de modification de l’application par défaut existante à l’heure de l’installation et l’installer à nouveau en tant que gestionnaire au moment de la désinstallation. Pour ce faire, vous devez inscrire la nouvelle application plus bas dans la liste d’associations que celle de l’application par défaut. L’application par défaut est inscrite ici :

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      image
         shell
            edit
               command
                  (Default) = app.exe %1
```

La nouvelle application doit s’inscrire ici :

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         edit
            command
               (Default) = app.exe %1
```

## <a name="registering-for-the-slideshow-verb"></a>Inscription pour le verbe de diaporama

à partir de Windows Vista, une application peut également inscrire le verbe de **diaporama** . Les applications qui implémentent un diaporama peuvent s’inscrire pour être appelées lorsque le verbe de diaporama est choisi. Cette inscription s’effectue exactement de la même manière, comme expliqué pour le verbe Preview ci-dessus. Il est fortement recommandé que les applications implémentent la forme DropTarget du verbe. De cette façon, il est possible de passer un ensemble complet d’éléments. L’implémentation de DropTarget est inscrite comme indiqué ici :

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         slideshow
            DropTarget
               CLSID = {CLSID of the implementation}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation des associations de fichiers](/windows/desktop/shell/fa-intro)
</dt> <dt>

[À propos de GDI+](../gdiplus/-gdiplus-about-gdi--about.md)
</dt> </dl>

 

 