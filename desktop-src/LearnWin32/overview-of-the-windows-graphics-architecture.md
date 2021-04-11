---
title: Vue d’ensemble de l’architecture graphique Windows
description: Décrit les API graphiques C++/COM dans Windows.
ms.assetid: 9654b18b-d615-455d-a92a-6fc2ccda469e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45ba44f54b947d923b888d51080ff0335119a1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "104116014"
---
# <a name="overview-of-the-windows-graphics-architecture"></a>Vue d’ensemble de l’architecture graphique Windows

Windows fournit plusieurs API C++/COM pour les graphiques. Ces API sont présentées dans le diagramme suivant.

![diagramme qui montre les API graphiques Windows.](images/graphics01.png)

-   Graphics Device Interface (GDI) est l’interface graphique d’origine pour Windows. GDI a été écrit pour la première fois pour Windows 16 bits, puis mis à jour pour Windows 32 bits et 64 bits.
-   GDI+ a été introduit dans Windows XP en tant que successeur de GDI. La bibliothèque GDI+ est accessible via un ensemble de classes C++ qui encapsulent des fonctions C plates. Le .NET Framework fournit également une version managée de GDI+ dans l’espace de noms **System. Drawing** .
-   Direct3D prend en charge les graphiques 3D.
-   Direct2D est une API moderne pour les graphiques 2D, le successeur de GDI et GDI+.
-   DirectWrite est un moteur de rastérisation et de mise en page de texte. Vous pouvez utiliser GDI ou Direct2D pour dessiner le texte pixellisé.
-   L’infrastructure DXGI (DirectX Graphics) effectue des tâches de bas niveau, telles que la présentation des frames pour la sortie. La plupart des applications n’utilisent pas directement DXGI. Au lieu de cela, elle sert de couche intermédiaire entre le pilote Graphics et Direct3D.

Direct2D et DirectWrite ont été introduits dans Windows 7. Ils sont également disponibles pour Windows Vista et Windows Server 2008 via une mise à jour de plateforme. Pour plus d’informations, consultez [mise à jour de la plateforme pour Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

Direct2D est le sujet de ce module. Bien que GDI et GDI+ continuent à être pris en charge dans Windows, Direct2D et DirectWrite sont recommandés pour les nouveaux programmes. Dans certains cas, une combinaison de technologies peut être plus pratique. Dans ce cas, Direct2D et DirectWrite sont conçus pour interagir avec GDI.

Les sections suivantes décrivent certains des avantages de Direct2D.

### <a name="hardware-acceleration"></a>Accélération matérielle

Le terme « *accélération matérielle* » fait référence aux calculs graphiques effectués par l’unité de traitement graphique (GPU), plutôt que par le processeur. Les GPU modernes sont hautement optimisés pour les types de calcul utilisés dans le rendu des graphiques. En général, plus ce travail est déplacé du processeur vers le GPU, mieux c’est.

Bien que GDI prenne en charge l’accélération matérielle pour certaines opérations, de nombreuses opérations GDI sont liées à l’UC. Direct2D est superposé à Direct3D et tire pleinement parti de l’accélération matérielle fournie par le GPU. Si le GPU ne prend pas en charge les fonctionnalités requises pour Direct2D, Direct2D revient au rendu logiciel. En général, Direct2D exécute GDI et GDI+ dans la plupart des cas.

### <a name="transparency-and-anti-aliasing"></a>Transparence et anticrénelage

Direct2D prend en charge la transparence alpha à accélération matérielle totale (transparence).

GDI offre une prise en charge limitée pour la fusion alpha. La plupart des fonctions GDI ne prennent pas en charge la fusion alpha, bien que GDI prenne en charge la fusion alpha pendant une opération BitBlt. GDI+ prend en charge la transparence, mais la fusion alpha est effectuée par le processeur, de sorte qu’il ne tire pas parti de l’accélération matérielle.

La fusion alpha avec accélération matérielle permet également l’anticrénelage. L' *alias* est un artefact provoqué par l’échantillonnage d’une fonction continue. Par exemple, lorsqu’une ligne incurvée est convertie en pixels, l’alias peut entraîner une apparence irrégulière. \[ 3 \] toute technique qui réduit les artefacts provoqués par les alias est considérée comme une forme d’anticrénelage. Dans les graphiques, l’anticrénelage s’effectue en fusionnant les bords avec l’arrière-plan. Par exemple, voici un cercle dessiné par GDI et le même cercle dessiné par Direct2D.

![illustration des techniques d’anticrénelage dans Direct2D.](images/graphics02.png)

L’image suivante montre un détail de chaque cercle.

![détail de l’image précédente.](images/graphics03.png)

Le cercle dessiné par GDI (à gauche) est constitué de pixels noirs qui se rapprochent d’une courbe. Le cercle dessiné par Direct2D (Right) utilise la fusion pour créer une courbe plus lisse.

GDI ne prend pas en charge l’anticrénelage lorsqu’il dessine une géométrie (lignes et courbes). GDI peut dessiner du texte avec anticrénelage à l’aide de ClearType. dans le cas contraire, le texte GDI est également associé à un alias. L’alias est particulièrement visible pour le texte, car les lignes en escalier perturbent la conception des polices, ce qui rend le texte moins lisible. Bien que GDI+ prenne en charge l’anticrénelage, il est appliqué par le processeur, de sorte que les performances ne sont pas aussi efficaces que Direct2D.

### <a name="vector-graphics"></a>Graphismes vectoriels

Direct2D prend en charge les *graphiques vectoriels*. Dans les graphiques vectoriels, les formules mathématiques sont utilisées pour représenter des lignes et des courbes. Ces formules ne sont pas dépendantes de la résolution d’écran et peuvent donc être mises à l’échelle en dimensions arbitraires. Les graphiques vectoriels sont particulièrement utiles quand une image doit être mise à l’échelle pour prendre en charge différentes tailles d’analyse ou résolutions d’écran.

## <a name="next"></a>Suivant

[Gestionnaire de fenêtrage](the-desktop-window-manager.md)

 

 
