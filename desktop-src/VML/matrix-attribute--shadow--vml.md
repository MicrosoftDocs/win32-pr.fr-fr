---
title: Attribut Matrix (Shadow) (VML)
description: Attribut Matrix (Shadow) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382676"
---
# <a name="matrix-attribute-shadowvml"></a>Attribut Matrix (Shadow) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit une transformation de perspective pour une ombre. En lecture/écriture. **Chaîne**.

**S’applique à**

[Shadow](msdn-online-vml-shadow-element.md)

**Syntaxe de balise**

<v : *Element* Matrix = " *expression* " >

**Syntaxe du script**

*Element* . Matrix = "*expression*"

*expression* = *élément*. Matrix

**Remarques**

Matrice de transformation de perspective sous la forme « Sxx, SXY, syx, SYY, PX, py » où s = Scale et p = perspective. Si le décalage est en unités absolues alors que PX, py est en unités de 1/UME ; Sinon, il s’agit d’une fraction inverse de la taille de la forme.

*Attribut standard VML*

 

 