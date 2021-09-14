---
title: À propos des objets MediaCollection et Media
description: À propos des objets MediaCollection et Media
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Lecteur Windows Media, objet MediaCollection
- Lecteur Windows Media modèle objet, objet MediaCollection
- modèle objet, objet MediaCollection
- Lecteur Windows Media ActiveX contrôle, objet MediaCollection
- contrôle ActiveX, objet MediaCollection
- Lecteur Windows Media contrôle Mobile ActiveX, objet MediaCollection
- Lecteur Windows Media Mobile, objet MediaCollection
- Objet MediaCollection
- Lecteur Windows Media, objet multimédia
- Lecteur Windows Media modèle objet, objet multimédia
- modèle objet, objet Media
- Lecteur Windows Media ActiveX contrôle, objet multimédia
- contrôle ActiveX, objet Media
- Lecteur Windows Media contrôle Mobile ActiveX, objet Media
- Lecteur Windows Media Mobile, objet multimédia
- Objet Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232901"
---
# <a name="about-the-mediacollection-and-media-objects"></a>À propos des objets MediaCollection et Media

les objets **MediaCollection** et **media** gouvernent la collection de supports, qui définit les emplacements des fichiers multimédias numériques auxquels Lecteur Windows Media peut accéder. Vous récupérez l’objet **MediaCollection** à partir de la propriété **MediaCollection** de l’objet **Player** . La propriété **mediaCollection** retourne l’objet **mediaCollection** . Vous pouvez uniquement accéder aux propriétés de l’objet **MediaCollection** après l’avoir créé. Par exemple, pour ajouter un objet **multimédia** (une chanson), utilisez le code suivant :


```C++
player.mediacollection.add('laure.wma');

```



Vous avez ajouté le fichier Laure. WMA à la collection de supports.

Vous pouvez récupérer l’objet **multimédia** en cours à l’aide de la propriété **currentMedia** du **lecteur**. Par exemple, ce code obtient la propriété **Duration** de l’objet **média** actuel :


```C++
myduration = player.currentmedia.duration;

```



Il existe de nombreuses façons d’obtenir un objet **multimédia** afin de pouvoir accéder à ses propriétés. Par exemple, si vous souhaitez accéder à la propriété **Duration** du média actuel, chacune des lignes de code suivantes peut être utilisée.

Pour connaître la durée du média en cours de diffusion :


```C++
player.currentMedia.duration;

```



Pour obtenir la durée du média actuel dans une sélection :


```C++
player.controls.currentItem.duration;

```



Pour obtenir la durée du troisième élément multimédia dans une sélection :


```C++
player.currentPlaylist.item(2).duration;

```



Pour obtenir la durée du troisième élément multimédia dans un genre « jazz » :


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



Pour connaître la durée du troisième élément multimédia de la deuxième sélection :


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Modèle objet de lecteur pour les langages de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




