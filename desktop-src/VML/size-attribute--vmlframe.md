---
title: Attribut Size (VMLFrame)
description: Attribut Size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32d496bc40b5b84b7a8a16bf6b84a2926010d56dcc311659dd63300363a7067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754124"
---
# <a name="size-attribute-vmlframe"></a>Attribut Size (VMLFrame)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la taille de la zone de découpage du frame. En lecture/écriture. **VgVector2D**.

**S’applique à**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Syntaxe de balise**

<v : *Element* size = " *expression* " >

**Syntaxe du script**

*Element* . Size = "*expression*"

*expression* = *Element*. Size

**Remarques**

La valeur par défaut est 0,0. Notez que la **taille** ne fonctionne que si [clip](msdn-online-vml-clip-attribute.md) a la **valeur true**. Dans cet attribut, la taille est définie comme la largeur et la hauteur du cadre.

*Attribut standard VML*

**Exemple**

La taille de la zone de découpage sera 50pt, 50pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 