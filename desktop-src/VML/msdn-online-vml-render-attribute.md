---
title: Attribut de rendu VML
description: Attribut de rendu VML
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17063d1e742a5b014e18d61d2d4290eb2511843ef24f1513bd3564ee83c5e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513339"
---
# <a name="vml-render-attribute"></a>Attribut de rendu VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

*Microsoft Office Attribut extensions*

 

 