---
title: BWNormal VML (attribut)
description: BWNormal VML (attribut)
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2811a9cd734e0f2ca6ca2f707b6313d7434ac756a1f9cd8982d7179c75748bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754954"
---
# <a name="vml-bwnormal-attribute"></a>BWNormal VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le mode noir et blanc pour les périphériques de sortie noir et blanc normaux. En lecture/écriture. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :bwnormal = " *expression* " >

**Remarques**

Quand [BWMode](msdn-online-vml-bwmode-attribute.md) est défini sur **auto**, cet attribut est utilisé pour déterminer comment afficher la forme en noir et blanc normal.

Pour plus d’informations sur les valeurs de cet attribut, consultez la rubrique [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . La valeur par défaut est **auto**.

*Microsoft Office Attribut extensions*

**Exemple**

La forme est traitée comme une image en nuances de gris pour une sortie noir et blanc normale.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 