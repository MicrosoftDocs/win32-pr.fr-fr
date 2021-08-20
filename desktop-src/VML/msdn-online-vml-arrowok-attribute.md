---
title: ArrowOK VML (attribut)
description: ArrowOK VML (attribut)
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95b8fa7068f55246263e6622527a8ecec17d3351c284a0810cd77b085784aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124968"
---
# <a name="vml-arrowok-attribute"></a>ArrowOK VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si les flèches sont affichées. En lecture/écriture. **VgTriState**.

**S’applique à**

[Chemin d’accès](msdn-online-vml-path-element.md)

**Syntaxe de balise**

<v : *Element* arrowok = " *expression* " >

**Syntaxe du script**

*Element* . arrowok = "*expression*"

*expression* = *élément*. arrowok

**Remarques**

Si la **valeur est false**, le chemin d’accès ne contient pas de pointe de flèche. La valeur par défaut est **False**. Cet attribut remplace tous les autres attributs de la flèche dans l’élément parent ou **Stroke** .

*Attribut standard VML*

**Exemple**

Le chemin d’accès n’a pas de flèche.


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 