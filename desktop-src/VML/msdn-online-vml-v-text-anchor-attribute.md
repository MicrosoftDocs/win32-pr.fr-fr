---
title: VML V-text-anchor (attribut)
description: VML V-text-anchor (attribut)
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c4b355aa4e56e3b0320200a092a66aa1f504b16be02f697e1335cd295627c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057697"
---
# <a name="vml-v-text-anchor-attribute"></a>VML V-text-anchor (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit l’ancrage vertical du texte dans une zone de texte. En lecture/écriture. **Chaîne**.

**S’applique à**

[TextBox](msdn-online-vml-textbox-element.md)

**Syntaxe de balise**

<v : *élément* v-text-anchor = " *expression* " >

**Remarques**

Ces valeurs comprennent :

-   **Top** (par défaut)
-   **intergiciel**
-   **ballon**
-   **Haut-centre**
-   **Centre au milieu**
-   **en bas au centre**
-   **haut de la ligne de base**
-   **Bas-ligne de base**
-   **Haut-centre-ligne de base**
-   **bas-centre-ligne de base**

Le texte est ancré à une position verticale dans la zone de texte, comme indiqué par la valeur de l’attribut. L’alignement d’une ancre de texte devient évident si la [fonction mso-fit-Text-to-Model](msdn-online-vml-mso-fit-text-to-shape-attribute.md) a la **valeur false**. Cet attribut est différent de l’attribut de style **vertical-align** , qui est utilisé pour les langages idéographiques.

cet attribut est utilisé par Microsoft Office pour stocker des données dans des documents Web, mais il n’est pas rendu dans Microsoft Internet Explorer 5 ou version ultérieure.

*Attribut standard VML*

**Exemple**

Le texte est aligné au bas de la zone de texte.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 