---
title: TextBoxRect VML (attribut)
description: TextBoxRect VML (attribut)
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644d4a89effa54a991d04de4c97c4f9d86876a78d86149d9b99c3a8161585b44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597481"
---
# <a name="vml-textboxrect-attribute"></a>TextBoxRect VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit une ou plusieurs zones de texte à l’intérieur d’une forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Chemin d’accès](msdn-online-vml-path-element.md)

**Syntaxe de balise**

<v : *Element* textboxrect = " *expression* " >

**Syntaxe du script**

*Element* . textboxrect = "*expression*"

*expression* = *élément*. textboxrect

**Remarques**

Une zone de texte est définie par un ou plusieurs ensembles de nombres spécifiant (dans l’ordre) les points gauche, supérieur, droit et inférieur du rectangle. Les jeux multiples sont délimités par un point-virgule. La valeur par défaut est la même valeur de dimension que le rectangle conteneur. Si plusieurs zones de texte sont définies, les jeux quadruples délimités par des virgules qui définissent chaque zone de texte sont séparés par des points-virgules. Normalement, les zones de texte sont des jeux de 1, 2, 3 ou 6 rectangles sur une forme.

*Attribut standard VML*

**Exemple**

Une zone de texte de 95 unités par unité de 95 est définie et placée 5 unités dans le coin supérieur gauche de la forme.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 