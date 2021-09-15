---
title: Fonctionnement des commandes et des contrôles
description: la séparation de la logique de la présentation est la philosophie de conception qui inspire le système de présentation de commande du Windows infrastructure de ruban \ 8212 ; un système basé sur un modèle de conception où les fonctionnalités et le comportement sont implémentés indépendamment des contrôles qui exposent cette fonctionnalité.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Windows Ruban, vue d’ensemble des commandes
- Ruban, vue d’ensemble des commandes
- Windows Ruban, vue d’ensemble des contrôles
- Ruban, vue d’ensemble des contrôles
- système de commandes pour Windows ruban
- contrôles pour Windows ruban
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411416"
---
# <a name="understanding-commands-and-controls"></a>Fonctionnement des commandes et des contrôles

la séparation de la logique de la présentation est la philosophie de conception qui inspire le système de présentation de commande de l’infrastructure du ruban Windows, un système basé sur un modèle de conception dans lequel les fonctionnalités et le comportement sont implémentés indépendamment des contrôles qui exposent cette fonctionnalité.

-   [Introduction](#introduction)
-   [système de commandes du ruban Windows](#the-windows-ribbon-command-system)
    -   [Contrôles](#understanding-commands-and-controls)
    -   [Commandes](#understanding-commands-and-controls)
    -   [L’expérience de commande en action](#the-command-experience-in-action)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Cet article décrit la conception du système de commandes du Framework du ruban. Il décrit les concepts des commandes et des contrôles et explore comment ils fonctionnent ensemble pour fournir une expérience de commande riche avec un grand nombre de nouvelles fonctionnalités de l’interface utilisateur.

## <a name="the-windows-ribbon-command-system"></a>système de commandes du ruban Windows

Dans l’infrastructure du ruban, les commandes et les contrôles sont des entités indépendantes. Une commande est une structure abstraite, sans contraintes de présentation, qui représente une tâche ou une classe de fonctionnalité spécifique. Un contrôle, en revanche, est un objet concret qui expose les fonctionnalités de commande par le biais de l’interface ruban.

Cette distinction permet de définir des commandes qui sont exemptes de détails de l’interface utilisateur et de s’exécuter sur l’intention d’une action sans avoir à gérer la façon dont l’action a été appelée.

### <a name="controls"></a>Commandes

Les contrôles sont les objets d’interface utilisateur requis pour la présentation de commande. Elles sont rendues et gérées au moment de l’exécution par le Framework en fonction de l’interaction de l’utilisateur et d’un ensemble de propriétés et de comportements inhérents.

Appelée disposition adaptative, la flexibilité gérée par l’infrastructure de l’interface utilisateur est l’un des atouts du ruban. Les contrôles de ruban peuvent être reconfigurés automatiquement à l’aide de modèles de disposition dépendants du Framework ou définis par le développeur qui sont en mesure de répondre à différentes exigences de temps d’exécution, tout cela sans écrire une seule ligne de code de présentation. Pour plus d’informations, consultez [Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md).

Outre les avantages de la mise en page adaptative, un certain nombre de contrôles de ruban complexes fournissent des solutions autonomes pour des espaces de problème d’interface utilisateur spécifiques. en proposant un modèle d’interaction sophistiqué, les contrôles de ruban, tels que FontControl ou ColorPicker, permettent de manipuler des données en termes plus abstraits par le biais de conteneurs de propriétés d’attributs de police ou de couleur réels plutôt que par l’intermédiaire de différents sous-contrôles, énumérations et valeurs d’index de contrôles de Windows standard.

### <a name="commands"></a>Commandes

Faiblement couplé aux contrôles du ruban qui exposent leurs fonctionnalités, les implémentations de commande sont le domaine de l’application hôte et prennent la forme d’écouteurs d’événements, de gestionnaires de commandes et de diverses propriétés de commande.

Les commandes sont déclarées dans le balisage du ruban avec un ID unique, ou un ID généré par le compilateur de balisage est assigné lors de la compilation. Les commandes sont associées à des contrôles via un nom de commande mais, contrairement aux contrôles, leurs fonctionnalités réelles sont définies dans le code où elles sont liées à des gestionnaires de commandes spécifiques par le biais de l’ID de commande.

> [!Note]  
> Lors de la compilation, cet ID est stocké dans un fichier d’en-tête de définition d’ID qui expose des commandes à leurs gestionnaires de commandes correspondants dans l’application hôte du ruban.

 

Chaque commande possède un type de commande sous-jacent dans l’énumération [**\_ COMMANDTYPE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) .

### <a name="the-command-experience-in-action"></a>L’expérience de commande en action

Les fonctionnalités de ce modèle de commande sont illustrées par la barre d’outils accès rapide du ruban. Le QAT fournit aux utilisateurs finaux un moyen de définir facilement leurs propres raccourcis pour quasiment n’importe quel contrôle dans l’interface utilisateur du ruban. Un raccourci est ajouté dynamiquement au QAT au moment de l’exécution lorsque l’utilisateur clique avec le bouton droit sur un contrôle de ruban et sélectionne **Ajouter à la barre d’outils accès rapide** dans le menu contextuel.

l’illustration suivante montre les commandes **coller** et **coller à partir** de, représentées par un contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) , dans le ruban de Windows 7 Paint.

![image du SplitButton coller dans le ruban Microsoft Paint.](images/overviews/paint-paste-splitbutton-ribbon.png)

l’illustration suivante montre les mêmes commandes **coller** et **coller** dans les commandes, toujours représentées par un contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) , dans le ruban QAT de Windows 7 Paint.

![image du SplitButton coller dans Microsoft Paint qat.](images/overviews/paint-paste-splitbutton-qat.png)

Lorsqu’un contrôle est hébergé par le QAT, la nouvelle instance du contrôle conserve toutes les fonctionnalités du contrôle d’origine sans qu’il soit nécessaire d’utiliser des écouteurs d’événements et des gestionnaires de commandes supplémentaires pour le prendre en charge. Les deux contrôles sont liés au même gestionnaire de commandes du ruban via un identificateur de commande partagé. De cette façon, l’infrastructure traite les deux contrôles comme un, quelle que soit la méthode appelée.

> [!Note]  
> Les mêmes avantages sont obtenus lorsque les commandes sont incorporées dans un [**ContextPopup**](windowsribbon-element-contextpopup.md) au moment de la conception. Dans ce cas, les gestionnaires de commandes Coller peuvent être utilisés, que le contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) apparaisse dans le ruban, le qat ou le **ContextPopup**.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[présentation de l’infrastructure du ruban Windows](windowsribbon-introduction.md)
</dt> <dt>

[Création d’une application de ruban](windowsribbon-stepbystep.md)
</dt> <dt>

[Déclaration des commandes et des contrôles avec le balisage du ruban](windowsribbon-schema.md)
</dt> </dl>

 

 