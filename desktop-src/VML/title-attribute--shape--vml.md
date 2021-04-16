---
title: Attribut titre (Shape) (VML)
description: Attribut titre (Shape) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463663"
---
# <a name="title-attribute-shapevml"></a>Attribut titre (Shape) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le texte affiché lorsque le pointeur de la souris se déplace sur la forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *élément* title = " *expression* " >

**Syntaxe du script**

*Element* . title = "*expression*"

*expression* = *Element*. title

**Remarques**

L’attribut **title** est semblable à l’attribut de **titre** HTML standard. Le comportement d’un titre est semblable à celui d’une info-bulle Microsoft Windows.

**Attribut standard VML**

**Exemple**

Le titre de la forme est « affichage de l’info-bulle » et s’affiche lorsque le pointeur de la souris se déplace au-dessus de la forme.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemple d’attribut title](/previous-versions/bb264097(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 