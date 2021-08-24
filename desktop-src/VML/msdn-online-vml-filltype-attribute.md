---
title: FillType VML (attribut)
description: FillType VML (attribut)
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0264fe6cd8cd3dfb7592aea25ef855fda01632647b23f0ab2cffe84c4c504918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680799"
---
# <a name="vml-filltype-attribute"></a>FillType VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le type de remplissage utilisé pour l’arrière-plan d’un trait. En lecture/écriture. **VgFillType**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* fillType = " *expression* " >

**Syntaxe du script**

*Element* . fillType = "*expression*"

*expression* = *élément*. fillType

**Remarques**

Ces valeurs comprennent :



| DashStyle | Description                                    |
|-----------|------------------------------------------------|
| Unie     | Le motif de remplissage est plein. Valeur par défaut.      |
| Tile      | L’image de remplissage est en mosaïque.                       |
| Modèle   | L’image de remplissage est étirée pour former un modèle. |
| Frame     | L’image de remplissage devient une bordure pour la forme. |



 

*Attribut standard VML*

**Exemple**

Le trait de la forme a une texture en mosaïque créée à partir de l’image cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 