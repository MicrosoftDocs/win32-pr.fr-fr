---
title: ID, attribut (VMLFrame) (VML)
description: ID, attribut (VMLFrame) (VML)
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031454"
---
# <a name="id-attribute-vmlframevml"></a>ID, attribut (VMLFrame) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit un identificateur unique pour le frame. En lecture/écriture. **Chaîne**.

**S’applique à**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Syntaxe de balise**

<v : *élément* ID = « *expression* » >

**Syntaxe du script**

*Element* . ID = "*expression*"

*expression* = *élément*. ID

**Remarques**

Utilisez l' **ID** pour référencer un frame. Par exemple, vous pouvez déplacer le cadre sur la page en modifiant la position de cadre référencée par l' **ID**.

*Attribut standard VML*

**Exemple**

L' **ID** du frame est « frame01 ».


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 