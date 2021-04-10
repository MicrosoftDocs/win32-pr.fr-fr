---
title: Attributs de sélection
description: Attributs de sélection
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Lecteur Windows Media, sélections
- Modèle objet du lecteur Windows Media, sélections
- modèle objet, sélections
- Windows Media Player Mobile, sélections
- Contrôle ActiveX du lecteur Windows Media, sélections
- Contrôle ActiveX mobile du lecteur Windows Media, sélections
- Contrôle ActiveX, sélections
- sélections, attributs
- sélections de métafichiers, attributs
- Sélections de métafichiers Windows Media, attributs
- attributs, sélections
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939834"
---
# <a name="playlist-attributes"></a><span data-ttu-id="2aaec-114">Attributs de sélection</span><span class="sxs-lookup"><span data-stu-id="2aaec-114">Playlist Attributes</span></span>

<span data-ttu-id="2aaec-115">Les sélections comportent des informations de métadonnées appelées attributs, tout comme les éléments multimédias ont des attributs.</span><span class="sxs-lookup"><span data-stu-id="2aaec-115">Playlists have metadata information called attributes, just as media items have attributes.</span></span> <span data-ttu-id="2aaec-116">Vous pouvez récupérer les noms et les valeurs des attributs de sélection et les afficher dans votre interface utilisateur, ou votre code peut prendre des mesures en fonction de la valeur d’un attribut.</span><span class="sxs-lookup"><span data-stu-id="2aaec-116">You can retrieve the names and values of playlist attributes and display them in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="2aaec-117">Les sélections sont définies dans des fichiers organisés dans un format XML, et des éléments particuliers du fichier définissent des attributs de sélection.</span><span class="sxs-lookup"><span data-stu-id="2aaec-117">Playlists are defined in files organized in an XML format, and particular elements in the file define playlist attributes.</span></span> <span data-ttu-id="2aaec-118">Certains éléments d’attribut sont connus ; l’auteur du métafichier peut également définir des attributs arbitraires.</span><span class="sxs-lookup"><span data-stu-id="2aaec-118">Some attribute elements are well-known; the author of the metafile can also define arbitrary attributes.</span></span> <span data-ttu-id="2aaec-119">Pour plus d’informations sur les éléments d’attribut dans les fichiers de sélection, consultez [récupération des métadonnées](retrieving-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="2aaec-119">For more information about attribute elements in playlist files, see [Retrieving Metadata](retrieving-metadata.md).</span></span>

<span data-ttu-id="2aaec-120">La bibliothèque peut fournir des attributs de sélection supplémentaires, tels que **SourceURL** ou **UserLastPlayedTime**.</span><span class="sxs-lookup"><span data-stu-id="2aaec-120">The library may provide additional playlist attributes, such as **SourceURL** or **UserLastPlayedTime**.</span></span> <span data-ttu-id="2aaec-121">Pour plus d’informations sur les attributs de sélection de bibliothèque, consultez la [référence](attribute-reference.md)des attributs du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2aaec-121">For more information about the library playlist attributes, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="2aaec-122">*Sélection*. la propriété **attributeCount** récupère le nombre d’attributs associés à la sélection.</span><span class="sxs-lookup"><span data-stu-id="2aaec-122">The *Playlist*.**attributeCount** property retrieves the number of attributes associated with the playlist.</span></span> <span data-ttu-id="2aaec-123">*Sélection*. la propriété **AttributeName** récupère le nom d’un attribut en fonction de son index et de la *sélection*. la méthode **getItemInfo** récupère la valeur d’un attribut en fonction de son nom.</span><span class="sxs-lookup"><span data-stu-id="2aaec-123">The *Playlist*.**attributeName** property retrieves the name of an attribute based on its index, and the *Playlist*.**getItemInfo** method retrieves the value of an attribute based on its name.</span></span>

<span data-ttu-id="2aaec-124">Vous pouvez modifier la valeur d’un attribut de la sélection actuelle avec la *sélection*. méthode **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="2aaec-124">You can modify the value of an attribute of the current playlist with the *Playlist*.**setItemInfo** method.</span></span>

<span data-ttu-id="2aaec-125">Une utilisation spéciale de la méthode **setItemInfo** consiste à trier les éléments de la sélection, à l’aide de l’attribut **SortAttribute** .</span><span class="sxs-lookup"><span data-stu-id="2aaec-125">A special use of the **setItemInfo** method is to sort the items in the playlist, using the **SortAttribute** attribute.</span></span> <span data-ttu-id="2aaec-126">L’exemple C# suivant trie une sélection selon les valeurs de l’attribut **UserLastPlayedTime** .</span><span class="sxs-lookup"><span data-stu-id="2aaec-126">The following C# example sorts a playlist by the values of the **UserLastPlayedTime** attribute.</span></span> <span data-ttu-id="2aaec-127">La *sélection* de variable est une référence à un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="2aaec-127">The variable *Playlist* is a reference to a **Playlist** object.</span></span>


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



<span data-ttu-id="2aaec-128">Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="2aaec-128">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="2aaec-129">L’exemple de code C# suivant montre comment récupérer des attributs de sélection.</span><span class="sxs-lookup"><span data-stu-id="2aaec-129">The following C# example code demonstrates retrieving playlist attributes.</span></span> <span data-ttu-id="2aaec-130">La première fonction, ShowPlaylists, remplit un contrôle ListBox avec les noms des sélections disponibles.</span><span class="sxs-lookup"><span data-stu-id="2aaec-130">The first function, ShowPlaylists, populates a ListBox control with the names of the available playlists.</span></span> <span data-ttu-id="2aaec-131">La deuxième partie est le gestionnaire d’événements de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="2aaec-131">The second part is the list box event handler.</span></span> <span data-ttu-id="2aaec-132">Quand l’utilisateur clique sur un nom de playlist, ce code récupère les attributs de cette playlist et affiche ces attributs dans une deuxième zone de liste.</span><span class="sxs-lookup"><span data-stu-id="2aaec-132">When the user clicks a playlist name, this code retrieves the attributes for that playlist and displays those attributes in a second list box.</span></span>


```C++
// Member variables
IWMPPlaylistCollection PlaylistColl;
IWMPPlaylistArray PlaylistArray;

private void ShowPlaylists()
{
    // Retrieve the playlist collection
    PlaylistColl = Player.playlistCollection;
    // Store the collection in a playlist array
    PlaylistArray = PlaylistColl.getAll();

    // Retrieve the count of elements
    iCount = PlaylistArray.count;

    // Update the list box with the playlist names.
    lstPlaylist.BeginUpdate();
    for (int i=0; i<iCount; i++)
    {
        lstPlaylist.Items.Add(PlaylistArray.Item(i).name);
    }
    lstPlaylist.EndUpdate();

    // Set the selected index to zero
    lstPlaylist.SelectedIndex = 0;
}

```



<span data-ttu-id="2aaec-133">L’événement SelectedIndexChanged du contrôle ListBox est appelé chaque fois que l’utilisateur sélectionne un nom de sélection.</span><span class="sxs-lookup"><span data-stu-id="2aaec-133">The SelectedIndexChanged event for the ListBox control is called each time the user selects a playlist name.</span></span> <span data-ttu-id="2aaec-134">Le gestionnaire d’événements suivant remplit une deuxième zone de liste avec les noms d’attributs et les valeurs correspondant à la sélection de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2aaec-134">The following event handler fills a second list box with the attribute names and values corresponding to the user's selection.</span></span>


```C++
private void lstPlaylist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    IWMPPlaylist Playlist = PlaylistArray.Item(lstPlaylist.SelectedIndex);
    string strAttr="";
    string strItemNames="";
    int iAttribCount=0;

    iAttribCount = Playlist.attribCount;
    for (j=0; j<iAttribCount; j++)
    {
        strAttr=Playlist.get_attributeName(j) + " -- ";
        strAttr+=Playlist.getItemInfo(Playlist.get_attributeName(j));
        lstOutput.Items.Add(strAttr);
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="2aaec-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2aaec-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aaec-136">**Gestion des sélections**</span><span class="sxs-lookup"><span data-stu-id="2aaec-136">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="2aaec-137">**Attributs d’élément multimédia**</span><span class="sxs-lookup"><span data-stu-id="2aaec-137">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="2aaec-138">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="2aaec-138">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




