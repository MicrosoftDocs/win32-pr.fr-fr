---
title: ViewpointOrigin VML (attribut)
description: ViewpointOrigin VML (attribut)
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5e69357eddfe535b3c6164579454260d8f478430f7a9f1c7bede3262b1b040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007559"
---
# <a name="vml-viewpointorigin-attribute"></a>ViewpointOrigin VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit l’origine du point de vue dans le cadre englobant de la forme. En lecture/écriture. **VgVector2D**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : *Element* viewpointorigin = " *expression* " >

**Syntaxe du script**

*Element* . viewpointorigin = "*expression*"

*expression* = *élément*. viewpointorigin

**Remarques**

Définit le point de vue en fonction des valeurs x et y de la forme d’origine. Les valeurs x et y sont comprises entre 0,5 et-0,5 (50% à-50% de l’origine de la coordonnée de la forme). La valeur par défaut est 0, 0.

*Microsoft Office Attribut extensions*

 

 