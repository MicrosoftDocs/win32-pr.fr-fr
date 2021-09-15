---
description: La plupart des applications tentent de prendre en charge le rendu WYSIWYG (ce que vous obtenez).
ms.assetid: 34a1f37c-0fbf-451b-bb55-80ad85bcd4de
title: Affichage et sortie WYSIWYG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c03e4fa653c0d8e891cb079a7a7e7a003f9ad1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522449"
---
# <a name="wysiwyg-display-and-output"></a>Affichage et sortie WYSIWYG

La plupart des applications tentent de prendre en charge le rendu WYSIWYG (ce que vous obtenez). Cela signifie que le texte dessiné avec une police de caractères gras Helvetica de 10 points dans la fenêtre d’application doit avoir une apparence similaire lorsqu’il est imprimé. L’obtention d’une vraie sortie WYSIWYG est pratiquement impossible et même indésirable dans la plupart des cas. Cela est dû, en partie, aux différences dans les technologies de vidéo et d’impression. un pixel sur un écran est généralement plus grand qu’un point sur une imprimante laser commune. Les distances d’affichage sont également différentes ; un utilisateur d’ordinateur se trouve généralement à deux mètres de l’écran, mais les yeux d’un lecteur sont généralement d’un pied de page ou moins sur la page imprimée.

Pour compenser les différences de lisibilité entre les écrans et la page imprimée, le système prend en charge une unité appelée pouce logique qui est toujours spécifiée en pixels. Pour un affichage vidéo, le pouce logique est toujours supérieur au pouce physique pour compenser la distance de visualisation plus longue et la résolution plus grossière (généralement). Pour les imprimantes, le pouce logique est toujours égal au pouce physique.

Pour obtenir un effet WYSIWYG lors du dessin de texte, deux problèmes connexes sont impliqués : faire en sorte que les caractères individuels aient le même aspect et la disposition de page indépendante du périphérique. Pour résoudre le premier problème, une application peut utiliser la fonction [**CreateFont**](/windows/desktop/api/wingdi/nf-wingdi-createfonta) pour spécifier le nom de la police et la taille d’une police idéale (ou logique), puis appeler la fonction [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) pour identifier le contexte de périphérique d’affichage ou d’imprimante. Lorsque l’application appelle **SelectObject** , le système sélectionne une police physique qui est la correspondance la plus proche possible à la police logique spécifiée. Lorsque le système sélectionne la police d’affichage, il choisit une police physique supérieure à la taille réelle. Cela se produit en raison du plus grand pouce logique sur l’affichage. Toutefois, du point de vue de l’utilisateur, il semble très proche de la hauteur correcte. Lorsque le système sélectionne la police de l’imprimante, il choisit une police physique qui correspond réellement à la taille demandée. Pour plus d’informations sur les polices et la sortie de texte, consultez [polices et texte](/windows/desktop/gdi/fonts-and-text).

Le deuxième problème, en ce qui concerne la mise en page indépendante du périphérique, peut être résolu par l’utilisation des métriques TrueType. Cela est vrai même lorsque vous conservez la compatibilité avec les versions 16 bits de Windows. Pour plus d’informations, consultez [utilisation des métriques TrueType portables](/windows/desktop/gdi/using-portable-truetype-metrics).

Pour obtenir un effet WYSIWYG lors du dessin de graphiques bitmap, une application peut récupérer la largeur et la hauteur, en pouces logiques, de l’écran et de la page imprimée. À l’aide de ces valeurs, l’application peut créer des facteurs de mise à l’échelle horizontale et verticale pour maintenir la proportion d’images bitmap lorsqu’elles sont dessinées sur une imprimante. Pour plus d’informations sur les bitmaps et la sortie bitmap, consultez [bitmaps](/windows/desktop/gdi/bitmaps).

 

 
