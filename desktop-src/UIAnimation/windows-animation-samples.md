---
title: Exemples d’animation Windows
description: Les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la documentation du gestionnaire d’animations Windows.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Animation Windows Animation Windows, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310862"
---
# <a name="windows-animation-samples"></a>Exemples d’animation Windows

Les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la documentation du gestionnaire d’animations Windows.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                     | Description                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Exemple d’animation pilotée par les applications](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [Exemple d’animation pilotée par minuterie](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [Exemple d’interpolateur personnalisé](custom-interpolator-sample.md)<br/>                   | Montre comment utiliser l’animation Windows avec votre propre interpolateur personnalisé, avec Direct2D utilisé pour le rendu. <br/> |
| [Exemple de disposition en grille](grid-layout-sample.md)<br/>                                   | Montre comment utiliser l’animation Windows, à l’aide de Direct2D pour animer une grille d’images. <br/>                         |
| [Exemple de comparaison de priorité](priority-comparison-sample.md)<br/>                   | Montre comment utiliser l’animation Windows avec votre propre comparaison de priorité, à l’aide de Direct2D pour le rendu.<br/>      |



 

## <a name="sample-files"></a>Fichiers exemples

Chaque exemple contient un grand nombre des fichiers de clé suivants :

<dl> <dt>

<span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp
</dt> <dd>

Définit le point d’entrée de l’application.

</dd> <dt>

<span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h
</dt> <dd>

Déclare la classe CMainWindow.

</dd> <dt>

<span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp
</dt> <dd>

Initialise les composants d’animation et la plateforme graphique, charge les images et restitue la zone cliente.

</dd> <dt>

<span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager. h
</dt> <dd>

Déclare la classe CLayoutManager.

</dd> <dt>

<span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager. cpp
</dt> <dd>

Calcule la disposition des images dans la fenêtre principale, crée des storyboards, ajoute des transitions à la table de montage séquentiel et planifie le Storyboard.

</dd> <dt>

<span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail. h
</dt> <dd>

Déclare la classe CThumbNail.

</dd> <dt>

<span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail. cpp
</dt> <dd>

Crée des variables d’animation et restitue des miniatures.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de développement d’animation Windows](windows-animation-developer-guide.md)
</dt> <dt>

[Informations de référence sur les animations Windows](windows-animation-reference.md)
</dt> </dl>

 

 





