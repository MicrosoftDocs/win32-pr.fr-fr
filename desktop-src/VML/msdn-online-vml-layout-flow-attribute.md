---
title: Attribut Layout-Flow VML
description: Attribut Layout-Flow VML
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941153"
---
# <a name="vml-layout-flow-attribute"></a>Attribut Layout-Flow VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine le déroulement de la disposition du texte dans une zone de texte. En lecture/écriture. **Chaîne**.

**S’applique à**

[TextBox](msdn-online-vml-textbox-element.md)

**Syntaxe de balise**

<v : type d' *élément* = « disposition-Flow : *expression* » >

**Remarques**

Ces valeurs comprennent :



| Valeur                  | Description                                 |
|------------------------|---------------------------------------------|
| horizontal             | Le texte est affiché horizontalement. Par défaut.    |
| Barr               | Le texte est affiché verticalement.               |
| vertical-IDÉOGRAPHIQUE   | Le texte IDÉOGRAPHIQUE est affiché verticalement.   |
| horizontal-IDÉOGRAPHIQUE | Le texte IDÉOGRAPHIQUE est affiché horizontalement. |



 

*Attribut standard VML*

**Exemple**

Le déroulement du texte dans la zone de texte est transmis verticalement.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 