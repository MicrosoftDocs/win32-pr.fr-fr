---
title: Attribut de commutateur VML
description: Attribut de commutateur VML
ms.assetid: fc099c0a-6789-41e8-ab08-36f4fd2d3bfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d102d6af20e698d8ec281cb1be6fae9690de4e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510260"
---
# <a name="vml-switch-attribute"></a>Attribut de commutateur VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si les directions du handle sont échangées. En lecture/écriture. **VgTriState**.

**S’applique à**

[H](msdn-online-vml-h-element.md) (sous-élément de [Handles](msdn-online-vml-handles-element.md))

**Syntaxe de balise**

<v : *élément* Switch = " *expression* " >

**Remarques**

Si la **valeur est true**, la poignée est basculée entre les directions x et y si la forme est plus grande que la largeur. La valeur par défaut est **False**.

Cet attribut est utilisé pour les formes avec un comportement d’étirement Limo.

*Attribut standard VML*

 

 