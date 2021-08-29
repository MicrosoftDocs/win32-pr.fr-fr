---
title: BWPure VML (attribut)
description: BWPure VML (attribut)
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b06c53ddc6279d16eeeaaed40a87794a1ab06d8b282ce4eef12a0e1bd74e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999299"
---
# <a name="vml-bwpure-attribute"></a>BWPure VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le mode noir et blanc pour les périphériques de sortie noir et blanc purs. En lecture/écriture. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :bwpure = " *expression* " >

**Remarques**

Quand [BWMode](msdn-online-vml-bwmode-attribute.md) est défini sur **auto**, cet attribut est utilisé pour déterminer comment afficher la forme en noir et blanc pur.

Pour plus d’informations sur les valeurs de cet attribut, consultez la rubrique [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . La valeur par défaut est **auto**.

*Microsoft Office Attribut extensions*

**Exemple**

La forme est traitée comme une image à contraste élevé pour une sortie en noir et blanc pur.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 