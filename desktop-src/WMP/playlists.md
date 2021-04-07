---
title: Sélections
description: Sélections
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Lecteur Windows Media, sélections
- Modèle objet du lecteur Windows Media, sélections
- modèle objet, sélections
- Contrôle ActiveX du lecteur Windows Media, sélections
- Contrôle ActiveX, sélections
- Contrôle ActiveX mobile du lecteur Windows Media, sélections
- Windows Media Player Mobile, sélections
- sélections, migration
- Sélections de métafichiers Windows Media, migration
- sélections de métafichiers, migration
- Guide de migration, sélections
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124c07a6bd3aec0bebd235678e9fa8a5f069ec73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028943"
---
# <a name="playlists"></a><span data-ttu-id="cff01-114">Sélections</span><span class="sxs-lookup"><span data-stu-id="cff01-114">Playlists</span></span>

<span data-ttu-id="cff01-115">Le modèle objet de contrôle ActiveX du lecteur Windows Media 6,4 comprend quatre méthodes et une propriété pour l’utilisation des sélections de métafichiers Windows Media :</span><span class="sxs-lookup"><span data-stu-id="cff01-115">The Windows Media Player 6.4 ActiveX control object model includes four methods and one property for working with Windows Media metafile playlists:</span></span>

-   <span data-ttu-id="cff01-116">*Player6*. **GetCurrentEntry**</span><span class="sxs-lookup"><span data-stu-id="cff01-116">*Player6*.**GetCurrentEntry**</span></span>
-   <span data-ttu-id="cff01-117">*Player6*. **SetCurrentEntry**</span><span class="sxs-lookup"><span data-stu-id="cff01-117">*Player6*.**SetCurrentEntry**</span></span>
-   <span data-ttu-id="cff01-118">*Player6*. **GetMediaParameter**</span><span class="sxs-lookup"><span data-stu-id="cff01-118">*Player6*.**GetMediaParameter**</span></span>
-   <span data-ttu-id="cff01-119">*Player6*. **GetMediaParameterName**</span><span class="sxs-lookup"><span data-stu-id="cff01-119">*Player6*.**GetMediaParameterName**</span></span>
-   <span data-ttu-id="cff01-120">*Player6*. **EntryCount**.</span><span class="sxs-lookup"><span data-stu-id="cff01-120">*Player6*.**EntryCount**.</span></span>

<span data-ttu-id="cff01-121">Ensemble, ils offrent des fonctionnalités limitées pour naviguer dans un métafichier de sélection avec une extension de nom de fichier. asx et récupérer des informations sur les entrées contenues dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="cff01-121">Together, these provide limited functionality for navigating a playlist metafile with an .asx file name extension and retrieving information about the entries contained in the playlist.</span></span>

<span data-ttu-id="cff01-122">Le lecteur Windows Media 7 a introduit la « bibliothèque multimédia ».</span><span class="sxs-lookup"><span data-stu-id="cff01-122">Windows Media Player 7 introduced "Media Library."</span></span> <span data-ttu-id="cff01-123">La bibliothèque permet aux utilisateurs d’organiser leur contenu multimédia numérique, ainsi que de créer des sélections personnalisées qui peuvent être gérées à partir de l’interface utilisateur graphique du lecteur.</span><span class="sxs-lookup"><span data-stu-id="cff01-123">The library allows users to organize their digital media content, as well as to create custom playlists that can be managed from the Player graphical user interface.</span></span> <span data-ttu-id="cff01-124">Le modèle objet de contrôle ActiveX Windows Media Player 7 ou version ultérieure prend en charge l’utilisation des sélections de bibliothèque, ainsi que les sélections contenues dans les fichiers Windows Media avec une extension de nom de fichier. asx.</span><span class="sxs-lookup"><span data-stu-id="cff01-124">The Windows Media Player 7 or later ActiveX control object model provides support for working with library playlists, as well as playlists contained in Windows Media metafiles with an .asx file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="cff01-125">Pour des raisons de sécurité, l’utilisateur doit accorder des droits d’accès à la bibliothèque pour que votre programme puisse manipuler son contenu.</span><span class="sxs-lookup"><span data-stu-id="cff01-125">For security reasons, the user must grant access rights to the library before your program can manipulate its content.</span></span> <span data-ttu-id="cff01-126">Les droits d’accès ne peuvent être demandés et accordés que par le biais du modèle objet Windows Media Player 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cff01-126">Access rights can only be requested and granted through the Windows Media Player 9 Series or later object model.</span></span> <span data-ttu-id="cff01-127">Pour plus d’informations sur les droits d’accès, consultez accès à la [bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cff01-127">For details about access rights, see [Library Access](library-access.md).</span></span>

 

<span data-ttu-id="cff01-128">Le modèle objet Windows Media Player 7 ou version ultérieure comprend trois objets pour la gestion des sélections.</span><span class="sxs-lookup"><span data-stu-id="cff01-128">The Windows Media Player 7 or later object model includes three objects for handling playlists.</span></span> <span data-ttu-id="cff01-129">L’objet **PlaylistCollection** fournit les fonctionnalités d’organisation des sélections. Il représente l’ensemble de la collection de sélections dans la bibliothèque de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cff01-129">The **PlaylistCollection** object provides functionality for organizing playlists; it represents the entire collection of playlists in the user's library.</span></span> <span data-ttu-id="cff01-130">L’objet **PlaylistArray** permet de récupérer une sélection spécifique à partir de l’objet **PlaylistCollection** à l’aide d’un numéro d’index. deux des méthodes de l’objet **PlaylistCollection** récupèrent un objet **PlaylistArray** .</span><span class="sxs-lookup"><span data-stu-id="cff01-130">The **PlaylistArray** object provides a way to retrieve a specific playlist from the **PlaylistCollection** object by using an index number; two of the **PlaylistCollection** object methods retrieve a **PlaylistArray** object.</span></span> <span data-ttu-id="cff01-131">L’objet **playlist** fournit les propriétés et les méthodes nécessaires pour manipuler les éléments multimédias contenus dans une seule playlist.</span><span class="sxs-lookup"><span data-stu-id="cff01-131">The **Playlist** object provides the properties and methods necessary to manipulate media items contained in a single playlist.</span></span>

<span data-ttu-id="cff01-132">Par exemple, étant donné que chaque sélection de la bibliothèque a un nom unique, vous pouvez récupérer une sélection à partir de la bibliothèque à l’aide de *PlaylistCollection*. méthode **GetByName** :</span><span class="sxs-lookup"><span data-stu-id="cff01-132">As an example, since each playlist in the library has a unique name, you can retrieve a playlist from the library using the *PlaylistCollection*.**getByName** method:</span></span>


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



<span data-ttu-id="cff01-133">Le plus souvent, vous souhaitez utiliser la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="cff01-133">You will most frequently want to work with the current playlist.</span></span> <span data-ttu-id="cff01-134">Bien qu’il soit possible d’utiliser plusieurs objets de sélection, un seul peut être récupéré par le *joueur*. propriété **currentPlaylist** à un moment donné : celle que le lecteur Windows Media traite à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="cff01-134">While it is possible to use several playlist objects, only one can be retrieved by the *Player*.**currentPlaylist** property at any given time: the one that Windows Media Player is processing at that moment.</span></span>

<span data-ttu-id="cff01-135">Lorsque Windows Media Player 7 ou version ultérieure lit un métafichier Windows Media avec une extension de nom de fichier. asx, il crée tout d’abord un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="cff01-135">When Windows Media Player 7 or later plays a Windows Media metafile with an .asx file name extension, it first creates a **Playlist** object.</span></span> <span data-ttu-id="cff01-136">Ensuite, il remplit l’objet avec les informations de la sélection. asx, puis fait de cet objet **playlist** la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="cff01-136">Next, it fills the object with the information from the .asx playlist, and then makes that **Playlist** object the current playlist.</span></span> <span data-ttu-id="cff01-137">Cela signifie que vous pouvez utiliser les propriétés et les méthodes associées à l’objet **playlist** pour manipuler les sélections. asx exactement comme vous le feriez pour gérer des sélections dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="cff01-137">This means that you can use the properties and methods associated with the **Playlist** object to manipulate .asx playlists exactly as you would handle playlists in the library.</span></span> <span data-ttu-id="cff01-138">Par exemple, pour récupérer le nombre d’entrées dans une sélection. asx à l’aide du modèle d’objet version 6,4, vous utilisez *Player6*. Propriété **EntryCount** :</span><span class="sxs-lookup"><span data-stu-id="cff01-138">For instance, to retrieve the number of entries in an .asx playlist using the version 6.4 object model, you use the *Player6*.**EntryCount** property:</span></span>


```C++
var entrycount = WMP64.EntryCount;

```



<span data-ttu-id="cff01-139">Lorsque vous utilisez le modèle objet Windows Media Player 7 ou version ultérieure, vous utilisez la *sélection*. propriété **Count** :</span><span class="sxs-lookup"><span data-stu-id="cff01-139">When using the Windows Media Player 7 or later object model, you use the *Playlist*.**count** property:</span></span>


```C++
var entrycount = WMP9.currentPlaylist.count;

```



<span data-ttu-id="cff01-140">Lorsque vous utilisez le contrôle version 6,4, vous pouvez utiliser *Player6*. Méthode **GetCurrentEntry** pour récupérer l’index de l’entrée actuelle dans une sélection. ASX :</span><span class="sxs-lookup"><span data-stu-id="cff01-140">When using the version 6.4 control, you can use the *Player6*.**GetCurrentEntry** method to retrieve the index of the current entry in an .asx playlist:</span></span>


```C++
var entrynum = WMP64.GetCurrentEntry();

```



<span data-ttu-id="cff01-141">Vous pouvez obtenir le même résultat en utilisant le modèle objet Windows Media Player 7 ou version ultérieure dans le script.</span><span class="sxs-lookup"><span data-stu-id="cff01-141">You can achieve the same result by using the Windows Media Player 7 or later object model in script.</span></span> <span data-ttu-id="cff01-142">L’exemple JScript suivant compare l’objet multimédia actuel à chaque élément de la sélection.</span><span class="sxs-lookup"><span data-stu-id="cff01-142">The following JScript example compares the current media object to each item in the playlist.</span></span> <span data-ttu-id="cff01-143">Lorsque le *média* est. **isIdentical** retourne la valeur true, une boîte de message affiche l’index de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="cff01-143">When *Media*.**isIdentical** returns true, a message box displays the index of the current media item.</span></span>


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



<span data-ttu-id="cff01-144">Pour spécifier l’index de l’entrée actuelle dans une sélection. asx, utilisez *Player6*. **SetCurrentEntry**.</span><span class="sxs-lookup"><span data-stu-id="cff01-144">To specify the index of the current entry in an .asx playlist, you use *Player6*.**SetCurrentEntry**.</span></span> <span data-ttu-id="cff01-145">Les index d’entrée de playlist dans la version 6,4 commencent par 1. par conséquent, pour faire de la seconde entrée dans une sélection de métafichiers celle qui est active, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="cff01-145">Playlist entry indexes in version 6.4 start with 1, so to make the second entry in a metafile playlist the current one, use the following syntax:</span></span>


```C++
WMP6.SetCurrentEntry(2);

```



<span data-ttu-id="cff01-146">Les index d’entrée de playlist sont de base zéro dans le lecteur Windows Media 7 ou version ultérieure ; pour faire de la deuxième entrée dans une sélection de métafichiers celle qui est active, lorsque vous utilisez le modèle objet Windows Media Player 7 ou version ultérieure, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="cff01-146">Playlist entry indexes are zero-based in Windows Media Player 7 or later; to make the second entry in a metafile playlist the current one, when using the Windows Media Player 7 or later object model, use the following syntax:</span></span>


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



<span data-ttu-id="cff01-147">L’exemple JScript suivant illustre une fonction qui accepte un numéro d’index en tant que paramètre, puis définit l’entrée de la sélection qui correspond à l’index de l’élément multimédia actuel :</span><span class="sxs-lookup"><span data-stu-id="cff01-147">The following JScript example demonstrates a function that accepts an index number as a parameter, and then makes the playlist entry that corresponds to the index the current media item:</span></span>


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



<span data-ttu-id="cff01-148">Les fichiers Windows Media peuvent contenir des éléments de paramètres personnalisés que vous spécifiez à l’aide de la **<PARAM>** balise.</span><span class="sxs-lookup"><span data-stu-id="cff01-148">Windows Media metafiles can contain custom parameter elements, which you specify by using the **<PARAM>** tag.</span></span> <span data-ttu-id="cff01-149">Lorsque vous utilisez le modèle d’objet version 6,4, vous pouvez récupérer le nom d’un paramètre particulier avec *Player6*. Méthode **GetMediaParameterName** .</span><span class="sxs-lookup"><span data-stu-id="cff01-149">When using the version 6.4 object model, you can retrieve the name of a particular parameter with the *Player6*.**GetMediaParameterName** method.</span></span> <span data-ttu-id="cff01-150">L’exemple JScript suivant récupère le nom du premier paramètre de la première entrée d’une sélection. ASX :</span><span class="sxs-lookup"><span data-stu-id="cff01-150">The following JScript example retrieves the name of the first parameter in the first entry of an .asx playlist:</span></span>


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



<span data-ttu-id="cff01-151">De même, vous pouvez récupérer la valeur associée au paramètre à l’aide de *Player6*. **GetMediaParameter**:</span><span class="sxs-lookup"><span data-stu-id="cff01-151">Similarly, you can retrieve the value associated with the parameter using *Player6*.**GetMediaParameter**:</span></span>


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



<span data-ttu-id="cff01-152">L’exemple JScript suivant utilise le modèle objet Windows Media Player 7 ou version ultérieure pour récupérer le nom et la valeur du paramètre de la première entrée dans une sélection. ASX :</span><span class="sxs-lookup"><span data-stu-id="cff01-152">The following JScript example uses the Windows Media Player 7 or later object model to retrieve the parameter name and value from the first entry in an .asx playlist:</span></span>


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



<span data-ttu-id="cff01-153">Vous pouvez utiliser *PlaylistCollection*. méthode **importPlaylist** pour ajouter une sélection. asx à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="cff01-153">You can use the *PlaylistCollection*.**importPlaylist** method to add an .asx playlist to the library.</span></span> <span data-ttu-id="cff01-154">Une fois importée, la sélection de métafichiers devient une sélection de bibliothèque, ce qui vous permet de la manipuler à l’aide de toutes les propriétés et méthodes à votre disposition.</span><span class="sxs-lookup"><span data-stu-id="cff01-154">Once imported, the metafile playlist becomes a library playlist, so you can manipulate it using all the properties and methods at your disposal.</span></span> <span data-ttu-id="cff01-155">L’utilisateur doit accorder des droits d’accès complets à la bibliothèque pour que votre application puisse utiliser la méthode **importPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="cff01-155">The user must grant full access rights to the library for your application to be able to use the **importPlaylist** method.</span></span>

<span data-ttu-id="cff01-156">Vous pouvez utiliser *PlaylistCollection*. **GetByName** pour tester si une sélection existe.</span><span class="sxs-lookup"><span data-stu-id="cff01-156">You can use *PlaylistCollection*.**getByName** to test whether a playlist exists.</span></span> <span data-ttu-id="cff01-157">Cette méthode retourne toujours un objet **PlaylistArray** valide.</span><span class="sxs-lookup"><span data-stu-id="cff01-157">This method always returns a valid **PlaylistArray** object.</span></span> <span data-ttu-id="cff01-158">Si le tableau de sélection récupéré contient exactement une sélection, alors il existe une sélection portant ce nom dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="cff01-158">If the playlist array retrieved contains exactly one playlist, then there exists a playlist with that name in the library.</span></span> <span data-ttu-id="cff01-159">Dans le cas contraire, le tableau de sélection ne contiendra aucun objet de sélection. Cela signifie qu’il n’y a aucune playlist dans la bibliothèque dont le nom est passé comme argument à la méthode **GetByName** .</span><span class="sxs-lookup"><span data-stu-id="cff01-159">Otherwise, the playlist array will contain no playlist object; this means there is no playlist in the library with the name passed as an argument to the **getByName** method.</span></span> <span data-ttu-id="cff01-160">L’exemple JScript suivant illustre ceci :</span><span class="sxs-lookup"><span data-stu-id="cff01-160">The following JScript example demonstrates this:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cff01-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cff01-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cff01-162">**Gestion des sélections**</span><span class="sxs-lookup"><span data-stu-id="cff01-162">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="cff01-163">**Guide de migration du modèle objet**</span><span class="sxs-lookup"><span data-stu-id="cff01-163">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="cff01-164">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="cff01-164">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




