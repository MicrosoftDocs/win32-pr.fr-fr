---
title: VML DCL-Wrap-distance-attribut supérieur
description: VML DCL-Wrap-distance-attribut supérieur
ms.assetid: 20444d16-fa84-4685-911c-288150c2674b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a16898733ead7bf3728d8f520888c8a05ef5fe6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512510"
---
# <a name="vml-mso-wrap-distance-top-attribute"></a>VML DCL-Wrap-distance-attribut supérieur

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la distance entre le haut de la forme et le texte qui l’entoure. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "mso-Wrap-distance-Top : *expression* " >

**Remarques**

Notez que cet attribut est différent de l’attribut **Margin** CSS. La **marge** modifie l’origine de la forme pour inclure les zones de marge, mais la distance de retour à la ligne dans Microsoft Office ne modifie pas l’origine de la forme.

*Attribut extensions Microsoft Office*

**Exemple**

La forme a une distance supérieure de 10 points.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 