---
title: Attribut HRef (Shape) (VML)
description: Attribut HRef (Shape) (VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031766"
---
# <a name="href-attribute-shapevml"></a>Attribut HRef (Shape) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit une URL pour une forme. Lorsque l’utilisateur clique sur la forme, le navigateur charge l’URL. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* href = " *expression* " >

**Syntaxe du script**

*Element* . href = "*expression*"

*expression* = *élément*. href

**Remarques**

L’attribut **href** est similaire à l’attribut HTML **href** standard des points d’ancrage.

L’utilisation de la fonction **href** vous permet de créer facilement des boutons intéressants sur une page Web.

*Attribut standard VML*

**Exemple**

Quand vous cliquez sur le rectangle, le navigateur charge la page d’accueil de Microsoft Corporation.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[Exemple d’attribut href](/previous-versions/bb229672(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 