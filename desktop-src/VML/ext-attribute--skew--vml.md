---
title: Attribut ext (skew) (VML)
description: Attribut ext (skew) (VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199295"
---
# <a name="ext-attribute-skewvml"></a>Attribut ext (skew) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le mode d’affichage d’une inclinaison. En lecture/écriture. **Chaîne**.

**S’applique à**

[Appliquez](msdn-online-vml-skew-element.md)

**Syntaxe de balise**

<o : *Element* v :ext = " *expression* " >

**Syntaxe du script**

*Element* . ext = "*expression*"

*expression* = *élément*. ext

**Remarques**

Cet attribut est utilisé pour indiquer aux éditeurs graphiques comment traiter l’élément **skew** . Ces valeurs comprennent :

-   **edit**
-   **affichage** (par défaut)
-   **backwardCompatible**

Si une extension est définie sur **modifier**, elle peut être ignorée par une visionneuse de logiciel. Si la valeur est définie sur **View**, la visionneuse doit restituer la représentation bitmap à la place.

*Attribut extensions Microsoft Office*

 

 