---
title: Attribut métallique VML
description: Attribut métallique VML
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58b137dd2f874333bb618d1b892632abb5a679d5b533b924a73416ff38732e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867189"
---
# <a name="vml-metal-attribute"></a>Attribut métallique VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si la surface de la forme extrudée est semblable à Metal. En lecture/écriture. **VgTriState**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : *élément* Metal = " *expression* " >

**Syntaxe du script**

*Element* . Metal = "*expression*"

*expression* = *élément*. Metal

**Remarques**

Si la valeur est **true**, cet attribut fait que le modèle éclairé réfléchi est la couleur matérielle au lieu de la couleur de la source de lumière, ce qui rend l’objet plus métallique. Pour rapprocher davantage un matériel métallique, specularity doit être relativement élevé (environ 1,2) et la diffusion est relativement faible (environ 0,6). La valeur par défaut est **False**.

*Microsoft Office Attribut extensions*

 

 