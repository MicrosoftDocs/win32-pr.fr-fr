---
title: Attribut Stroke VML
description: Attribut Stroke VML
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102273"
---
# <a name="vml-stroked-attribute"></a>Attribut Stroke VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit si le chemin d’accès doit être rayé. En lecture/écriture. [VgTriState](msdn-online-vml-vgtristate.md) .

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *élément* rayé = " *expression* " >

**Syntaxe du script**

*Element* . stroked = "*expression*"

*expression* = *élément*. traitd

**Remarques**

La valeur est dupliquée à partir de l’attribut **on** de l’élément [Stroke](msdn-online-vml-stroke-element.md) .

*Attribut standard VML*

**Exemple**

Le tracé de la forme est rayé.


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemple d’attribut rayé](/previous-versions/bb264094(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 