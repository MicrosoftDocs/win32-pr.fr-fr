---
title: BWPure VML (attribut)
description: BWPure VML (attribut)
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842445"
---
# <a name="vml-bwpure-attribute"></a>BWPure VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le mode noir et blanc pour les périphériques de sortie noir et blanc purs. En lecture/écriture. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :bwpure = " *expression* " >

**Remarques**

Quand [BWMode](msdn-online-vml-bwmode-attribute.md) est défini sur **auto**, cet attribut est utilisé pour déterminer comment afficher la forme en noir et blanc pur.

Pour plus d’informations sur les valeurs de cet attribut, consultez la rubrique [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . La valeur par défaut est **auto**.

*Attribut extensions Microsoft Office*

**Exemple**

La forme est traitée comme une image à contraste élevé pour une sortie en noir et blanc pur.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 