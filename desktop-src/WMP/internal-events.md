---
title: Événements internes
description: Événements internes
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Apparences du lecteur Windows Media, événements internes
- apparences, événements internes
- événements, internes
- écriture de code pour les apparences, événements internes
- événements internes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939748"
---
# <a name="internal-events"></a>Événements internes

Vous pouvez détecter les modifications qui se produisent dans le lecteur Windows Media ou les modifications apportées à votre propre apparence. Ces modifications peuvent être apportées aux propriétés ou méthodes de l’objet lecteur Windows Media, aux modifications apportées aux attributs d’apparence, etc.

## <a name="windows-media-player-property-changes"></a>Modifications des propriétés du lecteur Windows Media

Vous pouvez traiter les modifications dans le lecteur Windows Media à l’aide de l’écouteur wmpprop. Vous devez configurer l’écouteur en tant que valeur d’un attribut. Placez la valeur entre guillemets doubles et commencez par le mot « wmpprop » suivi d’un signe deux-points. Vous incluez ensuite la propriété que vous souhaitez écouter. Lorsque la propriété change, la valeur de l’attribut change également. Par exemple, pour que la valeur d’un élément Slider change à chaque modification de la valeur de l’attribut **CurrentPosition** , tapez la commande suivante :


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **Important** N’utilisez pas wmpprop sur les méthodes du lecteur Windows Media. Des résultats inattendus peuvent se produire.

## <a name="windows-media-player-method-changes"></a>Modifications de la méthode du lecteur Windows Media

Vous pouvez faire en sorte que votre apparence réponde à la disponibilité des méthodes sur le lecteur Windows Media à l’aide de wmpenabled et wmpdisabled. Celles-ci sont utilisées de la même façon que l’écouteur wmpprop, à ceci près que vous pouvez uniquement les utiliser sur les méthodes de l’objet de **contrôle** qui sont prises en charge par la méthode **isAvailable** .

Par exemple, vous pouvez activer un bouton uniquement lorsque la méthode **Play** est activée, à l’aide d’un code similaire à celui-ci :


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **Important** N’utilisez pas wmpenabled ou wmpdisabled sur les propriétés du lecteur Windows Media. Des résultats inattendus peuvent se produire.

## <a name="skin-attribute-changes"></a>Modifications des attributs d’apparence

Vous pouvez répondre aux modifications apportées à vos attributs d’apparence de l’une des deux manières suivantes : à l’aide de wmpprop ou de l’événement **\_ OnChange** .

Vous pouvez utiliser wmpprop pour écouter les modifications apportées à votre propre apparence. Par exemple, pour afficher la valeur de curseur dans une zone de texte, vous pouvez taper la commande suivante :


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



Vous pouvez utiliser l’événement **\_ OnChange** pour traiter les événements à l’intérieur d’un élément. Vous devez joindre le nom de l’attribut que vous souhaitez suivre à **\_ OnChange**. Par exemple, si vous souhaitez suivre la valeur d’une zone de texte, vous devez taper :


```C++
value_onchange

```



Vous assignerez ensuite une chaîne JScript que vous souhaitez exécuter lorsque la valeur change. Par exemple, pour répondre à une modification de la valeur d’une zone de texte qui peut être utilisée pour ajuster le volume du lecteur Windows Media, tapez la commande suivante à l’intérieur de votre élément de **texte** en tant qu’attribut :


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des événements**](handling-events.md)
</dt> </dl>

 

 




