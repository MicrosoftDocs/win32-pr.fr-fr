---
title: Attribut SRC (Stroke) (VML)
description: Attribut SRC (Stroke) (VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727541"
---
# <a name="src-attribute-strokevml"></a>Attribut SRC (Stroke) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit l’image source à charger pour un remplissage de trait. En lecture/écriture. **Chaîne**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* SRC = " *expression* " >

**Syntaxe du script**

*Element* . src = "*expression*"

*expression* = *élément*. SRC

**Remarques**

URL vers une image à charger pour les remplissages d’image et de motif. Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche. Si cet attribut apparaît seul, autrement dit, sans **href** ou **titre**, l’image est liée.

*Attribut standard VML*

**Exemple**

Le trait est créé avec l’image spécifiée par le fichier cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 