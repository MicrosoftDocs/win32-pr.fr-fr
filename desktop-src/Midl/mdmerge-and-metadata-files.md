---
title: Fichiers de métadonnées et MDMERGE
description: Compose plusieurs fichiers de métadonnées (. winmd) en un certain nombre de fichiers de métadonnées de sortie, en fonction de l’espace de noms.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- fichier winmd
- Métadonnées Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939697"
---
# <a name="mdmerge-and-metadata-files"></a><span data-ttu-id="acef0-106">Fichiers de métadonnées et MDMERGE</span><span class="sxs-lookup"><span data-stu-id="acef0-106">MDMERGE and metadata files</span></span>

<span data-ttu-id="acef0-107">Compose plusieurs fichiers de métadonnées (. winmd) en un certain nombre de fichiers de métadonnées de sortie, en fonction de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="acef0-107">Composes multiple metadata (.winmd) files into a number of output metadata files, based on namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="acef0-108">Utilisation</span><span class="sxs-lookup"><span data-stu-id="acef0-108">Usage</span></span>

<span data-ttu-id="acef0-109">Exécutez MDMERGE à partir de la ligne de commande à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="acef0-109">Run MDMERGE from the command line using the following command:</span></span>

<span data-ttu-id="acef0-110"> *< ***options*** de mdmerge>*</span><span class="sxs-lookup"><span data-stu-id="acef0-110">**mdmerge** *<***options***>*</span></span>

<span data-ttu-id="acef0-111">où *<  options >* représente les options de ligne de commande que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="acef0-111">where *<***options***>* represents the command-line options you want to use.</span></span>

<span data-ttu-id="acef0-112">Générez des fichiers de métadonnées pour vos composants de Windows Runtime personnalisés à l’aide du compilateur MIDLRT.</span><span class="sxs-lookup"><span data-stu-id="acef0-112">Generate metadata files for your custom Windows Runtime components by using the MIDLRT compiler.</span></span> <span data-ttu-id="acef0-113">Pour plus d’informations, consultez [MIDLRT et Windows Runtime Components](midlrt-and-windows-runtime-components.md).</span><span class="sxs-lookup"><span data-stu-id="acef0-113">For more info, see [MIDLRT and Windows Runtime components](midlrt-and-windows-runtime-components.md).</span></span>

## <a name="command-line-switches"></a><span data-ttu-id="acef0-114">Commutateurs de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="acef0-114">Command-line switches</span></span>

<span data-ttu-id="acef0-115">La liste suivante répertorie les commutateurs de ligne de commande utilisés par MDMERGE.</span><span class="sxs-lookup"><span data-stu-id="acef0-115">The following list shows the command-line switches that MDMERGE uses.</span></span>

<dl>

[<span data-ttu-id="acef0-116">**/i**</span><span class="sxs-lookup"><span data-stu-id="acef0-116">**/i**</span></span>](-mdmerge-i.md)  
[<span data-ttu-id="acef0-117">**/Metadata \_ dir**</span><span class="sxs-lookup"><span data-stu-id="acef0-117">**/metadata\_dir**</span></span>](-mdmerge-metadata-dir.md)  
[<span data-ttu-id="acef0-118">**/n**</span><span class="sxs-lookup"><span data-stu-id="acef0-118">**/n**</span></span>](-mdmerge-n.md)  
[<span data-ttu-id="acef0-119">**/o**</span><span class="sxs-lookup"><span data-stu-id="acef0-119">**/o**</span></span>](-mdmerge-o.md)  
[<span data-ttu-id="acef0-120">**/partial**</span><span class="sxs-lookup"><span data-stu-id="acef0-120">**/partial**</span></span>](-mdmerge-partial.md)  
[<span data-ttu-id="acef0-121">**/f**</span><span class="sxs-lookup"><span data-stu-id="acef0-121">**/v**</span></span>](-mdmerge-v.md)  
</dl>

<span data-ttu-id="acef0-122">Une liste complète des commutateurs et options du compilateur MDMERGE est disponible lorsque vous utilisez les options **-h** et **/ ?**</span><span class="sxs-lookup"><span data-stu-id="acef0-122">A complete listing of MDMERGE compiler switches and options is available when you use the **-h** and **/?**</span></span> <span data-ttu-id="acef0-123">Active.</span><span class="sxs-lookup"><span data-stu-id="acef0-123">switches.</span></span>

## <a name="remarks"></a><span data-ttu-id="acef0-124">Notes</span><span class="sxs-lookup"><span data-stu-id="acef0-124">Remarks</span></span>

<span data-ttu-id="acef0-125">La composition des métadonnées permet à plusieurs fichiers IDL de contenir des définitions pour Windows Runtime composants dans le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="acef0-125">Metadata composition enables multiple IDL files to contain definitions for Windows Runtime components in the same namespace.</span></span> <span data-ttu-id="acef0-126">Cela vous évite de définir tous les types dans un espace de noms au sein d’un seul fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="acef0-126">This frees you from defining all of the types in a namespace within a single IDL file.</span></span>

<span data-ttu-id="acef0-127">Vous pouvez avoir de nombreux composants de Windows Runtime que vos applications utilisent.</span><span class="sxs-lookup"><span data-stu-id="acef0-127">You're likely to have numerous Windows Runtime components that your apps use.</span></span> <span data-ttu-id="acef0-128">Lorsque vous effectuez l’étape finale pour produire des assemblys de métadonnées Windows Runtime déployables, vous pouvez configurer MDMERGE pour fusionner des composants à partir de plusieurs répertoires de métadonnées, comme ceux qui sont installés avec le système (% WINDOWS% \\ system32 \\ WinMetadata), vos types de fondation et le répertoire de build de votre projet actuel.</span><span class="sxs-lookup"><span data-stu-id="acef0-128">When you perform the final step to produce deployable Windows Runtime metadata assemblies, you can configure MDMERGE to merge components from multiple metadata directories, like those that are installed with the system (%WINDOWS%\\system32\\WinMetadata), your foundation types, and your current project’s build directory.</span></span> <span data-ttu-id="acef0-129">Tous les types nécessaires sont fusionnés dans les assemblys de métadonnées appropriés et déployables que vous pouvez empaqueter pour le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="acef0-129">All necessary types are merged into the correct, deployable, metadata assemblies that you can package for the Windows Store.</span></span>

<span data-ttu-id="acef0-130">Vous pouvez utiliser l’option [**/n**](-mdmerge-n.md) pour spécifier la profondeur d’espace de noms prise en charge pour composer des assemblys de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="acef0-130">You can use the [**/n**](-mdmerge-n.md) option to specify the supported namespace depth for composing metadata assemblies.</span></span> <span data-ttu-id="acef0-131">Cela permet de configurer une division à chaud pour vos composants Windows Runtime, afin qu’un seul fichier. winmd soit empaqueté au lieu de plusieurs.</span><span class="sxs-lookup"><span data-stu-id="acef0-131">This enables configuring a hot split for your Windows Runtime components, so that only a single .winmd file is packaged instead of many.</span></span> <span data-ttu-id="acef0-132">Cela réduit le temps de chargement et l’e/s de fichier requis par vos applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="acef0-132">This reduces the load times and file I/O required by your Windows Store apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acef0-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="acef0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acef0-134">Composants MIDLRT et Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="acef0-134">MIDLRT and Windows Runtime components</span></span>](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




