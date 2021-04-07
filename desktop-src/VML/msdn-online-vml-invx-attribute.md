---
title: InvX VML (attribut)
description: InvX VML (attribut)
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728076"
---
# <a name="vml-invx-attribute"></a>InvX VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si la position x du handle est inversée. En lecture/écriture. **VgTriState**.

**S’applique à**

[H](msdn-online-vml-h-element.md) (sous-élément de [Handles](msdn-online-vml-handles-element.md))

**Syntaxe de balise**

<v : *Element* INVX = " *expression* " >

**Remarques**

Si la valeur est **true**, la position x du handle est inversée en soustrayant la valeur x de la valeur x de **CoordOrigin** ajoutée à la valeur x de **CoordSize**. La valeur par défaut est **False**.

Cet attribut est l’équivalent de

coordorigin. x + coordsize. x-h. position. x

*Attribut standard VML*

 

 