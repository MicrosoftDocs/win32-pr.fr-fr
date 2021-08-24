---
description: Un contexte de périphérique (DC) contient des attributs qui affectent la sortie des courbes et des courbes. Les attributs de ligne et de courbe incluent la position actuelle, le style de pinceau, la couleur de pinceau, le style de stylet, la couleur du stylet, la transformation, etc.
ms.assetid: 9529b389-85f6-421f-8429-9b61cee56ef1
title: Attributs de courbes et de courbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5ab8758cf6e77b28568cacafd8c57312c052d9e9415211f034e3d1a70b6c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831609"
---
# <a name="line-and-curve-attributes"></a>Attributs de courbes et de courbes

Un contexte de périphérique (DC) contient des attributs qui affectent la sortie des courbes et des courbes. Les *attributs de ligne et de courbe* incluent la position actuelle, le style de pinceau, la couleur de pinceau, le style de stylet, la couleur du stylet, la transformation, etc.

La position actuelle par défaut d’un contrôleur de domaine se trouve au point (0, 0) dans l’espace logique (ou universel). Vous pouvez définir ces coordonnées sur une nouvelle position en appelant la fonction [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) et en passant un nouvel ensemble de coordonnées.

> [!Note]  
> Il existe deux ensembles de fonctions de dessin de courbes et de courbes. Le premier jeu conserve la position actuelle dans un DC et le deuxième jeu modifie la position. Vous pouvez identifier les fonctions qui modifient la position actuelle en examinant le nom de la fonction. Si le nom de la fonction se termine par la préposition « to », la fonction définit la position actuelle sur le point de fin de la dernière ligne dessinée ([**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto), [**PolylineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)ou [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)). Si le nom de fonction ne se termine pas par cette préposition, il laisse la position actuelle intacte ([**arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc), [**polyligne**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)ou [**Polybézier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)).

 

Le pinceau par défaut est un pinceau blanc Uni. Une application peut créer un nouveau pinceau en appelant la fonction [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) . Après la création d’un pinceau, l’application peut la sélectionner dans son DC en appelant la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Windows fournit un ensemble complet de fonctions pour créer, sélectionner et modifier le pinceau dans le contrôleur de l’application. Pour plus d’informations sur ces fonctions et sur les pinceaux en général, consultez [pinceaux](brushes.md).

Le stylet par défaut est un stylet cosmétique et un stylet noir Uni d’une largeur d’un pixel. Une application peut créer un stylet à l’aide de la fonction [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Après la création d’un stylet, votre application peut la sélectionner dans son DC en appelant la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Windows fournit un ensemble complet de fonctions pour créer, sélectionner et modifier le stylet dans le contrôleur de l’application. Pour plus d’informations sur ces fonctions et sur les plumes en général, consultez [stylets](pens.md).

La transformation par défaut est la transformation Unity (spécifiée par la matrice d’identité). Une application peut spécifier une nouvelle transformation en appelant la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) . Windows fournit un ensemble complet de fonctions pour transformer les lignes et les courbes en modifiant leur largeur, leur emplacement et leur apparence générale. Pour plus d’informations sur ces fonctions, consultez [espaces de coordonnées et transformations](coordinate-spaces-and-transformations.md).

 

 



