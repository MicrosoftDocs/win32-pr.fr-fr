---
title: Attribut de police VML
description: Attribut de police VML
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106530797"
---
# <a name="vml-font-attribute"></a>Attribut de police VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Spécifie une valeur composée d’attributs de police. En lecture/écriture. **Chaîne**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* style = "font : *expression* " >

**Syntaxe du script**

*Element* . style. font = "*expression*"

*expression* = *Element*. style. font

**Remarques**

Définit les attributs d’une police, y compris famille, style, poids, taille et variante. L’ordre des définitions dans la chaîne est le suivant : **style de police**, **police-variante**, police **-poids**, **police-taille**, **hauteur de ligne** et **famille de polices**. Les valeurs sont les mêmes que les attributs de style HTML standard.

*Attribut standard VML*

**Exemple**

La police du texte TextPath est italique, petite majuscule, gras, 36 point Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 