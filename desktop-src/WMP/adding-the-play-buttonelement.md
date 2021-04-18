---
title: Ajout de Play BUTTONELEMENT
description: Ajout de Play BUTTONELEMENT
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- créer des apparences, BUTTONELEMENT, élément
- Apparences du lecteur Windows Media, BUTTONELEMENT, élément
- Skins, BUTTONELEMENT, élément
- fichiers de définition d’apparence, élément BUTTONELEMENT
- Élément BUTTONELEMENT
- éléments, BUTTONELEMENT
- création d’apparences, boutons de lecture
- Apparences du lecteur Windows Media, boutons de lecture
- apparences, boutons de lecture
- fichiers de définition d’apparence, boutons de lecture
- Boutons de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507247"
---
# <a name="adding-the-play-buttonelement"></a>Ajout de Play BUTTONELEMENT

Enfin, vous pouvez ajouter les éléments **BUTTONELEMENT** qui connectent les boutons visuels à l’écran aux actions du lecteur Windows Media. C’est le cœur de votre apparence et vous pouvez le considérer comme un câblage de la surface de l’apparence à la machine interne du lecteur Windows Media.

**BUTTONELEMENT** s sont contenus dans un **BUTTONGROUP**. Vous devez toujours avoir au moins un **BUTTONELEMENT** à l’intérieur de chaque **BUTTONGROUP**.

Placez le code de lecture de la **BUTTONELEMENT** après le crochet pointu fermant de **BUTTONGROUP**.


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



Les attributs suivants sont utilisés pour définir **BUTTONELEMENT** pour le bouton de lecture :

**mappingColor**

Il s’agit de la valeur de couleur d’une région dans le fichier art de mappage que vous avez créé précédemment. Dans ce cas, il s’agit de la couleur verte unie. Cet attribut est obligatoire pour tout **BUTTONELEMENT**. En définissant cette couleur, vous indiquez au lecteur Windows Media d’associer cette zone de couleur au code XML de ce bouton.

**Info-bulle**

Cela définit le texte qui s’affichera si l’utilisateur pointe la souris sur le bouton. Ne confondez pas cela avec l’image de survol qui sera affichée. Une info-bulle est une petite légende qui prend un moment pour apparaître. Toutefois, l’image de la pointe de survol apparaît instantanément dans la couleur et la forme de votre choix.

**onClick**

Cela définit l’événement qui se produit lorsque la souris clique sur le bouton. La valeur de cet attribut d’événement est appelée gestionnaire d’événements et sera soit une ligne de code Microsoft JScript, soit une fonction JScript dans un fichier texte externe qui est chargée par l’attribut **loadScript** d’une **vue**. Dans ce cas, le code JScript appelle la méthode d' **URL** du lecteur Windows Media, qui charge et démarre la lecture d’un fichier nommé « Laure. WMA ». Notez que la ligne se termine par un point-virgule à l’intérieur des guillemets, ce qui est une bonne pratique de codage JScript. Notez également l’utilisation de guillemets simples à l’intérieur des guillemets doubles pour définir le nom du fichier. Pour plus d’informations sur JScript, consultez [utilisation de JScript](using-jscript.md) dans la section à propos des apparences de ce kit de développement logiciel (SDK).

Notez qu’il n’y a pas de balise **BUTTONELEMENT** de fin. Si un élément ne délimite pas un autre élément, vous pouvez le fermer à l’aide de la barre oblique juste avant le Chevron fermant. Cela indique au XML que vous avez terminé avec cet élément. Par exemple,


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



et


```C++
<BUTTONELEMENT/>
```



transmettent les mêmes informations en XML.

La puissance des habillages provient de l’utilisation de gestionnaires d’événements. Si l’utilisateur effectue une opération avec une souris, vous pouvez gérer cet événement avec JScript. Votre code peut être une ligne unique qui fait une action simple pour le lecteur Windows Media, ou bien une application complète écrite en JScript.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du fichier de définition d’apparence**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




