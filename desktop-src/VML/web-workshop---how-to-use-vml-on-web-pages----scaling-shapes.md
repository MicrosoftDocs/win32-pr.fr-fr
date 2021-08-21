---
title: Mise à l’échelle des formes
description: Mise à l’échelle des formes
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Atelier Web, mise à l’échelle des formes
- conception de pages Web, mise à l’échelle des formes
- Langage VML (VML), mise à l’échelle des formes
- VML (langage VML), mise à l’échelle des formes
- graphiques vectoriels, mise à l’échelle des formes
- Formes VML, mise à l’échelle
- mise à l’échelle des formes
- Langage VML (VML), formes de dimensionnement
- VML (langage VML), formes de redimensionnement
- graphiques vectoriels, formes de dimensionnement
- Formes VML, redimensionnement
- dimensionnement des formes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc7f62d802548ef1bc19aabf33c886c5b826098ae1280a9dd0b69413c9a61aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057009"
---
# <a name="scaling-shapes"></a>Mise à l’échelle des formes

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Vous avez appris à dessiner et à colorier des formes sur une page Web à l’aide de VML. Dans cette rubrique, nous allons vous montrer comment mettre les formes à l’échelle selon la taille de votre choix.

VML utilise la même syntaxe que celle définie dans la section [Détails du modèle de rendu visuel](https://www.w3.org/TR/PR-CSS2/visudet.mdl) de la [Spécification CSS2](https://www.w3.org/TR/PR-CSS2/) pour spécifier la taille de la zone conteneur afin que le contenu d’une forme soit rendu (dessiné) dans la zone conteneur. Vous pouvez utiliser les attributs de style de **largeur** et de **hauteur** pour définir la taille de la zone conteneur.

Par exemple, si vous dessinez un ovale et spécifiez **style**= 'width : 75pt ; height : 100pt', l’ovale sera dessiné dans une zone conteneur à une taille de 75 points (largeur) de 100 points (hauteur), comme indiqué dans l’image suivante :

![oval1.gif (660 octets)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





Si vous modifiez la taille en **style**= 'width : 120PT ; height : 140pt', l’ovale devient plus grand car il est mis à l’échelle dans la nouvelle zone conteneur à une taille de 120 points (largeur) de 140 points (hauteur), comme illustré dans l’image suivante :

![oval2.gif (966 octets)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





Si vous modifiez la taille en **style**= 'width : 60pt ; height : 40pt', l’ovale devient plus petit, car il est mis à l’échelle dans la nouvelle zone conteneur à une taille de 60 points (largeur) de 40 points (hauteur), comme indiqué dans l’image suivante :

![oval3.gif (394 octets)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 