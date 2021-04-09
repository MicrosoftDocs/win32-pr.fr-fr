---
title: Attribut VML V
description: Attribut VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101832"
---
# <a name="vml-v-attribute"></a>Attribut VML V

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit les commandes qui composent un chemin d’accès. En lecture/écriture. **Chaîne**.

**S’applique à**

[Chemin d’accès](msdn-online-vml-path-element.md)

**Syntaxe de balise**

<v : *élément* v = « *expression* » >

**Syntaxe du script**

*Element* . v = "*expression*"

*expression* = *élément*. v

**Remarques**

Remplace l’attribut de **chemin d’accès** d’une forme. Les coordonnées peuvent être des nombres fixes, des nombres relatifs ou des références à des formules (en utilisant le format « @n », où n est un numéro de formule ; par exemple, « @2 » fait référence à la deuxième formule dans le tableau de formules).

*Attribut standard VML*

**Exemple**

Un rectangle est créé à l’aide de l’attribut **V** . Notez qu’une lettre minuscule L (commande **LineTo** ) est utilisée après le premier jeu de coordonnées délimitées par des virgules.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 