---
title: utilisation du modèle objet Lecteur Windows Media 7 ou version ultérieure
description: utilisation du modèle objet Lecteur Windows Media 7 ou version ultérieure
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Lecteur Windows Media, modèle objet
- Lecteur Windows Media modèle objet, version 7 ou ultérieure
- modèle objet, version 7 ou ultérieure
- Lecteur Windows Media contrôle ActiveX, version 7 ou ultérieure
- contrôle ActiveX, version 7 ou ultérieure
- Lecteur Windows Media contrôle de ActiveX Mobile, version 7 ou ultérieure
- Lecteur Windows Media Mobile, modèle objet
- Guide de migration, version 7 ou ultérieure
- versions de Lecteur Windows Media, modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa40dea2718c602bfae305703913b418d0f8a48b90278683aba099dfe0d703bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117027"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a>utilisation du modèle objet Lecteur Windows Media 7 ou version ultérieure

la plupart des tâches que vous avez effectuées à l’aide de l’Lecteur Windows Media 6,4 ActiveX modèle objet de contrôle nécessitent une nouvelle approche. dans de nombreux cas, les noms des propriétés, des méthodes et des événements ont changé dans le modèle objet Lecteur Windows Media 7 ou version ultérieure. Par exemple, pour spécifier le chemin d’accès du fichier dans le modèle d’objet version 6,4, vous devez définir la propriété **Player6. FileName** :


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



lorsque vous utilisez le modèle objet Lecteur Windows Media 7 ou version ultérieure, vous devez définir la propriété **Player. URL** :


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



Ou bien, à l’aide du modèle d’objet 10, vous pouvez obtenir un objet **multimédia** à partir de la bibliothèque, puis définir la propriété **Player. currentMedia** :


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



la plupart des fonctionnalités du modèle objet Lecteur Windows Media 7 ou version ultérieure sont accessibles par le biais de la hiérarchie d’objets. Comme illustré dans l’exemple précédent, vous pouvez obtenir un objet de **sélection** à l’aide de la méthode **GetAll** de l’objet **mediaCollection** , accessible par le biais de l’objet **lecteur** racine. Vous pouvez ensuite obtenir un objet **multimédia** particulier à partir de l’objet **playlist** à l’aide de la méthode **Item** de l’objet **playlist** . Cinq méthodes supplémentaires sont accessibles via l’objet **mediaCollection** qui retournent un objet **playlist** . chaque méthode vous permet de récupérer l’objet en fonction de critères spécifiques, tels que le genre ou l’album.

la structure hiérarchique de la Lecteur Windows Media 7 ou version ultérieure ActiveX modèle objet de contrôle fournit une approche plus logique pour organiser les propriétés, les méthodes et les événements disponibles pour votre utilisation. Toutes les fonctionnalités pour les contrôles de lecteur sont contenues dans l’objet de **contrôle** , toutes les fonctionnalités de la connexion réseau du lecteur sont contenues dans l’objet **réseau** , et ainsi de suite. Par exemple, pour démarrer la lecture de contenu à l’aide du modèle d’objet version 6,4, utilisez la méthode **Player6. Play** :


```C++
WMP64.Play();

```



lorsque vous utilisez le modèle objet Lecteur Windows Media 7 ou version ultérieure, vous devez accéder à la méthode **Play** à l’aide de l’objet **controls** :


```C++
WMP9.controls.play();

```



La profondeur du modèle objet, toutefois, peut entraîner des instructions de script très longues :


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



Les instructions telles que le précédent peuvent être rendues plus simples et plus lisibles en utilisant des objets nommés individuels. L’exemple suivant remplace l’instruction de code précédente par une syntaxe utilisant des variables d’objet distinctes :


```C++
// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Get a playlist from the media collection that contains
// one media item named "MySong".
var temp = WMP9.mediaCollection.getByName("MySong");

// Get the individual media item from the temp playlist.
var song = temp.item(0);

// Append the media item to the current playlist.
pl.appendItem(song);

```



Ce style de codage nécessite plus de lignes de script, mais il est beaucoup plus facile à suivre, en particulier avec les commentaires ajoutés. Il existe un autre avantage : l’objet **currentPlaylist** est facile à réutiliser car il est stocké dans la variable pl.

la plupart des propriétés, méthodes et événements dans le modèle objet Lecteur Windows Media 7 ou ultérieur définissent ou récupèrent des valeurs différentes, ou retournent des valeurs d’un type ou d’un nombre différent, par rapport aux fonctionnalités correspondantes dans le modèle objet version 6,4. par exemple, lorsque **Player6. openState** récupère 2, cette valeur correspond au Visual Basic constante **nsLoadingNSC**, ce qui signifie que le lecteur charge un fichier de station avec l’extension de nom de fichier. nsc. toutefois, lorsque la propriété de l’objet Lecteur Windows Media 7 ou version ultérieure **Player. openState** récupère 2, cette valeur correspond à l’état PlaylistLocating, ce qui signifie que Lecteur Windows Media tente de localiser une sélection. en outre, la propriété **Player6. openState** peut récupérer sept valeurs différentes, tandis que la propriété Lecteur Windows Media 7 ou ultérieure **Player. openState** peut récupérer 22 valeurs différentes. veillez à vous reporter à la référence du modèle objet pour la section script du kit de développement logiciel (SDK) Lecteur Windows Media lors de la révision du code pour utiliser une version de modèle objet différente.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Guide de migration du modèle objet**](object-model-migration-guide.md)
</dt> </dl>

 

 




