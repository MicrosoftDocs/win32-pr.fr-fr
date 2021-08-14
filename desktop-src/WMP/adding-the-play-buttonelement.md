---
title: Ajout de Play BUTTONELEMENT
description: Ajout de Play BUTTONELEMENT
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- créer des apparences, BUTTONELEMENT, élément
- habillages Lecteur Windows Media, élément BUTTONELEMENT
- Skins, BUTTONELEMENT, élément
- fichiers de définition d’apparence, élément BUTTONELEMENT
- Élément BUTTONELEMENT
- éléments, BUTTONELEMENT
- création d’apparences, boutons de lecture
- apparences de Lecteur Windows Media, boutons de lecture
- apparences, boutons de lecture
- fichiers de définition d’apparence, boutons de lecture
- Boutons de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab52691b48876327f45fbaf30a98de78c8c0c46a2eafd0a2c342e51c5a8683
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583543"
---
# <a name="adding-the-play-buttonelement"></a>Ajout de Play BUTTONELEMENT

enfin, vous pouvez ajouter les éléments **BUTTONELEMENT** qui connectent les boutons visuels à l’écran pour Lecteur Windows Media actions. c’est le cœur de votre peau et vous pouvez le considérer comme un câblage de la surface de la peau à la machine interne de Lecteur Windows Media.

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

Il s’agit de la valeur de couleur d’une région dans le fichier art de mappage que vous avez créé précédemment. Dans ce cas, il s’agit de la couleur verte unie. Cet attribut est obligatoire pour tout **BUTTONELEMENT**. en définissant cette couleur, vous indiquez Lecteur Windows Media pour associer cette zone de couleur au code XML de ce bouton.

**Info-bulle**

Cela définit le texte qui s’affichera si l’utilisateur pointe la souris sur le bouton. Ne confondez pas cela avec l’image de survol qui sera affichée. Une info-bulle est une petite légende qui prend un moment pour apparaître. Toutefois, l’image de la pointe de survol apparaît instantanément dans la couleur et la forme de votre choix.

**onClick**

Cela définit l’événement qui se produit lorsque la souris clique sur le bouton. la valeur de cet attribut d’événement est appelée un gestionnaire d’événements et sera soit une ligne de code JScript Microsoft, soit une fonction JScript dans un fichier texte externe qui est chargé par l’attribut **loadScript** d’une **vue**. dans ce cas, le code JScript appelle la méthode **URL** de Lecteur Windows Media, qui charge et commence à exécuter un fichier nommé « laure. wma ». notez que la ligne se termine par un point-virgule à l’intérieur des guillemets, ce qui constitue une bonne pratique de codage JScript. Notez également l’utilisation de guillemets simples à l’intérieur des guillemets doubles pour définir le nom du fichier. pour plus d’informations sur JScript, consultez [utilisation de JScript](using-jscript.md) dans la section à propos des apparences de ce kit de développement logiciel (SDK).

Notez qu’il n’y a pas de balise **BUTTONELEMENT** de fin. Si un élément ne délimite pas un autre élément, vous pouvez le fermer à l’aide de la barre oblique juste avant le Chevron fermant. Cela indique au XML que vous avez terminé avec cet élément. Par exemple,


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



et


```C++
<BUTTONELEMENT/>
```



transmettent les mêmes informations en XML.

La puissance des habillages provient de l’utilisation de gestionnaires d’événements. Si l’utilisateur effectue une opération avec une souris, vous pouvez gérer cet événement avec JScript. votre code peut être une ligne unique qui fait de Lecteur Windows Media effectuer une opération simple, telle que la lecture, ou il peut s’agir d’une application complète écrite en JScript.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du fichier de définition d’apparence**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




