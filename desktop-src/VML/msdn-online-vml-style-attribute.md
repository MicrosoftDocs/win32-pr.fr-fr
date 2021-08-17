---
title: Attribut de style VML
description: Attribut de style VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0b7ce7985687d560fc46ebb98d41b51e7a461e811deb228b0a5709a35c5d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475189"
---
# <a name="vml-style-attribute"></a>Attribut de style VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 