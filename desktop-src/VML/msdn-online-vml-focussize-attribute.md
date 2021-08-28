---
title: FocusSize VML (attribut)
description: FocusSize VML (attribut)
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322bea9f9d78ff76cd631cc36149939bb5b3db5f87dc9c80e9f2a5100f031c1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099259"
---
# <a name="vml-focussize-attribute"></a>FocusSize VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la taille du focus pour les remplissages radiaux. En lecture/écriture. **VgVector2D**.

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *Element* focussize = " *expression* " >

**Syntaxe du script**

*Element* . focussize = "*expression*"

*expression* = *élément*. focussize

**Remarques**

Les valeurs sont des fractions de la largeur et de la hauteur de la forme. Le premier est un pourcentage du remplissage jusqu’au bord droit de la forme et le deuxième est un pourcentage du remplissage jusqu’au fond de la forme. La valeur par défaut est 0,0. Une valeur **FocusSize** de 100%, 100% et un **FocusPosition** de 0, 0 ferait que Color2 domine complètement la fusion. Les petites valeurs d’environ 10%, 10% sont recommandées pour les fusions équilibrées.

*Attribut standard VML*

**Exemple**

Le remplissage radial crée une fusion à partir du centre en bleu et devient rouge sur les quatre bords. Le centre de la fusion est défini par **FocusPosition** et la taille de la couleur de début interne est déterminée par **FocusSize**.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 