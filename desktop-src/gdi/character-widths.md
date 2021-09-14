---
description: Les applications doivent récupérer des données de largeur de caractères lorsqu’elles effectuent des tâches telles que des chaînes de texte à des largeurs de page ou de colonne.
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: Largeurs de caractères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fbb7e6ad1e5f4ef12f2abd9e528ce3158a869
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122309"
---
# <a name="character-widths"></a>Largeurs de caractères

Les applications doivent récupérer des données de largeur de caractères lorsqu’elles effectuent des tâches telles que des chaînes de texte à des largeurs de page ou de colonne. Il existe quatre fonctions qu’une application peut utiliser pour récupérer des données de largeur de caractères. Deux de ces fonctions récupèrent la largeur des caractères-Advance et deux de ces fonctions récupèrent les données de la largeur réelle des caractères.

Une application peut utiliser les fonctions [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) et [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) pour récupérer la largeur d’avance pour des caractères ou des symboles individuels dans une chaîne de texte. La largeur d’avance correspond à la distance que le curseur sur un affichage vidéo ou le côté impression d’une imprimante doit avancer avant d’imprimer le caractère suivant dans une chaîne de texte. La fonction [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) retourne la largeur avancée sous la forme d’une valeur entière. Si une précision supérieure est requise, une application peut utiliser la fonction [**GetCharWidthFloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) pour récupérer les valeurs de largeur d’avance fractionnaires.

Une application peut récupérer des données de largeur de caractères réelles à l’aide des fonctions [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) et [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) . La fonction **GetCharABCWidthsFloat** fonctionne avec toutes les polices. La fonction [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) fonctionne uniquement avec les polices TrueType et OpenType. Pour plus d’informations sur les polices TrueType et OpenType, consultez [polices Raster, Vector, TrueType et OpenType](raster--vector--truetype--and-opentype-fonts.md).

L’illustration suivante montre les trois composants d’une largeur de caractère :

![Illustration montrant l’espacement a, l’espacement b et l’espacement en c de deux caractères adjacents](images/csftx-02.png)

L’espacement est la largeur à ajouter à la position actuelle avant de placer le caractère. L’espacement B est la largeur du caractère lui-même. L’espacement C est l’espace blanc à droite du caractère. La largeur totale de l’avance est déterminée en calculant la somme de A + B + C. La cellule de caractère est un rectangle imaginaire qui entoure chaque caractère ou symbole dans une police. Étant donné que les caractères peuvent déborder ou bloquer la cellule de caractère, l’un des incréments A et C, ou les deux, peuvent être un nombre négatif.

 

 
