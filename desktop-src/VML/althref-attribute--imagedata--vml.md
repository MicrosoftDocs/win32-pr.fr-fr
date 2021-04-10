---
title: Attribut AltHRef (ImageData) (VML)
description: Attribut AltHRef (ImageData) (VML)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031426"
---
# <a name="althref-attribute-imagedatavml"></a>Attribut AltHRef (ImageData) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

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

*Attribut extensions Microsoft Office*

 

 