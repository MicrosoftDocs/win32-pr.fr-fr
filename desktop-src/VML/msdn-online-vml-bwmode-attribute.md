---
title: BWMode VML (attribut)
description: BWMode VML (attribut)
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5640680af40f4649f7ab34b2ec8cfd4e5cf94ee4c7c6ce3c3f2185e68bdac360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754964"
---
# <a name="vml-bwmode-attribute"></a>BWMode VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine la façon dont une forme s’affiche pour les périphériques de sortie noir et blanc. En lecture/écriture. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :bwmode = " *expression* " >

**Remarques**

Quand une forme est imprimée sur une imprimante noir et blanc, ou affichée dans une vue en noir et blanc dans une application, plusieurs options sont possibles. Pour plus d’informations sur les valeurs de cet attribut, consultez la rubrique [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . La valeur par défaut est **auto**.

Si **auto** est spécifié, [BWNormal](msdn-online-vml-bwnormal-attribute.md) est utilisé pour déterminer le comportement de sortie noir et blanc normale, tandis que [BWPure](msdn-online-vml-bwpure-attribute.md) est utilisé pour déterminer le comportement de sortie en noir et blanc pur.

*Microsoft Office Attribut extensions*

**Exemple**

Le mode noir et blanc de la forme est **auto**.


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 