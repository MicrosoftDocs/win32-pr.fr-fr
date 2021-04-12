---
title: ForceDash VML (attribut)
description: ForceDash VML (attribut)
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031550"
---
# <a name="vml-forcedash-attribute"></a>ForceDash VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si un contour en pointillés est utilisé pour dessiner une forme lorsqu’une forme n’a pas de trait ou de remplissage. En lecture/écriture. **VgTriState**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :forcedash = " *expression* " >

**Remarques**

Utilisé par les espaces réservés Microsoft PowerPoint pour dessiner un contour en pointillés lorsqu’il n’y a pas de ligne et aucun remplissage pour une forme. La valeur par défaut est **False**. Si la **valeur est true**, un contour en pointillés est utilisé pour indiquer un espace réservé.

*Attribut extensions Microsoft Office*

**Exemple**

Une ligne en pointillés est utilisée pour afficher la forme en l’absence de ligne ou de remplissage.


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 