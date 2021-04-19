---
title: Attribut de rendu VML
description: Attribut de rendu VML
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70872e823a2d43d6a605fbf07a817473b19a125a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511504"
---
# <a name="vml-render-attribute"></a>Attribut de rendu VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le mode de rendu de l’extrusion. En lecture/écriture. **Chaîne**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : *élément* Render = " *expression* " >

**Syntaxe du script**

*Element* . Render = "*expression*"

*expression* = *élément*. Render

**Remarques**

Ces valeurs comprennent :



| Valeur        | Description                                                   |
|--------------|---------------------------------------------------------------|
| Solid        | Le rendu affiche une forme unie. Par défaut.                    |
| Wireframe    | Le rendu affiche une forme filaire.                         |
| boundingcube | Le rendu affiche le cube englobant qui contient la forme. |



 

*Attribut extensions Microsoft Office*

 

 