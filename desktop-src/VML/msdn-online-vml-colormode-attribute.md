---
title: Attribut ColorMode de VML
description: Attribut ColorMode de VML
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7126a3f5a95910eb85007fe9a80d500c5233e5e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382172"
---
# <a name="vml-colormode-attribute"></a>Attribut ColorMode de VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine le mode de couleur de l’extrusion. En lecture/écriture. **VgTriState**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : *Element* ColorMode = " *expression* " >

**Syntaxe du script**

*Element* . ColorMode = "*expression*"

*expression* = *élément*. ColorMode

**Remarques**

Ces valeurs comprennent :



| Valeur  | Description                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| auto   | Spécifie que la couleur de l’extrusion est identique à la couleur de remplissage de la forme. Par défaut.                |
| custom | Spécifie que l’extrusion sera la couleur de l’attribut [Color](color-attribute--extrusion--vml.md) . |



 

*Attribut extensions Microsoft Office*

 

 