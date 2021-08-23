---
title: Attribut Matrix (Shadow) (VML)
description: Attribut Matrix (Shadow) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6124005ef3202e11dc8a4e7eeeaacba8e87e9c3a7cb3a1dd1eee55c595e40ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057927"
---
# <a name="matrix-attribute-shadowvml"></a>Attribut Matrix (Shadow) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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

 

 