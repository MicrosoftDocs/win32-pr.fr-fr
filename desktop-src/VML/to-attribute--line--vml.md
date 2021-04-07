---
title: To, attribut (Line) (VML)
description: To, attribut (Line) (VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730132"
---
# <a name="to-attribute-linevml"></a>To, attribut (Line) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le point de fin d’une ligne. En lecture/écriture. **VgVector2D**.

**S’applique à**

[Ligne](msdn-online-vml-line-element.md)

**Syntaxe de balise**

<v : *Element* to = " *expression* " >

**Syntaxe du script**

*Element* . to = "*expression*"

*expression* = *élément*. to

**Remarques**

Définit le point de fin de la ligne dans l’espace de coordonnées de l’élément parent. Si le parent n’est pas un élément VML, l' [unité](msdn-online-vml-units.md) par défaut est un pixel (mais dans, cm, mm, PT, PC peut également être spécifié). La valeur par défaut est 10, 10.

**Attribut standard VML**

**Exemple**

La ligne se termine à un emplacement de 100 points et 100 pointe vers la droite de l’angle supérieur gauche de l’espace parent.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 