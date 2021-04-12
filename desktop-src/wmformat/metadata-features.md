---
title: Fonctionnalités de métadonnées
description: Les métadonnées sont utilisées dans les fichiers ASF pour décrire le contenu et les propriétés d’un fichier.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Media Format SDK, fonctionnalités de métadonnées
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités
- ASF (Advanced Systems Format), fonctionnalités de métadonnées
- ASF (format de systèmes avancés), fonctionnalités de métadonnées
- ASF (Advanced Systems Format), fonctionnalités
- ASF (format des systèmes avancés), fonctionnalités
- métadonnées, fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104381693"
---
# <a name="metadata-features"></a><span data-ttu-id="9f3d1-110">Fonctionnalités de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9f3d1-110">Metadata Features</span></span>

<span data-ttu-id="9f3d1-111">Les métadonnées sont utilisées dans les fichiers ASF pour décrire le contenu et les propriétés d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-111">Metadata is used in ASF files to describe file contents and properties.</span></span> <span data-ttu-id="9f3d1-112">Tous les fichiers ASF que vous créez doivent inclure les métadonnées appropriées.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-112">All ASF files you create should include appropriate metadata.</span></span> <span data-ttu-id="9f3d1-113">(Pour une vue d’ensemble, consultez [Metadata](metadata.md).) Le kit de développement logiciel (SDK) Windows Media format prend en charge la modification des métadonnées via l’objet Writer, l’objet éditeur de métadonnées et les objets lecteur et lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-113">(For an overview, see [Metadata](metadata.md).) The Windows Media Format SDK includes support for metadata editing through the writer object, the metadata editor object, and both the reader and synchronous reader objects.</span></span> <span data-ttu-id="9f3d1-114">La prise en charge native d’un large éventail d’attributs de métadonnées est incluse.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-114">Native support for a wide variety of metadata attributes is included.</span></span> <span data-ttu-id="9f3d1-115">Pour obtenir la liste des attributs prédéfinis, consultez [attributs](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="9f3d1-115">See [Attributes](attributes.md) for a list of the predefined attributes.</span></span>

<span data-ttu-id="9f3d1-116">La prise en charge des métadonnées fournie par les différents objets du kit de développement logiciel (SDK) du format Windows Media est flexible et puissante.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-116">The metadata support provided by the various objects of the Windows Media Format SDK is flexible and powerful.</span></span> <span data-ttu-id="9f3d1-117">Les principales fonctionnalités de métadonnées sont résumées dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="9f3d1-117">The main metadata features are summarized in the following list:</span></span>

-   <span data-ttu-id="9f3d1-118">Taille d’attribut flexible.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-118">Flexible attribute size.</span></span> <span data-ttu-id="9f3d1-119">La taille des attributs de métadonnées n’est pas limitée.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-119">Metadata attributes are not limited in size.</span></span>
-   <span data-ttu-id="9f3d1-120">Attributs au niveau du flux.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-120">Stream-level attributes.</span></span> <span data-ttu-id="9f3d1-121">Les métadonnées des fichiers ASF peuvent être assignées au fichier dans son ensemble ou à un flux de données particulier.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-121">Metadata in ASF files can be assigned to the file as a whole, or to a particular stream.</span></span>
-   <span data-ttu-id="9f3d1-122">Attributs dupliqués.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-122">Duplicated attributes.</span></span> <span data-ttu-id="9f3d1-123">Un attribut nommé peut être utilisé plusieurs fois dans le même fichier.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-123">A named attribute can be used multiple times in the same file.</span></span> <span data-ttu-id="9f3d1-124">Cette fonctionnalité est particulièrement utilisée lors de l’affectation d’attributs descriptifs de contenu.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-124">This feature is of particular use when assigning content descriptive attributes.</span></span> <span data-ttu-id="9f3d1-125">Par exemple, une chanson peut avoir plusieurs auteurs, chacun requérant un attribut **Author** distinct dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-125">For example, a song may have several authors, each requiring a separate **Author** attribute in the file.</span></span>
-   <span data-ttu-id="9f3d1-126">Plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-126">Multiple languages.</span></span> <span data-ttu-id="9f3d1-127">Chaque attribut est associé à une langue.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-127">Every attribute has a language associated with it.</span></span> <span data-ttu-id="9f3d1-128">Vous pouvez définir les langues prises en charge, puis en affecter une à chaque attribut que vous écrivez.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-128">You can set the supported languages and then assign one to each attribute you write.</span></span> <span data-ttu-id="9f3d1-129">Étant donné que vous pouvez dupliquer des attributs, vous pouvez fournir les attributs les plus importants dans plusieurs langues pour atteindre un public plus large.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-129">Because you can duplicate attributes, you can provide the most important attributes in several languages to reach a larger audience.</span></span> <span data-ttu-id="9f3d1-130">Si vous ne spécifiez pas de langue, la langue par défaut (obtenue à partir du système d’exploitation de l’ordinateur exécutant votre application) sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-130">If you do not specify a language, the default language (obtained from the operating system of the computer running your application) will be used.</span></span>
-   <span data-ttu-id="9f3d1-131">Attributs complexes.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-131">Complex attributes.</span></span> <span data-ttu-id="9f3d1-132">Certains des attributs prédéfinis prennent en charge les données structurées.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-132">Some of the predefined attributes support structured data.</span></span> <span data-ttu-id="9f3d1-133">Pour ces attributs, le type de données est Binary, mais la valeur est une structure définie dans ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="9f3d1-133">For these attributes, the data type is binary, but the value is a structure defined in this SDK.</span></span>

<span data-ttu-id="9f3d1-134">Les rubriques suivantes abordent les autres fonctionnalités de métadonnées prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-134">The following topics discuss the other supported metadata features.</span></span>



| <span data-ttu-id="9f3d1-135">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9f3d1-135">Topic</span></span>                                  | <span data-ttu-id="9f3d1-136">Description</span><span class="sxs-lookup"><span data-stu-id="9f3d1-136">Description</span></span>                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f3d1-137">Prise en charge d’ID3</span><span class="sxs-lookup"><span data-stu-id="9f3d1-137">ID3 Support</span></span>](id3.md)                 | <span data-ttu-id="9f3d1-138">Décrit la prise en charge des frames ID3 à l’aide des objets du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-138">Discusses the support for ID3 frames using the objects of the Windows Media Format SDK.</span></span> |
| [<span data-ttu-id="9f3d1-139">Métadonnées personnalisées</span><span class="sxs-lookup"><span data-stu-id="9f3d1-139">Custom Metadata</span></span>](custom-metadata.md) | <span data-ttu-id="9f3d1-140">Décrit les implications de l’utilisation de métadonnées personnalisées.</span><span class="sxs-lookup"><span data-stu-id="9f3d1-140">Discusses the implications of using custom metadata.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="9f3d1-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9f3d1-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f3d1-142">**Fonctionnalités**</span><span class="sxs-lookup"><span data-stu-id="9f3d1-142">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="9f3d1-143">**Interface IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="9f3d1-143">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="9f3d1-144">**Interface IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="9f3d1-144">**IWMHeaderInfo2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[<span data-ttu-id="9f3d1-145">**Interface IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="9f3d1-145">**IWMHeaderInfo3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[<span data-ttu-id="9f3d1-146">**Métadonnées**</span><span class="sxs-lookup"><span data-stu-id="9f3d1-146">**Metadata**</span></span>](metadata.md)
</dt> </dl>

 

 




