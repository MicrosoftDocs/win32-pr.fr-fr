---
title: Attribut points VML
description: Attribut points VML
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031335"
---
# <a name="vml-points-attribute"></a>Attribut points VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit un ensemble de points qui composent une polyligne. En lecture/écriture. [IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .

**S’applique à**

[Polyligne](msdn-online-vml-polyline-element.md)

**Syntaxe de balise**

<v : *Element* points = " *expression* " >

**Syntaxe du script**

*Element* . points = "*expression * * *"**

*expression* = *Element*. points

**Remarques**

Définit un ensemble de segments de ligne droite composés d’une série de points. Si le parent n’est pas un élément VML, l' [unité](msdn-online-vml-units.md) par défaut est un pixel (mais dans, cm, mm, PT, PC peut également être spécifié). La valeur par défaut est « 0, 0 10, 10 ». Notez que les virgules ne sont pas requises, mais qu’elles facilitent la lisibilité.

*Attribut standard VML*

**Exemple**

La polyligne commence au point 10, 10 et se termine à 100 100, avec les valeurs de points.


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 