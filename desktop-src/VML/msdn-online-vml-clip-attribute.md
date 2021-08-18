---
title: Attribut de clip VML
description: Attribut de clip VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cab4afdef2a10c9c6f6a0561dedf5b4df3538a97152cb53181452b8ac531bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999289"
---
# <a name="vml-clip-attribute"></a>Attribut de clip VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si le découpage est activé. En lecture/écriture. **VgTriState**.

**S’applique à**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Syntaxe de balise**

<v : *Element* clip = " *expression* " >

**Syntaxe du script**

*Element* . clip = "*expression*"

*expression* = *élément*. clip

**Remarques**

Si **clip** a la **valeur false**, la forme est mise à l’échelle pour s’ajuster au cadre. Si la **valeur est true**, toutes les parties de la forme qui sont en dehors du frame ne seront pas affichées.

Notez que [origin](origin-attribute--vmlframe--vml.md) et [Size](size-attribute--vmlframe.md) ne sont pas utilisés, sauf si **clip** a la **valeur true**.

*Attribut standard VML*

**Exemple**

L’image définie dans le fichier externe sera découpée.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 