---
title: Sélections
description: Sélections
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Lecteur Windows Media, sélections
- Lecteur Windows Media modèle objet, playlists
- modèle objet, sélections
- contrôle de ActiveX Lecteur Windows Media, sélections
- contrôle de ActiveX, sélections
- Lecteur Windows Media contrôle de ActiveX Mobile, sélections
- Lecteur Windows Media Mobile, sélections
- sélections, migration
- Windows Sélections de métafichiers multimédia, migration
- sélections de métafichiers, migration
- Guide de migration, sélections
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccdd98789de6c8d4faa06882376967298646febabd790067710dc4f460ba65b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334472"
---
# <a name="playlists"></a>Sélections

le Lecteur Windows Media 6,4 ActiveX modèle objet de contrôle comprend quatre méthodes et une propriété pour l’utilisation de Windows les sélections de métafichiers Media :

-   *Player6*. **GetCurrentEntry**
-   *Player6*. **SetCurrentEntry**
-   *Player6*. **GetMediaParameter**
-   *Player6*. **GetMediaParameterName**
-   *Player6*. **EntryCount**.

Ensemble, ils offrent des fonctionnalités limitées pour naviguer dans un métafichier de sélection avec une extension de nom de fichier. asx et récupérer des informations sur les entrées contenues dans la sélection.

Lecteur Windows Media 7 a introduit « la bibliothèque multimédia ». La bibliothèque permet aux utilisateurs d’organiser leur contenu multimédia numérique, ainsi que de créer des sélections personnalisées qui peuvent être gérées à partir de l’interface utilisateur graphique du lecteur. le Lecteur Windows Media 7 ou version ultérieure ActiveX modèle objet de contrôle assure la prise en charge de l’utilisation des listes de sélection de bibliothèque, ainsi que des sélections contenues dans Windows des fichiers multimédias avec une extension de nom de fichier. asx.

> [!Note]  
> Pour des raisons de sécurité, l’utilisateur doit accorder des droits d’accès à la bibliothèque pour que votre programme puisse manipuler son contenu. les droits d’accès peuvent uniquement être demandés et accordés par le biais du modèle objet série Lecteur Windows Media 9 ou version ultérieure. Pour plus d’informations sur les droits d’accès, consultez accès à la [bibliothèque](library-access.md).

 

le modèle objet Lecteur Windows Media 7 ou version ultérieure comprend trois objets pour la gestion des sélections. L’objet **PlaylistCollection** fournit les fonctionnalités d’organisation des sélections. Il représente l’ensemble de la collection de sélections dans la bibliothèque de l’utilisateur. L’objet **PlaylistArray** permet de récupérer une sélection spécifique à partir de l’objet **PlaylistCollection** à l’aide d’un numéro d’index. deux des méthodes de l’objet **PlaylistCollection** récupèrent un objet **PlaylistArray** . L’objet **playlist** fournit les propriétés et les méthodes nécessaires pour manipuler les éléments multimédias contenus dans une seule playlist.

Par exemple, étant donné que chaque sélection de la bibliothèque a un nom unique, vous pouvez récupérer une sélection à partir de la bibliothèque à l’aide de *PlaylistCollection*. méthode **GetByName** :


```C++
// Retrieve a PlaylistArray object that contains 
// exactly one Playlist object.
var plarray = WMP9.playlistCollection.getByName("MyPlaylist");

// Get the Playlist object from the PlaylistArray object.
// The Playlist object has index number zero.
var pl = plarray.item(0);

// Make the retrieved playlist the current playlist.
WMP9.currentPlaylist = pl;

```



Le plus souvent, vous souhaitez utiliser la sélection actuelle. Bien qu’il soit possible d’utiliser plusieurs objets de sélection, un seul peut être récupéré par le *joueur*. propriété **currentPlaylist** à un moment donné : celle que Lecteur Windows Media est en cours de traitement à ce moment-là.

lorsque Lecteur Windows Media 7 ou version ultérieure lit un métafichier Windows Media avec une extension de nom de fichier. asx, il crée tout d’abord un objet **Playlist** . Ensuite, il remplit l’objet avec les informations de la sélection. asx, puis fait de cet objet **playlist** la sélection actuelle. Cela signifie que vous pouvez utiliser les propriétés et les méthodes associées à l’objet **playlist** pour manipuler les sélections. asx exactement comme vous le feriez pour gérer des sélections dans la bibliothèque. Par exemple, pour récupérer le nombre d’entrées dans une sélection. asx à l’aide du modèle d’objet version 6,4, vous utilisez *Player6*. Propriété **EntryCount** :


```C++
var entrycount = WMP64.EntryCount;

```



lorsque vous utilisez le modèle objet Lecteur Windows Media 7 ou version ultérieure, vous utilisez la *sélection*. propriété **Count** :


```C++
var entrycount = WMP9.currentPlaylist.count;

```



Lorsque vous utilisez le contrôle version 6,4, vous pouvez utiliser *Player6*. Méthode **GetCurrentEntry** pour récupérer l’index de l’entrée actuelle dans une sélection. ASX :


```C++
var entrynum = WMP64.GetCurrentEntry();

```



vous pouvez obtenir le même résultat en utilisant le modèle objet Lecteur Windows Media 7 ou version ultérieure dans le script. l’exemple de JScript suivant compare l’objet multimédia actuel à chaque élément de la sélection. Lorsque le *média* est. **isIdentical** retourne la valeur true, une boîte de message affiche l’index de l’élément multimédia actuel.


```C++
function matchit(){
// Store the current playlist object in a variable.
var pl = WMP9.currentPlaylist;

// Loop through the playlist one entry at a time.
  for (var i = 0; i < pl.count; i++){

   // Test whether the current media item matches 
   // the item in the playlist at the current loop index.
   if (WMP9.currentmedia.isIdentical(pl.item(i))){

       // They match, display the index.
       var message = "Current media at index: " + i;
       alert(message);

       // Exit the function, don't continue looping!
       return;
      }
  }
}

```



Pour spécifier l’index de l’entrée actuelle dans une sélection. asx, utilisez *Player6*. **SetCurrentEntry**. Les index d’entrée de playlist dans la version 6,4 commencent par 1. par conséquent, pour faire de la seconde entrée dans une sélection de métafichiers celle qui est active, utilisez la syntaxe suivante :


```C++
WMP6.SetCurrentEntry(2);

```



les index d’entrée de Playlist sont de base zéro dans Lecteur Windows Media 7 ou version ultérieure ; pour faire de la deuxième entrée dans une sélection de métafichier la seconde en cours, lorsque vous utilisez le modèle objet Lecteur Windows Media 7 ou version ultérieure, utilisez la syntaxe suivante :


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



l’exemple de JScript suivant illustre une fonction qui accepte un numéro d’index en tant que paramètre, puis définit l’entrée de la sélection qui correspond à l’index de l’élément multimédia actuel :


```C++
function setindex(idx){
// Store the current playlist in a variable.
var pl = WMP9.currentPlaylist;

// Get the first playlist entry.
var firstmedia = pl.item(0);

// Start the Player to allow navigation within the playlist.
WMP9.controls.playItem(firstmedia);

// Test whether idx is within a valid range.
   if (idx < pl.count && idx >= 0){

     // Set the currentItem to the desired playlist item.
     WMP9.controls.currentItem = pl.item(idx);

     // Display the name of the media item.
     alert(WMP9.currentMedia.name);
     return true;
 }

// The index is out of range, stop the Player, alert the user.
WMP9.controls.stop();
alert("Index out of range");
return false;
}

```



Windows Les fichiers multimédias peuvent contenir des éléments de paramètres personnalisés que vous spécifiez à l’aide de la **<PARAM>** balise. Lorsque vous utilisez le modèle d’objet version 6,4, vous pouvez récupérer le nom d’un paramètre particulier avec *Player6*. Méthode **GetMediaParameterName** . l’exemple de JScript suivant récupère le nom du premier paramètre de la première entrée d’une sélection. asx :


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



De même, vous pouvez récupérer la valeur associée au paramètre à l’aide de *Player6*. **GetMediaParameter**:


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



l’exemple de JScript suivant utilise le modèle objet Lecteur Windows Media 7 ou version ultérieure pour récupérer le nom et la valeur du paramètre de la première entrée dans une sélection. asx :


```C++
function getattribute(){
// Store the first playlist entry as a Media object.
var firstmedia = WMP9.currentplaylist.item(0);

// Get the name of the first parameter in the object named firstmedia.
var attname = firstmedia.getAttributeName(0);

// Get the value of the first parameter in the object named firstmedia.
var attval = firstmedia.getItemInfo(attname);

// Display the information.
alert(attname + ": " + attval);
}

```



Vous pouvez utiliser *PlaylistCollection*. méthode **importPlaylist** pour ajouter une sélection. asx à la bibliothèque. Une fois importée, la sélection de métafichiers devient une sélection de bibliothèque, ce qui vous permet de la manipuler à l’aide de toutes les propriétés et méthodes à votre disposition. L’utilisateur doit accorder des droits d’accès complets à la bibliothèque pour que votre application puisse utiliser la méthode **importPlaylist** .

Vous pouvez utiliser *PlaylistCollection*. **GetByName** pour tester si une sélection existe. Cette méthode retourne toujours un objet **PlaylistArray** valide. Si le tableau de sélection récupéré contient exactement une sélection, alors il existe une sélection portant ce nom dans la bibliothèque. Dans le cas contraire, le tableau de sélection ne contiendra aucun objet de sélection. Cela signifie qu’il n’y a aucune playlist dans la bibliothèque dont le nom est passé comme argument à la méthode **GetByName** . l’exemple de JScript suivant illustre ce qui suit :


```C++
// Specify an .asx playlist file.
WMP9.URL = "https://www.microsoft.com/someplaylist.asx";

// Open the playlist and start playing the content.
WMP9.controls.play();

// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Attempt to retrieve from the library 
// a playlist having the same name as the current playlist.
var plarray = WMP9.playlistCollection.getByName(pl.name);

// Test whether the PlaylistArray object, plarray, contains
// a Playlist object.
if (!plarray.count)
   
   // If plarray contains no playlist, then import 
   // the current one.
   WMP9.playlistCollection.importPlaylist(pl);
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des sélections**](managing-playlists.md)
</dt> <dt>

[**Guide de migration du modèle objet**](object-model-migration-guide.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> </dl>

 

 




