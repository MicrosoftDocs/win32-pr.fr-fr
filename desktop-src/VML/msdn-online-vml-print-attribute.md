---
title: Attribut d’impression VML
description: Attribut d’impression VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509035"
---
# <a name="vml-print-attribute"></a>Attribut d’impression VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si la forme sera imprimée. En lecture/écriture. [VgTriState](msdn-online-vml-vgtristate.md).

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *élément* Print = " *expression* " >

**Syntaxe du script**

*Element* . Print = "*expression*"

*expression* = *élément*. Print

**Remarques**

Fourni comme moyen de spécifier si les formes seront imprimées. Notez qu’une forme peut toujours être affichée sur l’écran, même si elle n’est pas imprimée suite à l’affichage de cet attribut avec la **valeur false**. La valeur par défaut est **True**.

Cet attribut est utilisé par Microsoft Office mais n’est pas utilisé par Microsoft Internet Explorer.

*Attribut extensions Microsoft Office*

 

 