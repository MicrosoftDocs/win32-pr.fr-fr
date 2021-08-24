---
title: Attribut VML V
description: Attribut VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbf2f8654d32714d20e9b0c5a36fb939173698749569692120c04b89e84b6e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768329"
---
# <a name="vml-v-attribute"></a>Attribut VML V

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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





 

 