---
title: VML V-text-align (attribut)
description: VML V-text-align (attribut)
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bf8ec2e781b04e7ababc0b30ea3996e569e5cf9066a4bac072806fd7329eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117939128"
---
# <a name="vml-v-text-align-attribute"></a>VML V-text-align (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit l’alignement du texte. En lecture/écriture. **Chaîne**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* style = "v-text-align : *expression* " >

**Syntaxe du script**

*Element* . style. v-text-align = "*expression*"

*expression* = *Element*. style. v-text-align

**Remarques**

Ces valeurs comprennent :

-   **gauche** (valeur par défaut)
-   **Oui**
-   **gestionnaire**
-   **prouver**
-   **lettre-Justify**
-   **étirer-justifier**

*Attribut standard VML*

**Exemple**

Le texte sera étiré pour s’ajuster au tracé, mais l’espace supplémentaire sera placé entre chaque lettre.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 