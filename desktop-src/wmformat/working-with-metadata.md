---
title: Utilisation des métadonnées
description: Utilisation des métadonnées
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows Media Format SDK, vue d’ensemble des métadonnées
- ASF (Advanced Systems Format), vue d’ensemble des métadonnées
- ASF (format des systèmes avancés), vue d’ensemble des métadonnées
- métadonnées, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104381701"
---
# <a name="working-with-metadata"></a><span data-ttu-id="cb110-107">Utilisation des métadonnées</span><span class="sxs-lookup"><span data-stu-id="cb110-107">Working with Metadata</span></span>

<span data-ttu-id="cb110-108">La prise en charge des métadonnées est fournie par l’objet Writer, le lecteur et les objets lecteur synchrones, ainsi que l’objet éditeur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cb110-108">Metadata support is provided by the writer object, the reader and synchronous reader objects, and the metadata editor object.</span></span> <span data-ttu-id="cb110-109">Pour obtenir des informations générales sur les métadonnées, consultez [métadonnées](metadata.md).</span><span class="sxs-lookup"><span data-stu-id="cb110-109">For general information about metadata, see [Metadata](metadata.md).</span></span> <span data-ttu-id="cb110-110">Pour plus d’informations sur les fonctionnalités de prise en charge des métadonnées dans le kit de développement logiciel Windows Media format, consultez [fonctionnalités de métadonnées](metadata-features.md).</span><span class="sxs-lookup"><span data-stu-id="cb110-110">For information about the features supporting metadata in the Windows Media Format SDK, see [Metadata Features](metadata-features.md).</span></span>

<span data-ttu-id="cb110-111">L’interface pour la modification des métadonnées est [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), que vous pouvez obtenir en appelant la méthode **QueryInterface** de n’importe quelle interface dans l’un des objets mentionnés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="cb110-111">The interface for metadata editing is [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), which you can obtain by calling the **QueryInterface** method of any interface in one of the objects listed above.</span></span> <span data-ttu-id="cb110-112">**IWMHeaderInfo3** hérite des méthodes de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) et [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span><span class="sxs-lookup"><span data-stu-id="cb110-112">**IWMHeaderInfo3** inherits the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span></span> <span data-ttu-id="cb110-113">Les méthodes de **IWMHeaderInfo3** qui traitent des attributs de métadonnées représentent une approche différente de l’accès aux métadonnées que celle utilisée par les méthodes de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="cb110-113">The methods of **IWMHeaderInfo3** that deal with metadata attributes represent a different approach to accessing metadata than that used by the methods of **IWMHeaderInfo**.</span></span> <span data-ttu-id="cb110-114">Vous devez toujours utiliser les méthodes plus récentes.</span><span class="sxs-lookup"><span data-stu-id="cb110-114">You should always use the newer methods.</span></span>

<span data-ttu-id="cb110-115">Les métadonnées d’un fichier ASF sont identifiées par un index et un numéro de flux.</span><span class="sxs-lookup"><span data-stu-id="cb110-115">Metadata in an ASF file is identified by an index and a stream number.</span></span> <span data-ttu-id="cb110-116">Un numéro de flux 0 est assigné aux attributs au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="cb110-116">File-level attributes are assigned a stream number of 0.</span></span> <span data-ttu-id="cb110-117">Dans les versions précédentes du kit de développement logiciel (SDK) Windows Media format, les attributs pouvaient être identifiés par leur nom.</span><span class="sxs-lookup"><span data-stu-id="cb110-117">In previous versions of the Windows Media Format SDK, attributes could be identified by name.</span></span> <span data-ttu-id="cb110-118">Toutefois, étant donné que vous pouvez désormais dupliquer des noms d’attribut dans un flux, ce n’est plus possible.</span><span class="sxs-lookup"><span data-stu-id="cb110-118">However, because you can now duplicate attribute names within a stream, this is no longer possible.</span></span> <span data-ttu-id="cb110-119">Au lieu de cela, vous pouvez récupérer tous les index correspondant à un nom.</span><span class="sxs-lookup"><span data-stu-id="cb110-119">Instead, you can retrieve all the indexes matching a name.</span></span> <span data-ttu-id="cb110-120">Pour plus d’informations, consultez [récupération des attributs de métadonnées](retrieving-metadata-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="cb110-120">For more information, see [Retrieving Metadata Attributes](retrieving-metadata-attributes.md).</span></span>

<span data-ttu-id="cb110-121">Pour faciliter la recherche d’attributs rapidement, vous pouvez utiliser un numéro de flux spécial, 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="cb110-121">To aid in finding attributes quickly, you can use a special stream number, 0xFFFF.</span></span> <span data-ttu-id="cb110-122">Utilisez ce numéro de flux pour identifier l’ensemble du fichier, plutôt qu’un flux spécifique ou les attributs au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="cb110-122">Use this stream number to identify the file as a whole, rather than a specific stream or the file-level attributes.</span></span> <span data-ttu-id="cb110-123">Les objets du kit de développement logiciel (SDK) de format Windows Media gèrent des index distincts pour chaque flux et pour les attributs de niveau fichier.</span><span class="sxs-lookup"><span data-stu-id="cb110-123">The objects of the Windows Media Format SDK maintain separate indexes for each stream and for the file-level attributes.</span></span> <span data-ttu-id="cb110-124">Lorsque vous utilisez Stream 0xFFFF, les index sont différents de ceux que vous utilisez lors de la spécification d’un flux spécifique.</span><span class="sxs-lookup"><span data-stu-id="cb110-124">When using stream 0xFFFF, the indexes are different from those you use when specifying a specific stream.</span></span> <span data-ttu-id="cb110-125">Par exemple, l’attribut qui est l’index 0 pour le flux 0 ne sera pas le même que l’attribut index 0 pour Stream 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="cb110-125">For example, the attribute that is index 0 for stream 0 will not be the same as the attribute that is index 0 for stream 0xFFFF.</span></span>

<span data-ttu-id="cb110-126">Les sections suivantes décrivent l’utilisation des métadonnées plus en détail.</span><span class="sxs-lookup"><span data-stu-id="cb110-126">The following sections describe the use of metadata in greater detail.</span></span>



| <span data-ttu-id="cb110-127">Section</span><span class="sxs-lookup"><span data-stu-id="cb110-127">Section</span></span>                                                                    | <span data-ttu-id="cb110-128">Description</span><span class="sxs-lookup"><span data-stu-id="cb110-128">Description</span></span>                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="cb110-129">Récupération des attributs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="cb110-129">Retrieving Metadata Attributes</span></span>](retrieving-metadata-attributes.md)       | <span data-ttu-id="cb110-130">Décrit comment lire les attributs de métadonnées d’un en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="cb110-130">Describes how to read metadata attributes from a file header.</span></span>                     |
| [<span data-ttu-id="cb110-131">Définition des attributs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="cb110-131">Setting Metadata Attributes</span></span>](setting-metadata-attributes.md)             | <span data-ttu-id="cb110-132">Décrit comment ajouter de nouveaux attributs de métadonnées à un en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="cb110-132">Describes how to add new metadata attributes to a file header.</span></span>                    |
| [<span data-ttu-id="cb110-133">Modification des attributs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="cb110-133">Editing Metadata Attributes</span></span>](editing-metadata-attributes.md)             | <span data-ttu-id="cb110-134">Décrit comment modifier des attributs de métadonnées existants.</span><span class="sxs-lookup"><span data-stu-id="cb110-134">Describes how to edit existing metadata attributes.</span></span>                               |
| [<span data-ttu-id="cb110-135">Supprimer des attributs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="cb110-135">Removing Metadata Attributes</span></span>](removing-metadata-attributes.md)           | <span data-ttu-id="cb110-136">Décrit comment supprimer des attributs de métadonnées existants.</span><span class="sxs-lookup"><span data-stu-id="cb110-136">Describes how to remove existing metadata attributes.</span></span>                             |
| [<span data-ttu-id="cb110-137">Utilisation d’attributs de métadonnées complexes</span><span class="sxs-lookup"><span data-stu-id="cb110-137">Using Complex Metadata Attributes</span></span>](using-complex-metadata-attributes.md) | <span data-ttu-id="cb110-138">Décrit comment utiliser des attributs dont les valeurs sont représentées par des structures.</span><span class="sxs-lookup"><span data-stu-id="cb110-138">Describes how to work with attributes whose values are represented by structures.</span></span> |



 

<span data-ttu-id="cb110-139">Plusieurs des exemples d’applications montrent comment récupérer et modifier des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cb110-139">Several of the sample applications show how to retrieve and edit metadata.</span></span> <span data-ttu-id="cb110-140">En particulier, consultez l’exemple MetadataEdit, qui se trouve à la fois dans les versions C++ et C#.</span><span class="sxs-lookup"><span data-stu-id="cb110-140">In particular, see the MetadataEdit sample, which comes in both C++ and C# versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb110-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb110-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb110-142">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="cb110-142">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="cb110-143">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="cb110-143">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="cb110-144">**Exemples d’applications**</span><span class="sxs-lookup"><span data-stu-id="cb110-144">**Sample Applications**</span></span>](sample-applications.md)
</dt> </dl>

 

 




