---
title: DoubleClickNotify VML (attribut)
description: DoubleClickNotify VML (attribut)
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9945f4391890f33d3569d1c1aed39a8ec5bbe4b0be29258da1cca4b7caf895da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124829"
---
# <a name="vml-doubleclicknotify-attribute"></a>DoubleClickNotify VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Envoie un message d’événement lors d’un double-clic sur une forme. En lecture/écriture. **VgTriState**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :doubleclicknotify = " *expression* " >

**Remarques**

La valeur par défaut est **false**, ce qui indique que l’événement ne sera pas déclenché.

*Microsoft Office Attribut extensions*

**Exemple**

La forme déclenche un événement de double-clic lorsque vous double-cliquez dessus.


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 