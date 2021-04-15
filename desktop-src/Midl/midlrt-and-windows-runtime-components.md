---
title: Composants MIDLRT et Windows Runtime
description: Montre comment créer des fichiers de métadonnées (. winmd) qui représentent l’API pour les composants de Windows Runtime personnalisés.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL du compilateur MIDL
- MIDL du compilateur MIDL, MIDL et Windows Runtime WinRT
- Windows Runtime MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508201"
---
# <a name="midlrt-and-windows-runtime-components"></a><span data-ttu-id="2768e-106">Composants MIDLRT et Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="2768e-106">MIDLRT and Windows Runtime components</span></span>

<span data-ttu-id="2768e-107">Montre comment créer des fichiers de métadonnées (. winmd) qui représentent l’API pour les composants de Windows Runtime personnalisés.</span><span class="sxs-lookup"><span data-stu-id="2768e-107">Shows how to create metadata (.winmd) files that represent the API for custom Windows Runtime components.</span></span>


<span data-ttu-id="2768e-108">Utilisez le compilateur MIDLRT pour générer des fichiers de métadonnées (. winmd) pour vos composants de Windows Runtime personnalisés.</span><span class="sxs-lookup"><span data-stu-id="2768e-108">Use the MIDLRT compiler to build metadata (.winmd) files for your custom Windows Runtime components.</span></span>

<span data-ttu-id="2768e-109">Lorsque vos fichiers de métadonnées sont générés, vous pouvez les composer dans un package plus efficace à l’aide de l’utilitaire MDMERGE.</span><span class="sxs-lookup"><span data-stu-id="2768e-109">When your metadata files are generated, you can compose them into a more efficient package by using the MDMERGE utility.</span></span> <span data-ttu-id="2768e-110">Pour plus d’informations, consultez [MDMERGE et fichiers de métadonnées](mdmerge-and-metadata-files.md).</span><span class="sxs-lookup"><span data-stu-id="2768e-110">For more info, see [MDMERGE and metadata files](mdmerge-and-metadata-files.md).</span></span>


<span data-ttu-id="2768e-111">L’utilisation de MIDLRT est similaire à l’utilisation du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="2768e-111">Using MIDLRT is similar to using the MIDL compiler.</span></span> <span data-ttu-id="2768e-112">Exécutez MIDLRT à partir de la ligne de commande à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2768e-112">Run MIDLRT from the command line using the following command:</span></span>

<span data-ttu-id="2768e-113">**midlrt**  *<* **options** _>_ **nom de fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="2768e-113">**midlrt** \*<\***options**_>_ **filename.idl**</span></span>

<span data-ttu-id="2768e-114">où \* < \***options** _>_ représente les options de ligne de commande que vous souhaitez utiliser, et nom_fichier. idl est le nom du fichier IDL à compiler.</span><span class="sxs-lookup"><span data-stu-id="2768e-114">where \*<\***options**_>_ represents the command-line options you want to use, and Filename.idl is the name of the IDL file to compile.</span></span>


<span data-ttu-id="2768e-115">La liste suivante répertorie les commutateurs de ligne de commande que MIDLRT.EXE utilise.</span><span class="sxs-lookup"><span data-stu-id="2768e-115">The following list shows the command-line switches that MIDLRT.EXE uses.</span></span>

<dl>

[<span data-ttu-id="2768e-116">**/enum ( \_ classe)**</span><span class="sxs-lookup"><span data-stu-id="2768e-116">**/enum\_class**</span></span>](-enum-class.md)  
[<span data-ttu-id="2768e-117">**/Metadata \_ dir**</span><span class="sxs-lookup"><span data-stu-id="2768e-117">**/metadata\_dir**</span></span>](-metadata-dir.md)  
[<span data-ttu-id="2768e-118">**/nomidl**</span><span class="sxs-lookup"><span data-stu-id="2768e-118">**/nomidl**</span></span>](-nomidl.md)  
[<span data-ttu-id="2768e-119">**/nomd**</span><span class="sxs-lookup"><span data-stu-id="2768e-119">**/nomd**</span></span>](-nomd.md)  
[<span data-ttu-id="2768e-120">**préfixe/NS \_**</span><span class="sxs-lookup"><span data-stu-id="2768e-120">**/ns\_prefix**</span></span>](-ns-prefix.md)  
[<span data-ttu-id="2768e-121">**/winmd**</span><span class="sxs-lookup"><span data-stu-id="2768e-121">**/winmd**</span></span>](-winmd.md)  
[<span data-ttu-id="2768e-122">**/WinRT**</span><span class="sxs-lookup"><span data-stu-id="2768e-122">**/winrt**</span></span>](-winrt.md)  
</dl>

<span data-ttu-id="2768e-123">Une liste complète des commutateurs et options du compilateur MIDLRT est disponible lorsque vous utilisez le compilateur MIDLRT [**/Help**](-help-.md) et/ ?</span><span class="sxs-lookup"><span data-stu-id="2768e-123">A complete listing of MIDLRT compiler switches and options is available when you use the MIDLRT compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="2768e-124">Active.</span><span class="sxs-lookup"><span data-stu-id="2768e-124">switches.</span></span> <span data-ttu-id="2768e-125">Les commutateurs sont organisés par catégories.</span><span class="sxs-lookup"><span data-stu-id="2768e-125">The switches are organized by categories.</span></span> <span data-ttu-id="2768e-126">Pour plus d’informations, consultez la [Référence du Command-Line MIDL](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2768e-126">For more info, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2768e-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2768e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2768e-128">Fichiers de métadonnées et MDMERGE</span><span class="sxs-lookup"><span data-stu-id="2768e-128">MDMERGE and metadata files</span></span>](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




