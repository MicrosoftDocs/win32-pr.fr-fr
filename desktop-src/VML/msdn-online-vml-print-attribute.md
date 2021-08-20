---
title: Attribut d’impression VML
description: Attribut d’impression VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfa364e573d887da2013f946ddf23e0a974e0f63211623de3d2046b0525b2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057727"
---
# <a name="vml-print-attribute"></a>Attribut d’impression VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si la forme sera imprimée. En lecture/écriture. [VgTriState](msdn-online-vml-vgtristate.md).

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *élément* Print = " *expression* " >

**Syntaxe du script**

*Element* . Print = "*expression*"

*expression* = *élément*. Print

**Remarques**

Fourni comme moyen de spécifier si les formes seront imprimées. Notez qu’une forme peut toujours être affichée sur l’écran, même si elle n’est pas imprimée suite à l’affichage de cet attribut avec la **valeur false**. La valeur par défaut est **True**.

cet attribut est utilisé par Microsoft Office mais n’est pas utilisé par Microsoft Internet Explorer.

*Microsoft Office Attribut extensions*

 

 