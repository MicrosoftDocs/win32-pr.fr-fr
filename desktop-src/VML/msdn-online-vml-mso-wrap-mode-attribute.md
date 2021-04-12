---
title: VML DCL-attribut de mode habillage
description: VML DCL-attribut de mode habillage
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315599"
---
# <a name="vml-mso-wrap-mode-attribute"></a>VML DCL-attribut de mode habillage

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le mode d’habillage pour le texte. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "mso-Wrap-mode : *expression* " >

**Remarques**

Ces valeurs comprennent :



| Valeur          | Description                          |
|----------------|--------------------------------------|
| square         | Encapsule le texte autour de la forme dans un carré. |
| raccords          | Le texte est renvoyé à la fin de la forme.  |
| haut et bas | Le texte se déplace de haut en bas.       |
| jusqu'à        | Le texte s’affiche dans la forme.     |
| aucun           | Le texte n’est pas renvoyé à la ligne.                   |



 

Utilisé par Microsoft PowerPoint pour l’enregistrement au format HTML pour indiquer si le retour automatique à la ligne dans une forme automatique est activé (**carré**) ou désactivé (**aucun**).

*Attribut extensions Microsoft Office*

**Exemple**

Le code suivant indique que les retours automatique à l’intérieur d’une forme automatique sont activés dans PowerPoint.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 