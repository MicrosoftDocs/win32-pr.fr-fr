---
title: Attribut AltHRef (ImageData) (VML)
description: Attribut AltHRef (ImageData) (VML)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca832ab684c2f3dd2efaa6b34343df11be75118cc797b16fece671d430f866fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137062"
---
# <a name="althref-attribute-imagedatavml"></a>Attribut AltHRef (ImageData) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Spécifie une autre référence pour une image. En lecture/écriture. **Chaîne**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *Element* o :althref = " *expression* " >

**Syntaxe du script**

*Element* . althref = "*expression*"

*expression* = *élément*. althref

**Remarques**

Prend en charge la préservation des données PICT via des roundtripping HTML. Lors de l’écriture HTML, l’autre représentation (c’est-à-dire, les données PICT d’origine si le fichier provient du Macintosh) est enregistrée. Sur une lecture HTML, **AltHRef** est privilégié sur **src**.

*Microsoft Office Attribut extensions*

 

 