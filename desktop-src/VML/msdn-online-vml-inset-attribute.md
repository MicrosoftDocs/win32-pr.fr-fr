---
title: Attribut incrusté VML
description: Attribut incrusté VML
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101796"
---
# <a name="vml-inset-attribute"></a>Attribut incrusté VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Spécifie les valeurs de marge intérieure pour le texte de zone de texte. En lecture/écriture. **Chaîne**.

**S’applique à**

[TextBox](msdn-online-vml-textbox-element.md)

**Syntaxe de balise**

<v : *élément* incrusté = " *expression* " >

**Syntaxe du script**

*Element* . incrusté = "*expression*"

*expression* = *élément*. incrusté

**Remarques**

La valeur de marge de texte interne est spécifiée sous la forme d’une chaîne contenant quatre valeurs, séparées par des virgules ou des espaces. Les valeurs mesurent les incrustations à partir des bords gauche, supérieur, droit et inférieur de la zone spécifiée par l’attribut [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) de **path**. Les valeurs manquantes sont définies sur la valeur par défaut, soit « 0.1 in, 0,05 dans, 0.1 in, 0,05 dans ».

Pour les formes pivotées dans des navigateurs qui ne prennent pas en charge la rotation, le cadre englobant sera aligné sur le multiple le plus proche de 90 degrés.

*Attribut standard VML*

**Exemple**

La zone de texte aura une marge en incrustation de 10 pixels.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 