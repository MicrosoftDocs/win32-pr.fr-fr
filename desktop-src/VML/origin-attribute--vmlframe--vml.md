---
title: Origin, attribut (VMLFrame) (VML)
description: Origin, attribut (VMLFrame) (VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874b857a2408927e296f82f0f9aa0a5e15f6da69b1e2af6eaf6ebe2c5df746d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768259"
---
# <a name="origin-attribute-vmlframevml"></a>Origin, attribut (VMLFrame) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit l’origine de la zone de découpage du frame. En lecture/écriture. **VgVector2D**.

**S’applique à**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Syntaxe de balise**

<v : *élément* Origin = " *expression* " >

**Syntaxe du script**

*Element* . Origin = "*expression*"

*expression* = *élément*. Origin

**Remarques**

La valeur par défaut est 0,0. Notez que **origin** fonctionne uniquement si [clip](msdn-online-vml-clip-attribute.md) a la **valeur true**. Dans cet attribut, l’origine est définie comme l’angle supérieur gauche du frame.

*Attribut standard VML*

**Exemple**

L’origine de la région de découpage est 100pt, 100pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 