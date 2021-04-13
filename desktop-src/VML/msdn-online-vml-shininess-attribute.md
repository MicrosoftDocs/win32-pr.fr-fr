---
title: Attribut brillance VML
description: Attribut brillance VML
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a116adeb955c0f3449b374947a3f8121bd848e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315227"
---
# <a name="vml-shininess-attribute"></a>Attribut brillance VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la concentration de la lumière réfléchie sur une surface d’extrusion. En lecture/écriture. **VgNumber**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : *élément* brillance = " *expression* " >

**Syntaxe du script**

*Element* . brillance = "*expression*"

*expression* = *Element*. brillance

**Remarques**

Les valeurs élevées (8-10) se rapprochent de la brillance d’un miroir et les valeurs basses (2-3) se rapprochent d’un effet flou. Les valeurs de 4-7 sont standard. Les réflexions ne reflètent pas les autres objets ; seules les sources de lumière de repérage sont reflétées. La valeur par défaut est 5.

*Attribut extensions Microsoft Office*

 

 