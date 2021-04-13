---
title: Métadonnées
description: Dans le cadre de ce kit de développement logiciel (SDK), les métadonnées sont des informations qui décrivent un fichier ASF ou le contenu du fichier.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows Media Format SDK, vue d’ensemble des métadonnées
- ASF (Advanced Systems Format), vue d’ensemble des métadonnées
- ASF (format des systèmes avancés), vue d’ensemble des métadonnées
- métadonnées, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311251"
---
# <a name="metadata"></a><span data-ttu-id="e6c6f-107">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="e6c6f-107">Metadata</span></span>

<span data-ttu-id="e6c6f-108">Dans le cadre de ce kit de développement logiciel (SDK), les métadonnées sont des informations qui décrivent un fichier ASF ou le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-108">Metadata, for the purposes of this SDK, is information that describes an ASF file or the contents of the file.</span></span> <span data-ttu-id="e6c6f-109">La section d’en-tête d’un fichier ASF contient toutes les métadonnées associées à ce fichier.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-109">The header section of an ASF file contains all of the metadata associated with that file.</span></span> <span data-ttu-id="e6c6f-110">Les éléments de métadonnées d’un fichier ASF sont appelés attributs.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-110">Individual items of metadata in an ASF file are called attributes.</span></span> <span data-ttu-id="e6c6f-111">Chaque attribut a un nom et une valeur.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-111">Each attribute has a name and a value.</span></span> <span data-ttu-id="e6c6f-112">Tout au long de cette documentation, les constantes globales sont utilisées pour identifier les attributs.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-112">Throughout this documentation, global constants are used to identify attributes.</span></span> <span data-ttu-id="e6c6f-113">Par exemple, le titre d’un fichier ASF est stocké dans l’attribut **g \_ wszWMTitle** .</span><span class="sxs-lookup"><span data-stu-id="e6c6f-113">For example, the title of an ASF file is stored in the **g\_wszWMTitle** attribute.</span></span>

<span data-ttu-id="e6c6f-114">Un certain nombre d’attributs sont définis dans le kit de développement logiciel (SDK) Windows Media format pour gérer les métadonnées les plus courantes.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-114">A number of attributes are defined in the Windows Media Format SDK to handle the most common metadata needs.</span></span> <span data-ttu-id="e6c6f-115">En outre, vous pouvez créer vos propres attributs.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-115">In addition, you can create your own attributes.</span></span> <span data-ttu-id="e6c6f-116">Toutefois, lorsque vous nommez des attributs personnalisés, vous devez être prudent, car d’autres développeurs d’applications peuvent utiliser les mêmes noms et des conflits peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-116">You should take care when naming custom attributes, however, because other application developers can use the same names, and conflicts can occur.</span></span>

<span data-ttu-id="e6c6f-117">Certains attributs sont définis par le kit de développement logiciel (SDK) et ne peuvent pas être modifiés manuellement.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-117">Some attributes are set by the SDK and cannot be changed manually.</span></span> <span data-ttu-id="e6c6f-118">Par exemple, lorsque vous indexez un fichier ASF, le kit de développement logiciel (SDK) définit l’attribut **g \_ wszWMSeekable** pour indiquer que le fichier peut désormais être lu à partir de n’importe quel point spécifié.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-118">For example, when you index an ASF file, the SDK sets the **g\_wszWMSeekable** attribute to show that the file can now be read from any specified point.</span></span>

<span data-ttu-id="e6c6f-119">D’autres attributs sont purement informatifs et doivent être définis manuellement.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-119">Other attributes are purely informational and must be set manually.</span></span> <span data-ttu-id="e6c6f-120">Par exemple, si vous souhaitez effectuer le suivi de l’auteur d’un fichier, vous devez définir **g \_ wszWMAuthor**.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-120">For example, if you want to keep track of the author of a file, you should set **g\_wszWMAuthor**.</span></span>

<span data-ttu-id="e6c6f-121">Le kit de développement logiciel (SDK) Windows Media format prend en charge les attributs qui s’appliquent à l’ensemble du fichier, ainsi que les attributs qui s’appliquent aux flux individuels.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-121">The Windows Media Format SDK provides support for attributes that apply to the entire file, and attributes that apply to individual streams.</span></span>

<span data-ttu-id="e6c6f-122">Vous pouvez utiliser le kit de développement logiciel (SDK) de format Windows Media pour modifier les métadonnées dans les fichiers MP3, même si vous devez toujours utiliser des attributs conformes à ID3 dans des fichiers MP3 pour maintenir la compatibilité avec d’autres programmes de manipulation MP3.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-122">You can use the Windows Media Format SDK to edit the metadata in MP3 files, though you should always use ID3-compliant attributes in MP3 files to maintain compatibility with other MP3 manipulation programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6c6f-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e6c6f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6c6f-124">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-124">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="e6c6f-125">**Éditeur de métadonnées, objet**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-125">**Metadata Editor Object**</span></span>](metadata-editor-object.md)
</dt> <dt>

[<span data-ttu-id="e6c6f-126">**Fonctionnalités de métadonnées**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-126">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="e6c6f-127">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-127">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




