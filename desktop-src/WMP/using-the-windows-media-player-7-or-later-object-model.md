---
title: Utilisation du modèle objet Windows Media Player 7 ou version ultérieure
description: Utilisation du modèle objet Windows Media Player 7 ou version ultérieure
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Lecteur Windows Media, modèle objet
- Windows Media Player Object Model, version 7 ou ultérieure
- modèle objet, version 7 ou ultérieure
- Contrôle ActiveX du lecteur Windows Media, version 7 ou ultérieure
- Contrôle ActiveX, version 7 ou ultérieure
- Windows Media Player Mobile contrôle ActiveX, version 7 ou ultérieure
- Windows Media Player Mobile, modèle objet
- Guide de migration, version 7 ou ultérieure
- versions du lecteur Windows Media, modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310394"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a><span data-ttu-id="38512-112">Utilisation du modèle objet Windows Media Player 7 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="38512-112">Using the Windows Media Player 7 or Later Object Model</span></span>

<span data-ttu-id="38512-113">La plupart des tâches que vous avez pu effectuer à l’aide du modèle objet de contrôle ActiveX du lecteur Windows Media 6,4 nécessitent une nouvelle approche.</span><span class="sxs-lookup"><span data-stu-id="38512-113">Most of the tasks you may have been performing using the Windows Media Player 6.4 ActiveX control object model will require a new approach.</span></span> <span data-ttu-id="38512-114">Dans de nombreux cas, les noms des propriétés, des méthodes et des événements ont changé dans le modèle objet Windows Media Player 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="38512-114">In many cases, the names of the properties, methods, and events have changed in the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="38512-115">Par exemple, pour spécifier le chemin d’accès du fichier dans le modèle d’objet version 6,4, vous devez définir la propriété **Player6. FileName** :</span><span class="sxs-lookup"><span data-stu-id="38512-115">For instance, to specify the file path in the version 6.4 object model, you set the **Player6.FileName** property:</span></span>


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="38512-116">Lorsque vous utilisez le modèle objet Windows Media Player 7 ou version ultérieure, vous devez définir la propriété **Player. URL** :</span><span class="sxs-lookup"><span data-stu-id="38512-116">When using the Windows Media Player 7 or later object model, you must set the **Player.URL** property:</span></span>


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="38512-117">Ou bien, à l’aide du modèle d’objet 10, vous pouvez obtenir un objet **multimédia** à partir de la bibliothèque, puis définir la propriété **Player. currentMedia** :</span><span class="sxs-lookup"><span data-stu-id="38512-117">Alternatively, using the 10 object model, you can obtain a **Media** object from the library, and then set the **Player.currentMedia** property:</span></span>


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



<span data-ttu-id="38512-118">La plupart des fonctionnalités du modèle objet Windows Media Player 7 ou version ultérieure sont accessibles par le biais de la hiérarchie d’objets.</span><span class="sxs-lookup"><span data-stu-id="38512-118">Much of the functionality in the Windows Media Player 7 or later object model is accessed through the object hierarchy.</span></span> <span data-ttu-id="38512-119">Comme illustré dans l’exemple précédent, vous pouvez obtenir un objet de **sélection** à l’aide de la méthode **GetAll** de l’objet **mediaCollection** , accessible par le biais de l’objet **lecteur** racine.</span><span class="sxs-lookup"><span data-stu-id="38512-119">As the previous example showed, you can obtain a **Playlist** object by using the **getAll** method of the **mediaCollection** object, which is accessed through the root **Player** object.</span></span> <span data-ttu-id="38512-120">Vous pouvez ensuite obtenir un objet **multimédia** particulier à partir de l’objet **playlist** à l’aide de la méthode **Item** de l’objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="38512-120">You can then obtain a particular **Media** object from the **Playlist** object by using the **item** method of the **Playlist** object.</span></span> <span data-ttu-id="38512-121">Cinq méthodes supplémentaires sont accessibles via l’objet **mediaCollection** qui retournent un objet **playlist** . chaque méthode vous permet de récupérer l’objet en fonction de critères spécifiques, tels que le genre ou l’album.</span><span class="sxs-lookup"><span data-stu-id="38512-121">There are five additional methods accessible through the **mediaCollection** object that return a **Playlist** object; each method allows you to retrieve the object based on specific criteria, like genre or album.</span></span>

<span data-ttu-id="38512-122">La structure hiérarchique du modèle objet de contrôle ActiveX Windows Media Player 7 ou version ultérieure offre une approche plus logique pour organiser les propriétés, les méthodes et les événements disponibles pour votre utilisation.</span><span class="sxs-lookup"><span data-stu-id="38512-122">The hierarchical structure of the Windows Media Player 7 or later ActiveX control object model provides a more logical approach to organizing the properties, methods, and events available for your use.</span></span> <span data-ttu-id="38512-123">Toutes les fonctionnalités pour les contrôles de lecteur sont contenues dans l’objet de **contrôle** , toutes les fonctionnalités de la connexion réseau du lecteur sont contenues dans l’objet **réseau** , et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="38512-123">All the functionality for the Player controls is contained in the **Controls** object, all the functionality for the Player network connection is contained in the **Network** object, and so forth.</span></span> <span data-ttu-id="38512-124">Par exemple, pour démarrer la lecture de contenu à l’aide du modèle d’objet version 6,4, utilisez la méthode **Player6. Play** :</span><span class="sxs-lookup"><span data-stu-id="38512-124">For example, to start content playing using the version 6.4 object model, you use the **Player6.Play** method:</span></span>


```C++
WMP64.Play();

```



<span data-ttu-id="38512-125">Lorsque vous utilisez le modèle objet Windows Media Player 7 ou version ultérieure, vous devez accéder à la méthode **Play** à l’aide de l’objet **Controls** :</span><span class="sxs-lookup"><span data-stu-id="38512-125">When using the Windows Media Player 7 or later object model, you must access the **Play** method by using the **Controls** object:</span></span>


```C++
WMP9.controls.play();

```



<span data-ttu-id="38512-126">La profondeur du modèle objet, toutefois, peut entraîner des instructions de script très longues :</span><span class="sxs-lookup"><span data-stu-id="38512-126">The depth of the object model, however, can lead to very long script statements:</span></span>


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



<span data-ttu-id="38512-127">Les instructions telles que le précédent peuvent être rendues plus simples et plus lisibles en utilisant des objets nommés individuels.</span><span class="sxs-lookup"><span data-stu-id="38512-127">Statements like the preceding one can be made much simpler and more readable by working with individual named objects.</span></span> <span data-ttu-id="38512-128">L’exemple suivant remplace l’instruction de code précédente par une syntaxe utilisant des variables d’objet distinctes :</span><span class="sxs-lookup"><span data-stu-id="38512-128">The following example replaces the preceding code statement with syntax using separate object variables:</span></span>


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



<span data-ttu-id="38512-129">Ce style de codage nécessite plus de lignes de script, mais il est beaucoup plus facile à suivre, en particulier avec les commentaires ajoutés.</span><span class="sxs-lookup"><span data-stu-id="38512-129">This coding style requires more lines of script, but is much easier to follow, especially with the added comments.</span></span> <span data-ttu-id="38512-130">Il existe un autre avantage : l’objet **currentPlaylist** est facile à réutiliser car il est stocké dans la variable pl.</span><span class="sxs-lookup"><span data-stu-id="38512-130">There is another advantage: the **currentPlaylist** object is easy to reuse because it is stored in the variable pl.</span></span>

<span data-ttu-id="38512-131">La plupart des propriétés, méthodes et événements dans le modèle objet Windows Media Player 7 ou version ultérieure définissent ou récupèrent des valeurs différentes, ou retournent des valeurs d’un type ou d’un nombre différent, par rapport aux fonctionnalités correspondantes dans le modèle objet version 6,4.</span><span class="sxs-lookup"><span data-stu-id="38512-131">Many of the properties, methods, and events in the Windows Media Player 7 or later object model set or retrieve different values, or return values of a different type or number, compared to corresponding functionality in the version 6.4 object model.</span></span> <span data-ttu-id="38512-132">Par exemple, lorsque **Player6. openState** récupère 2, cette valeur correspond au Visual Basic constante **nsLoadingNSC**, ce qui signifie que le lecteur charge un fichier de station avec l’extension de nom de fichier. NSC.</span><span class="sxs-lookup"><span data-stu-id="38512-132">For instance, when **Player6.openState** retrieves 2, that value corresponds to the Visual Basic constant **nsLoadingNSC**, meaning the Player is loading a station file with a .nsc file name extension.</span></span> <span data-ttu-id="38512-133">Toutefois, lorsque la propriété de l’objet lecteur Windows Media 7 ou version ultérieure **Player. openState** récupère 2, cette valeur correspond à l’État PlaylistLocating, ce qui signifie que le lecteur Windows Media tente de localiser une sélection.</span><span class="sxs-lookup"><span data-stu-id="38512-133">But when the Windows Media Player 7 or later object model property **Player.openState** retrieves 2, that value corresponds to the state PlaylistLocating, meaning Windows Media Player is attempting to locate a playlist.</span></span> <span data-ttu-id="38512-134">En outre, la propriété **Player6. openState** peut récupérer sept valeurs différentes, tandis que la propriété Player **. OpenState** de Windows Media Player 7 peut récupérer 22 valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="38512-134">Additionally, the **Player6.openState** property can retrieve seven different values, while the Windows Media Player 7 or later **Player.openState** property can retrieve 22 different values.</span></span> <span data-ttu-id="38512-135">Veillez à vous reporter à la référence du modèle objet pour la section script du kit de développement logiciel (SDK) du lecteur Windows Media pour réviser le code et utiliser une version de modèle objet différente.</span><span class="sxs-lookup"><span data-stu-id="38512-135">Be sure to refer to the Object Model Reference for Scripting section of the Windows Media Player SDK when revising code to use a different object model version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38512-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38512-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38512-137">**À propos du modèle objet Player**</span><span class="sxs-lookup"><span data-stu-id="38512-137">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="38512-138">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="38512-138">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="38512-139">**Guide de migration du modèle objet**</span><span class="sxs-lookup"><span data-stu-id="38512-139">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




