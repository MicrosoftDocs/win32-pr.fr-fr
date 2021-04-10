---
title: Offset, attribut (Shadow) (VML)
description: Offset, attribut (Shadow) (VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941055"
---
# <a name="offset-attribute-shadowvml"></a>Offset, attribut (Shadow) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le degré d’extension de l’ombre au-delà de la forme. En lecture/écriture. **VgVector2D**.

**S’applique à**

[Shadow](msdn-online-vml-shadow-element.md)

**Syntaxe de balise**

<v : offset de l' *élément* = « *expression* » >

**Syntaxe du script**

*Element* . Offset = "*expression*"

*expression* = *Element*. Offset

**Remarques**

Le décalage par défaut de la valeur x est 2pt et la valeur par défaut de la valeur y est 2pt. Les valeurs sont soit une mesure absolue, soit une valeur fractionnaire de forme. Si fractionnaires, elles sont comprises entre 50% et-50%.

*Attribut standard VML*

**Exemple**

La forme a une ombre avec un décalage de 5 points vers le dessous et de 10 points vers la droite.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 