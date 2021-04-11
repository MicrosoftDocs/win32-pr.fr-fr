---
title: Gestion des éléments multimédias
description: Gestion des éléments multimédias
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Lecteur Windows Media, bibliothèque
- Modèle objet du lecteur Windows Media, bibliothèque
- modèle objet, bibliothèque
- Windows Media Player Mobile, bibliothèque pour le modèle objet
- Contrôle ActiveX du lecteur Windows Media, bibliothèque pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, bibliothèque pour le modèle objet
- Contrôle ActiveX, bibliothèque pour le modèle objet
- Bibliothèque du lecteur Windows Media, gestion des éléments multimédias
- bibliothèque, gestion des éléments multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100809"
---
# <a name="managing-media-items"></a><span data-ttu-id="c0914-112">Gestion des éléments multimédias</span><span class="sxs-lookup"><span data-stu-id="c0914-112">Managing Media Items</span></span>

<span data-ttu-id="c0914-113">Un objet **multimédia** représente un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="c0914-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="c0914-114">Il possède des propriétés et des méthodes que vous pouvez utiliser pour récupérer des informations et les afficher à l’utilisateur, ou pour effectuer des actions différentes en fonction de la valeur que vous récupérez.</span><span class="sxs-lookup"><span data-stu-id="c0914-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="c0914-115">La majeure partie de votre travail avec les objets **multimédias** implique des métadonnées sur le contenu de l’élément multimédia, appelé attributs.</span><span class="sxs-lookup"><span data-stu-id="c0914-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="c0914-116">La rubrique [attributs d’élément multimédia](media-item-attributes.md) décrit comment lire et modifier des valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="c0914-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="c0914-117">En plus de cette rubrique, consultez les [instructions relatives à l’utilisation des métadonnées Windows Media](/previous-versions/ms867702(v=msdn.10)) sur le site Web Microsoft pour plus d’informations sur les attributs et leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="c0914-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="c0914-118">L’objet **Media** possède des propriétés et des méthodes qui récupèrent des attributs directement, tels que le nom ou la durée de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c0914-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="c0914-119">Pour les éléments vidéo, vous pouvez récupérer la hauteur et la largeur de l’image, et vous pouvez récupérer les informations de marqueur en fonction du nom ou de l’index d’un marqueur.</span><span class="sxs-lookup"><span data-stu-id="c0914-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="c0914-120">Vous pouvez également déterminer si un élément multimédia particulier est inclus dans une sélection particulière.</span><span class="sxs-lookup"><span data-stu-id="c0914-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="c0914-121">Récupération d’un objet multimédia</span><span class="sxs-lookup"><span data-stu-id="c0914-121">Retrieving a Media Object</span></span>

<span data-ttu-id="c0914-122">Vous pouvez accéder rapidement à l’élément multimédia actuel à l’aide du *lecteur*. propriété **currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="c0914-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="c0914-123">Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="c0914-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="c0914-124">L’exemple C# suivant récupère un objet **multimédia** représentant l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="c0914-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="c0914-125">Vous pouvez créer un élément multimédia à partir d’un fichier multimédia numérique à l’aide du *lecteur*. méthode **newMedia** .</span><span class="sxs-lookup"><span data-stu-id="c0914-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="c0914-126">Vous transmettez à la méthode le chemin d’accès de l’URL d’un fichier multimédia numérique et retourne une référence au nouvel objet **Media** .</span><span class="sxs-lookup"><span data-stu-id="c0914-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="c0914-127">La méthode n’ajoute pas directement le nouvel objet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c0914-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="c0914-128">Toutefois, vous pouvez transmettre l’objet à la *sélection*. méthode **appendItem** ou *playlist*. méthode **InsertItem** .</span><span class="sxs-lookup"><span data-stu-id="c0914-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="c0914-129">L’exemple C# suivant crée un objet **multimédia** basé sur l’un des exemples de médias numériques installés avec le kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c0914-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="c0914-130">Vous devez inclure deux barres obliques inverses ( \) ou utiliser le caractère @ en C#) dans une chaîne pour représenter une barre oblique inverse réelle.</span><span class="sxs-lookup"><span data-stu-id="c0914-130">You must include two backslash (\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="c0914-131">Cela est dû au fait que C# utilise une barre oblique inverse unique pour définir une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="c0914-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="c0914-132">Vous pouvez créer un élément multimédia à partir d’un fichier multimédia numérique et l’ajouter à la bibliothèque en une seule étape à l’aide de *MediaCollection*. **Ajouter** une méthode.</span><span class="sxs-lookup"><span data-stu-id="c0914-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="c0914-133">Comme le *lecteur*. méthode **newMedia** , la méthode **Add** prend le chemin d’accès à un fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="c0914-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="c0914-134">L’exemple C# suivant crée un objet **multimédia** en fonction de l’un des exemples de fichiers du kit de développement logiciel (SDK) et ajoute cet objet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c0914-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="c0914-135">Vous pouvez récupérer un objet **multimédia** représentant un élément multimédia dans une sélection à l’aide de la *sélection*. méthode **Item** .</span><span class="sxs-lookup"><span data-stu-id="c0914-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="c0914-136">L’exemple C# suivant récupère le sixième élément multimédia de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="c0914-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="c0914-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c0914-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0914-138">**Controls. currentItem**</span><span class="sxs-lookup"><span data-stu-id="c0914-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="c0914-139">**Gestion des sélections**</span><span class="sxs-lookup"><span data-stu-id="c0914-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="c0914-140">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="c0914-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="c0914-141">**MediaCollection. Add**</span><span class="sxs-lookup"><span data-stu-id="c0914-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="c0914-142">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="c0914-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="c0914-143">**Player. newMedia**</span><span class="sxs-lookup"><span data-stu-id="c0914-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="c0914-144">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="c0914-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="c0914-145">**Utilisation de la bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="c0914-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




