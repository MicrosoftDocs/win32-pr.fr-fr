---
title: LockRotationCenter VML (attribut)
description: LockRotationCenter VML (attribut)
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511904"
---
# <a name="vml-lockrotationcenter-attribute"></a>LockRotationCenter VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si la rotation de l’objet extrudé est spécifiée par l’attribut [RotationAngle](msdn-online-vml-rotationangle-attribute.md) . En lecture/écriture. **VgTriState**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : *Element* lockrotationcenter = " *expression* " >

**Syntaxe du script**

*Element* . lockrotationcenter = "*expression*"

*expression* = *élément*. lockrotationcenter

**Remarques**

Si la **valeur est false**, la rotation est spécifiée par l’attribut [orientation](msdn-online-vml-orientation-attribute.md) . La valeur par défaut est **True**.

Notez les points suivants :


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



est identique à :


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Attribut extensions Microsoft Office*

 

 