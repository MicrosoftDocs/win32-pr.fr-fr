---
title: JoinStyle VML (attribut)
description: JoinStyle VML (attribut)
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbad649d2a8889846d1d0c1e1df3d62e94cb8e8ff03f0dfa5c47f7bd414dcdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599363"
---
# <a name="vml-joinstyle-attribute"></a>JoinStyle VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le style de jointure d’une polyligne. En lecture/écriture. Chaîne.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* joinstyle = " *expression* " >

**Syntaxe du script**

*Element* . joinstyle = "*expression*"

*expression* = *élément*. joinstyle

**Remarques**

Ces valeurs comprennent :

-   Round (valeur par défaut)
-   soudure
-   Mitre

*Attribut standard VML*

**Exemple**

Les jointures sur la polyligne sont biseautées.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 