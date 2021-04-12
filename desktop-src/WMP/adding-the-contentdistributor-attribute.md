---
title: Ajout de l’attribut ContentDistributor
description: Ajout de l’attribut ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player Online stores, ajout de l’attribut ContentDistributor
- magasins en ligne, ajouter un attribut ContentDistributor
- types 1 magasins en ligne, ajout de l’attribut ContentDistributor
- type 2 magasins en ligne, ajout de l’attribut ContentDistributor
- Windows Media Player Online stores, attribut ContentDistributor
- magasins en ligne, attribut ContentDistributor
- types 1 magasins en ligne, attribut ContentDistributor
- types 2 magasins en ligne, attribut ContentDistributor
- ajout de l’attribut ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310090"
---
# <a name="adding-the-contentdistributor-attribute"></a><span data-ttu-id="92b08-113">Ajout de l’attribut ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="92b08-113">Adding the ContentDistributor Attribute</span></span>

<span data-ttu-id="92b08-114">Quand l’utilisateur tente de lire le contenu de la boutique en ligne ou de copier le contenu sur un CD ou un périphérique, le lecteur Windows Media appelle certaines méthodes dans votre objet COM.</span><span class="sxs-lookup"><span data-stu-id="92b08-114">When the user attempts to play online store content or to copy the content to a CD or device, Windows Media Player calls certain methods in your COM object.</span></span> <span data-ttu-id="92b08-115">Pour ce faire, le joueur a besoin d’un moyen de différencier votre contenu de celui d’autres fournisseurs de magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="92b08-115">To do this, the Player needs a way to differentiate your content from that of other online store providers.</span></span> <span data-ttu-id="92b08-116">En ajoutant le nom de votre clé de magasin en ligne comme valeur de **ContentDistributor** (qui est un alias de l’attribut **WM/ContentDistributor**) du kit de développement logiciel (SDK) du format Windows Media à votre contenu Windows Media, vous vous assurez que le lecteur peut identifier le contenu associé à votre service.</span><span class="sxs-lookup"><span data-stu-id="92b08-116">By adding your online store key name as the value for the **ContentDistributor** (which is an alias for the Windows Media Format SDK attribute named **WM/ContentDistributor**) attribute to your Windows Media-based content, you ensure that the Player can identify the content associated with your service.</span></span>

<span data-ttu-id="92b08-117">L’ajout d’une valeur pour **ContentDistributor** garantit également que le lecteur Windows Media va créer un nœud dans la bibliothèque pour le contenu que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="92b08-117">Adding a value for **ContentDistributor** also ensures that Windows Media Player will create a node in the library for content you provide.</span></span> <span data-ttu-id="92b08-118">Consultez [intégration](library-integration.md)de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="92b08-118">See [Library Integration](library-integration.md).</span></span>

<span data-ttu-id="92b08-119">Vous pouvez spécifier cette valeur de deux manières :</span><span class="sxs-lookup"><span data-stu-id="92b08-119">You can specify this value two ways:</span></span>

-   <span data-ttu-id="92b08-120">Utilisez le modèle objet du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="92b08-120">Use the Windows Media Player object model.</span></span> <span data-ttu-id="92b08-121">Dans ce cas, le lecteur Windows Media ajoute la valeur que vous spécifiez à la base de données de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="92b08-121">When you do this, Windows Media Player adds the value you specify to the library database.</span></span> <span data-ttu-id="92b08-122">Finalement, le lecteur écrira également la valeur de l’attribut dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="92b08-122">Eventually, the Player will also write the attribute value to the digital media file.</span></span>
-   <span data-ttu-id="92b08-123">Utilisez le kit de développement logiciel (SDK) de format Windows Media pour ajouter par programmation l’attribut **WM/ContentDistributor** .</span><span class="sxs-lookup"><span data-stu-id="92b08-123">Use the Windows Media Format SDK to programmatically add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="92b08-124">Dans ce cas, le lecteur Windows Media lit la valeur de l’attribut et l’ajoute à la base de données lorsque le fichier multimédia numérique est ajouté à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="92b08-124">When you do this, Windows Media Player reads the attribute value and adds it to the database when the digital media file is added to the library.</span></span>

<span data-ttu-id="92b08-125">Lorsque vous créez votre objet COM de magasin en ligne, la valeur d’attribut de fichier que vous définissez pour **ContentDistributor** et la valeur assignée à la constante KszContentDistributorID dans YourProject. h doivent correspondre exactement.</span><span class="sxs-lookup"><span data-stu-id="92b08-125">When creating your online store COM object, the file attribute value you set for **ContentDistributor** and the value assigned to the constant kszContentDistributorID in YourProject.h must match exactly.</span></span> <span data-ttu-id="92b08-126">Rappelez-vous que vous avez spécifié cette valeur constante pour votre objet COM lorsque vous avez créé le projet à l’aide de l’Assistant projet.</span><span class="sxs-lookup"><span data-stu-id="92b08-126">Recall that you specified this constant value for your COM object when you created the project by using the project wizard.</span></span> <span data-ttu-id="92b08-127">Vous pouvez modifier cette valeur manuellement.</span><span class="sxs-lookup"><span data-stu-id="92b08-127">You can change this value manually.</span></span> <span data-ttu-id="92b08-128">Veillez simplement à utiliser une chaîne qui identifie de façon unique votre service.</span><span class="sxs-lookup"><span data-stu-id="92b08-128">Just be sure to use a string that uniquely identifies your service.</span></span>

## <a name="using-the-windows-media-player-object-model"></a><span data-ttu-id="92b08-129">Utilisation du modèle objet du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="92b08-129">Using the Windows Media Player Object Model</span></span>

<span data-ttu-id="92b08-130">Pour spécifier une valeur pour **ContentDistributor** à l’aide du modèle objet du lecteur Windows Media, utilisez la méthode [Media. setItemInfo](media-setiteminfo.md) .</span><span class="sxs-lookup"><span data-stu-id="92b08-130">To specify a value for **ContentDistributor** using the Windows Media Player object model, use the [Media.setItemInfo](media-setiteminfo.md) method.</span></span> <span data-ttu-id="92b08-131">L’exemple de code suivant spécifie la valeur « Proseware » pour **ContentDistributor** pour l’élément multimédia en cours de diffusion :</span><span class="sxs-lookup"><span data-stu-id="92b08-131">The following example code specifies the value "Proseware" for **ContentDistributor** for the currently playing media item:</span></span>


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a><span data-ttu-id="92b08-132">Utilisation du kit de développement logiciel (SDK) Windows Media format</span><span class="sxs-lookup"><span data-stu-id="92b08-132">Using the Windows Media Format SDK</span></span>

<span data-ttu-id="92b08-133">Le kit de développement logiciel (SDK) du lecteur Windows Media comprend un exemple de fichier C++, nommé SetContentDistributor. cpp, qui montre comment utiliser le kit de développement logiciel (SDK) Windows Media Format 9 pour ajouter l’attribut **WM/ContentDistributor** .</span><span class="sxs-lookup"><span data-stu-id="92b08-133">The Windows Media Player SDK includes a sample C++ file, named SetContentDistributor.cpp, which demonstrates how to use the Windows Media Format 9 Series SDK to add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="92b08-134">Vous pouvez trouver cet exemple de fichier dans le dossier nommé Metadata où vous avez installé le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="92b08-134">You can locate this sample file in the folder named Metadata where you installed the SDK.</span></span> <span data-ttu-id="92b08-135">Pour utiliser ce code, vous devez effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="92b08-135">To use this code you must follow these steps:</span></span>

1.  <span data-ttu-id="92b08-136">Installez le kit de développement logiciel (SDK) Windows Media Format 9 Series et configurez le runtime comme décrit dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="92b08-136">Install the Windows Media Format 9 Series SDK and configure the runtime as described in the documentation.</span></span>
2.  <span data-ttu-id="92b08-137">Créez un projet C++ vide dans Visual Studio et ajoutez l’exemple de fichier nommé SetContentDistributor. cpp au projet.</span><span class="sxs-lookup"><span data-stu-id="92b08-137">Create a new empty C++ project in Visual Studio and add the sample file named SetContentDistributor.cpp to the project.</span></span>
3.  <span data-ttu-id="92b08-138">Ajoutez le chemin d’accès aux dossiers lib du kit de développement logiciel (SDK) Windows Media Format 9 Series dans votre liste de chemins d’accès aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="92b08-138">Add the path to the Windows Media Format 9 Series SDK Lib folders to your list of file paths.</span></span> <span data-ttu-id="92b08-139">Dans le menu **Outils** , choisissez **Options**.</span><span class="sxs-lookup"><span data-stu-id="92b08-139">From the **Tools** menu, choose **Options**.</span></span>
4.  <span data-ttu-id="92b08-140">Dans la boîte de dialogue **options** , cliquez sur **projets**, puis sur **Répertoires VC + +**.</span><span class="sxs-lookup"><span data-stu-id="92b08-140">In the **Options** dialog box, click **Projects**, and then click **VC++ Directories**.</span></span>
5.  <span data-ttu-id="92b08-141">Dans la zone de liste déroulante **afficher les répertoires pour** , cliquez sur **fichiers de bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="92b08-141">In the **Show Directories for** drop-down list box, click **Library files**.</span></span>
6.  <span data-ttu-id="92b08-142">Utilisez les boutons pour ajouter les chemins d’accès aux zones de liste.</span><span class="sxs-lookup"><span data-stu-id="92b08-142">Use the buttons to add the paths to the list boxes.</span></span>
7.  <span data-ttu-id="92b08-143">Ouvrez la boîte de dialogue pages de propriétés de votre projet.</span><span class="sxs-lookup"><span data-stu-id="92b08-143">Open the property pages dialog box for your project.</span></span> <span data-ttu-id="92b08-144">Choisissez **Propriétés de configuration**, puis **éditeur de liens**, puis **entrée**.</span><span class="sxs-lookup"><span data-stu-id="92b08-144">Choose **Configuration Properties**, then **Linker**, and then **Input**.</span></span> <span data-ttu-id="92b08-145">Tapez « wmvcore. lib » dans la zone de texte **dépendances supplémentaires** .</span><span class="sxs-lookup"><span data-stu-id="92b08-145">Type "wmvcore.lib" in the **Additional Dependencies** text box.</span></span>

<span data-ttu-id="92b08-146">L’exemple de code crée un programme de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="92b08-146">The sample code creates a command-line program.</span></span> <span data-ttu-id="92b08-147">Les arguments que vous fournissez lors de l’exécution du programme spécifient le chemin d’accès au fichier multimédia numérique à modifier et une chaîne pour la valeur de l’attribut **ContentDistributor** .</span><span class="sxs-lookup"><span data-stu-id="92b08-147">The arguments you provide when running the program specify the path to the digital media file to modify and a string for the **ContentDistributor** attribute value.</span></span> <span data-ttu-id="92b08-148">Le code utilise **IWMHeaderInfo :: setAttribute** pour ajouter l’attribut au fichier que vous avez spécifié.</span><span class="sxs-lookup"><span data-stu-id="92b08-148">The code uses **IWMHeaderInfo::SetAttribute** to add the attribute to the file you specified.</span></span> <span data-ttu-id="92b08-149">Vous pouvez utiliser cet exemple tel quel ou l’utiliser comme point de départ pour votre propre programme.</span><span class="sxs-lookup"><span data-stu-id="92b08-149">You can use this sample as is or use it as a starting point for your own program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92b08-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92b08-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92b08-151">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="92b08-151">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




