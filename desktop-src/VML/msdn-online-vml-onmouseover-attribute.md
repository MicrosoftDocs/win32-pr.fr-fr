---
title: Attribut VML OnMouseOver
description: Attribut VML OnMouseOver
ms.assetid: 68f0fa7a-0d22-4ede-8404-e007296960e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d2bb65864987988996cfad710360fd908a5248c11857e8df1eb5a941b1b895b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999129"
---
# <a name="vml-onmouseover-attribute"></a>Attribut VML OnMouseOver

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Déclenche un événement de souris pour une forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* onmouseover = " *expression* " >

**Remarques**

Un événement « MouseOver » est généré lorsque le pointeur de la souris se trouve sur la forme. La valeur est générée à l’aide du mot clé **This** (en tant que référence à l’objet) suivi de la syntaxe du modèle objet. Par exemple, pour modifier la couleur de remplissage en rouge, utilisez la commande suivante :

onmouseover = "This. FillColor = 'Red'"

Notez l’utilisation de guillemets simples et doubles pour définir l’expression.

*Attribut standard VML*

**Exemple**

Lorsque le pointeur de la souris se trouve sur la forme, la couleur de remplissage passe du rouge au vert.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20"
   onmouseover='this.fillcolor="green"'>
   </v:rect>
```



[Exemple d’attribut onmouseover](/previous-versions/bb264088(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 