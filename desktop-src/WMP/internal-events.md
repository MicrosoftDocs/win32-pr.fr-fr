---
title: Événements internes
description: Événements internes
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- apparences de Lecteur Windows Media, événements internes
- apparences, événements internes
- événements, internes
- écriture de code pour les apparences, événements internes
- événements internes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8859ed86cb4951509d452b24c108e73d4129e474abf1c0bc2f51487e2d42bd9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572519"
---
# <a name="internal-events"></a>Événements internes

vous pouvez détecter les modifications qui se produisent dans Lecteur Windows Media ou les modifications de votre propre apparence. il peut s’agir de modifications apportées aux propriétés ou méthodes de l’objet Lecteur Windows Media, aux modifications apportées aux attributs d’apparence, etc.

## <a name="windows-media-player-property-changes"></a>Lecteur Windows Media Modifications des propriétés

vous pouvez traiter les modifications apportées à Lecteur Windows Media à l’aide de l’écouteur wmpprop. Vous devez configurer l’écouteur en tant que valeur d’un attribut. Placez la valeur entre guillemets doubles et commencez par le mot « wmpprop » suivi d’un signe deux-points. Vous incluez ensuite la propriété que vous souhaitez écouter. Lorsque la propriété change, la valeur de l’attribut change également. Par exemple, pour que la valeur d’un élément Slider change à chaque modification de la valeur de l’attribut **CurrentPosition** , tapez la commande suivante :


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **Important** n’utilisez pas wmpprop sur les méthodes Lecteur Windows Media. Des résultats inattendus peuvent se produire.

## <a name="windows-media-player-method-changes"></a>Lecteur Windows Media Modifications de méthode

vous pouvez faire en sorte que votre apparence réponde à la disponibilité des méthodes sur Lecteur Windows Media à l’aide de wmpenabled et wmpdisabled. Celles-ci sont utilisées de la même façon que l’écouteur wmpprop, à ceci près que vous pouvez uniquement les utiliser sur les méthodes de l’objet de **contrôle** qui sont prises en charge par la méthode **isAvailable** .

Par exemple, vous pouvez activer un bouton uniquement lorsque la méthode **Play** est activée, à l’aide d’un code similaire à celui-ci :


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **Important** n’utilisez pas wmpenabled ou wmpdisabled sur les propriétés de Lecteur Windows Media. Des résultats inattendus peuvent se produire.

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



vous assignerez ensuite une chaîne de JScript que vous souhaitez exécuter lorsque la valeur change. par exemple, pour répondre à une modification de la valeur d’une zone de texte qui peut être utilisée pour ajuster le volume de Lecteur Windows Media, tapez la commande suivante à l’intérieur de votre élément de **texte** en tant qu’attribut :


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des événements**](handling-events.md)
</dt> </dl>

 

 




