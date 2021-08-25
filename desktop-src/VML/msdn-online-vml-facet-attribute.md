---
title: Attribut de facette VML
description: Attribut de facette VML
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b1ae12ba31d286f1e029dcd433820e8c50acb05c86a92b2c06e1df50c73a0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681009"
---
# <a name="vml-facet-attribute"></a>Attribut de facette VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le nombre de facettes utilisées pour décrire les surfaces courbes d’une extrusion. En lecture/écriture. **VgNumber**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : *élément* facette = " *expression* " >

**Syntaxe du script**

*Element* . facette = "*expression*"

*expression* = *élément*. facette

**Remarques**

Définit la façon dont un moteur de rendu se rapproche de l’extrusion. Un nombre inférieur indique une tolérance de rendu inférieure pour le moteur de rendu et génère plus de facettes. Des nombres plus élevés feront apparaître l’extrusion plus à facettes. La valeur par défaut est 30 000.

*Microsoft Office Attribut extensions*

 

 