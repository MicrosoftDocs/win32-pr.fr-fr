---
title: InvY VML (attribut)
description: InvY VML (attribut)
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d012e8ac6afe0e7808236c36d8dd3088ce9fa3552b4b7efa0542ea8612e4d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599867"
---
# <a name="vml-invy-attribute"></a>InvY VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si la position y du handle est inversée. En lecture/écriture. **VgTriState**.

**S’applique à**

[H](msdn-online-vml-h-element.md) (sous-élément de [Handles](msdn-online-vml-handles-element.md))

**Syntaxe de balise**

<v : *Element* invy = " *expression* " >

**Remarques**

Si la valeur est **true**, la position y du handle est inversée en soustrayant la valeur y de la valeur y de **CoordOrigin** ajoutée à la valeur y de **CoordSize**. La valeur par défaut est **False**.

Cet attribut est l’équivalent de


```HTML
coordorigin.y + coordsize.y - h.position.y
```



*Attribut standard VML*

 

 