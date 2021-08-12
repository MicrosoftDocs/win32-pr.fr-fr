---
title: VML, attribut de classe
description: VML, attribut de classe
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ada95b56430dacd09801a9aaa200c92abab064bbbb5732b369372de63c34de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602180"
---
# <a name="vml-class-attribute"></a>VML, attribut de classe

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Fait référence à une définition d’un style CSS. En lecture/écriture. **Chaîne**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* Class = " *expression* " >

**Syntaxe du script**

*Element* . ClassName = "*expression*"

*expression* = *élément*. ClassName

**Remarques**

L’attribut de **classe** est semblable à l’attribut de **classe** HTML standard utilisé avec les feuilles de style CSS.

Notez que **className** est utilisé à la place de **Class** pour les scripts. Notez également que pour les scripts, la **className** peut uniquement être lue. la modification de la valeur de **className** ne modifiera pas le rendu de la forme.

*Attribut standard VML*

**Voir aussi**

[Forme](shape-element--vml.md)

**Exemple**

Une classe pour **Width** est créée avec le style


```HTML
   .narrowstyle {width:50;height:100}
```



La largeur est alors référencée par l’inclusion du style. Notez que la largeur andheight n’est pas définie dans l’attribut **style** , mais sera définie par le style.


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



Notez que la **classe** s’applique uniquement aux attributs CSS-type.

 

 