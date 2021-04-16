---
title: Attribut de style VML
description: Attribut de style VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463190"
---
# <a name="vml-style-attribute"></a>Attribut de style VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le style du frame. En lecture/écriture. **Chaîne**.

**S’applique à**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Syntaxe de balise**

<v : *Element* style = " *expression* " >

**Syntaxe du script**

*Element* . style = "*expression*"

*expression* = *Element*. style

**Remarques**

Cet attribut utilise les attributs de style CSS normaux pour le positionnement.

*Attribut standard VML*

**Exemple**

Le style définit la position réelle du frame.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 