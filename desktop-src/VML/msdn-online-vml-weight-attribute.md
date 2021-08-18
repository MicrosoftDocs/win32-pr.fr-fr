---
title: Attribut de pondération VML
description: Attribut de pondération VML
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1a4dc7e33a4a1bf8421350bed9df374f7edd31a1c1a48a2b3e1549dc63084d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999089"
---
# <a name="vml-weight-attribute"></a>Attribut de pondération VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit l’épaisseur d’un trait. En lecture/écriture. **Chaîne**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : poids de l' *élément* = « *expression* » >

**Syntaxe du script**

*Element* . Weight = "*expression*"

*expression* = *élément*. poids

**Remarques**

Cet attribut est le même que l’attribut **StrokeWeight** de **Shape** et le remplace. La valeur par défaut est 1 point.

*Attribut standard VML*

**Exemple**

Le trait a une épaisseur de 5 points, et non pas de 2 points.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 