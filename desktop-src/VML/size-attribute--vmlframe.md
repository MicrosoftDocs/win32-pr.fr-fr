---
title: Attribut Size (VMLFrame)
description: Attribut Size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031304"
---
# <a name="size-attribute-vmlframe"></a>Attribut Size (VMLFrame)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 