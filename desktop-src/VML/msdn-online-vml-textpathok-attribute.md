---
title: TextPathOK VML (attribut)
description: TextPathOK VML (attribut)
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2c14d613df36c314dea75275a4d60fe8792d6dea644ef2595422e74a73dc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597453"
---
# <a name="vml-textpathok-attribute"></a>TextPathOK VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si un chemin d’accès de texte sera affiché. En lecture/écriture. **VgTriState**.

**S’applique à**

[Chemin d’accès](msdn-online-vml-path-element.md)

**Syntaxe de balise**

<v : *Element* textpathok = " *expression* " >

**Syntaxe du script**

*élément* . textpathok = "*expression*"

*expression* = *élément*. textpathok

**Remarques**

Si la **valeur est false**, le chemin d’accès ne peut pas contenir de texte. La valeur par défaut est **False**. Cet attribut doit avoir la valeur **true** pour afficher du texte sur un tracé.

*Attribut standard VML*

**Exemple**

La forme a un tracé de texte. Le texte « Hello VML » s’affiche sur une courbe en forme de sourire.


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 