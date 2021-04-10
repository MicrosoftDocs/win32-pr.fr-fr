---
description: Les modules de fusion multilingues, les transformations de langage et les fichiers CAB doivent être créés de telle sorte que l’ordre des fichiers corresponde à l’ordre spécifié dans la table de fichiers.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Classement de la séquence de fichiers dans le fichier CAB d’un module de fusion à plusieurs langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bdd00d8b09c0605b7ddcf656d87d41e3f53776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210777"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a><span data-ttu-id="bc27f-103">Classement de la séquence de fichiers dans le fichier CAB d’un module de fusion à plusieurs langues</span><span class="sxs-lookup"><span data-stu-id="bc27f-103">Ordering the File Sequence in the CAB of a Multiple Language Merge Module</span></span>

<span data-ttu-id="bc27f-104">Les modules de fusion multilingues, les transformations de langage et les fichiers CAB doivent être créés de telle sorte que l’ordre des fichiers dans le fichier. cab corresponde à l’ordre d’installation des fichiers spécifiés dans la [table de fichiers](file-table.md), même après l’application de la transformation de langue.</span><span class="sxs-lookup"><span data-stu-id="bc27f-104">Multiple-language merge modules, language transforms, and cabinet files must be authored such that the order of the files in the .cab matches the installation order of files specified in the [File Table](file-table.md), even after the application of the language transform.</span></span> <span data-ttu-id="bc27f-105">Si l’ordre dans le module et dans le fichier. cab ne correspond pas, le module de fusion ne peut pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="bc27f-105">If the order in the module and in the .cab do not match, the merge module cannot be used.</span></span>

<span data-ttu-id="bc27f-106">Assignez à chaque fichier dans le module, un numéro de séquence unique qui est indépendant de sa langue, puis utilisez toujours ce numéro de séquence pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="bc27f-106">Assign to each file in the module, a unique sequence number that is independent of its language, and then always use that sequence number for the file.</span></span> <span data-ttu-id="bc27f-107">Utilisez la même séquence lors de la génération du fichier CAB et de la création d’une transformation de langue.</span><span class="sxs-lookup"><span data-stu-id="bc27f-107">Use the same sequence when building the cabinet file and authoring a language transform.</span></span>

<span data-ttu-id="bc27f-108">Étant donné que le programme d’installation installe uniquement les fichiers répertoriés dans la [table de fichiers](file-table.md), l’utilisation d’une séquence de fichiers globale dans le fichier CAB, la [table de fichiers](file-table.md)et la transformation de langue permet à l’outil de fusion d’ignorer tous les fichiers supplémentaires stockés dans le fichier CAB qui ne sont pas répertoriés dans la table de [fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="bc27f-108">Because the Installer only installs the files listed in the [File Table](file-table.md), the use of a global file sequence in the cabinet, [File Table](file-table.md), and language transform enables the merge tool to skip any extra files stored in the cabinet that are not listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="bc27f-109">D’autres fichiers peuvent exister dans le fichier CAB, mais ils ne doivent pas être listés dans la [table file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="bc27f-109">Other files may exist in the cabinet, but they must not be listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="bc27f-110">Par exemple, un module qui installe Code.dll, anglais. dat, allemand. dat et français. dat peut utiliser l’ordre de séquence de fichiers Global suivant.</span><span class="sxs-lookup"><span data-stu-id="bc27f-110">For example, a module installing Code.dll, English.dat, German.dat, and French.dat can use the following global file sequence order.</span></span>



| <span data-ttu-id="bc27f-111">Fichier</span><span class="sxs-lookup"><span data-stu-id="bc27f-111">File</span></span>        | <span data-ttu-id="bc27f-112">Séquence</span><span class="sxs-lookup"><span data-stu-id="bc27f-112">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="bc27f-113">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="bc27f-113">Code.Dll</span></span>    | <span data-ttu-id="bc27f-114">1</span><span class="sxs-lookup"><span data-stu-id="bc27f-114">1</span></span>        |
| <span data-ttu-id="bc27f-115">Anglais. dat</span><span class="sxs-lookup"><span data-stu-id="bc27f-115">English.Dat</span></span> | <span data-ttu-id="bc27f-116">2</span><span class="sxs-lookup"><span data-stu-id="bc27f-116">2</span></span>        |
| <span data-ttu-id="bc27f-117">Allemand. dat</span><span class="sxs-lookup"><span data-stu-id="bc27f-117">German.Dat</span></span>  | <span data-ttu-id="bc27f-118">3</span><span class="sxs-lookup"><span data-stu-id="bc27f-118">3</span></span>        |
| <span data-ttu-id="bc27f-119">Français. dat</span><span class="sxs-lookup"><span data-stu-id="bc27f-119">French.Dat</span></span>  | <span data-ttu-id="bc27f-120">4</span><span class="sxs-lookup"><span data-stu-id="bc27f-120">4</span></span>        |



 

<span data-ttu-id="bc27f-121">Les transformations de langage peuvent ensuite être créées pour modifier la [table de fichiers](file-table.md) du module pour l’anglais, l’allemand ou le français.</span><span class="sxs-lookup"><span data-stu-id="bc27f-121">Language transforms can then be authored to modify the [File Table](file-table.md) of the module for English, German, or French.</span></span>

<span data-ttu-id="bc27f-122">[Table de fichiers](file-table.md) (partielle pour l’anglais)</span><span class="sxs-lookup"><span data-stu-id="bc27f-122">[File Table](file-table.md) (partial for English)</span></span>



| <span data-ttu-id="bc27f-123">Fichier</span><span class="sxs-lookup"><span data-stu-id="bc27f-123">File</span></span>        | <span data-ttu-id="bc27f-124">Séquence</span><span class="sxs-lookup"><span data-stu-id="bc27f-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="bc27f-125">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="bc27f-125">Code.Dll</span></span>    | <span data-ttu-id="bc27f-126">1</span><span class="sxs-lookup"><span data-stu-id="bc27f-126">1</span></span>        |
| <span data-ttu-id="bc27f-127">Anglais. dat</span><span class="sxs-lookup"><span data-stu-id="bc27f-127">English.Dat</span></span> | <span data-ttu-id="bc27f-128">2</span><span class="sxs-lookup"><span data-stu-id="bc27f-128">2</span></span>        |



 

<span data-ttu-id="bc27f-129">[Table de fichiers](file-table.md) (partielle pour l’allemand)</span><span class="sxs-lookup"><span data-stu-id="bc27f-129">[File Table](file-table.md) (partial for German)</span></span>



| <span data-ttu-id="bc27f-130">Fichier</span><span class="sxs-lookup"><span data-stu-id="bc27f-130">File</span></span>       | <span data-ttu-id="bc27f-131">Séquence</span><span class="sxs-lookup"><span data-stu-id="bc27f-131">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="bc27f-132">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="bc27f-132">Code.Dll</span></span>   | <span data-ttu-id="bc27f-133">1</span><span class="sxs-lookup"><span data-stu-id="bc27f-133">1</span></span>        |
| <span data-ttu-id="bc27f-134">Allemand. dat</span><span class="sxs-lookup"><span data-stu-id="bc27f-134">German.Dat</span></span> | <span data-ttu-id="bc27f-135">3</span><span class="sxs-lookup"><span data-stu-id="bc27f-135">3</span></span>        |



 

<span data-ttu-id="bc27f-136">[Table de fichiers](file-table.md) (partielle pour le français)</span><span class="sxs-lookup"><span data-stu-id="bc27f-136">[File Table](file-table.md) (partial for French)</span></span>



| <span data-ttu-id="bc27f-137">Fichier</span><span class="sxs-lookup"><span data-stu-id="bc27f-137">File</span></span>       | <span data-ttu-id="bc27f-138">Séquence</span><span class="sxs-lookup"><span data-stu-id="bc27f-138">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="bc27f-139">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="bc27f-139">Code.Dll</span></span>   | <span data-ttu-id="bc27f-140">1</span><span class="sxs-lookup"><span data-stu-id="bc27f-140">1</span></span>        |
| <span data-ttu-id="bc27f-141">Français. dat</span><span class="sxs-lookup"><span data-stu-id="bc27f-141">French.Dat</span></span> | <span data-ttu-id="bc27f-142">4</span><span class="sxs-lookup"><span data-stu-id="bc27f-142">4</span></span>        |



 

<span data-ttu-id="bc27f-143">Pour plus d’informations, consultez [création d’une transformation de langage pour un module de fusion multilingue](authoring-a-language-transform-for-a-multiple-language-merge-module.md) et [tables de fichiers de module de fusion de création](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bc27f-143">For more information, see [Authoring a Language Transform for a Multiple Language Merge Module](authoring-a-language-transform-for-a-multiple-language-merge-module.md) and [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

 

 



