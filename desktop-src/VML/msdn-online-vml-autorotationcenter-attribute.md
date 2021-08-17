---
title: AutoRotationCenter VML (attribut)
description: AutoRotationCenter VML (attribut)
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54b363b34a6b2f943be45d457e252eebcf597afd7f82b7992cf151b0c2eda4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347101"
---
# <a name="vml-autorotationcenter-attribute"></a>AutoRotationCenter VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si le centre de rotation sera le centre géométrique de l’extrusion. En lecture/écriture. **VgTriState**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : *Element* autorotationcenter = " *expression* " >

**Syntaxe du script**

*Element* . autorotationcenter = "*expression*"

*expression* = *élément*. autorotationcenter

**Remarques**

Le centre géométrique d’une forme extrudée est 0, 0,0. Si la valeur de cet attribut est **false**, le centre de rotation est déterminé par l’attribut [RotationCenter](msdn-online-vml-rotationcenter-attribute.md) . La valeur par défaut est **False**.

*Microsoft Office Attribut extensions*

 

 