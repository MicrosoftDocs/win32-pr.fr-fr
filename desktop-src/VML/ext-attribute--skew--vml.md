---
title: Attribut ext (skew) (VML)
description: Attribut ext (skew) (VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a001812a5504940509fac82333b2ca637ae76a913218f44cd3a06b4c18bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125359"
---
# <a name="ext-attribute-skewvml"></a>Attribut ext (skew) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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

*Microsoft Office Attribut extensions*

 

 