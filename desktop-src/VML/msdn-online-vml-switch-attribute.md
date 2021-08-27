---
title: Attribut de commutateur VML
description: Attribut de commutateur VML
ms.assetid: fc099c0a-6789-41e8-ab08-36f4fd2d3bfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2205f83449b09c22314c81ed460bee8410a3873e8f5550c073d7f3a1c1e8c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123891"
---
# <a name="vml-switch-attribute"></a>Attribut de commutateur VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si les directions du handle sont échangées. En lecture/écriture. **VgTriState**.

**S’applique à**

[H](msdn-online-vml-h-element.md) (sous-élément de [Handles](msdn-online-vml-handles-element.md))

**Syntaxe de balise**

<v : *élément* Switch = " *expression* " >

**Remarques**

Si la **valeur est true**, la poignée est basculée entre les directions x et y si la forme est plus grande que la largeur. La valeur par défaut est **False**.

Cet attribut est utilisé pour les formes avec un comportement d’étirement Limo.

*Attribut standard VML*

 

 