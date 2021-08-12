---
title: Attribut ColorMode de VML
description: Attribut ColorMode de VML
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81b9b8699ac4806d47581f166dace38f8f724b015b25d18807caa48b44b283e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602140"
---
# <a name="vml-colormode-attribute"></a>Attribut ColorMode de VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

*Microsoft Office Attribut extensions*

 

 