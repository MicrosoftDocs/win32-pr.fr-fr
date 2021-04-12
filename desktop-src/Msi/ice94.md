---
description: ICE94 vérifie le tableau de raccourcis, la table des fonctionnalités et la table MsiAssembly et publie un avertissement s’il existe des raccourcis non publiés pointant vers un fichier d’assembly dans le Global Assembly Cache.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209899"
---
# <a name="ice94"></a><span data-ttu-id="866c4-103">ICE94</span><span class="sxs-lookup"><span data-stu-id="866c4-103">ICE94</span></span>

<span data-ttu-id="866c4-104">ICE94 vérifie le tableau de [raccourcis](shortcut-table.md), la table des [fonctionnalités](feature-table.md)et la [table MsiAssembly](msiassembly-table.md) et publie un avertissement s’il existe des raccourcis non publiés pointant vers un fichier d’assembly dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="866c4-104">ICE94 checks the [Shortcut table](shortcut-table.md), [Feature table](feature-table.md), and [MsiAssembly table](msiassembly-table.md) and posts a warning if there are any unadvertised shortcuts pointing to an assembly file in the global assembly cache.</span></span> <span data-ttu-id="866c4-105">Si l’entrée dans le champ cible de la table de raccourcis n’est pas une fonctionnalité de la table de fonctionnalités, le raccourci n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="866c4-105">If the entry in the Target field of the Shortcut table is not a feature in the Feature table, the shortcut is unadvertised.</span></span> <span data-ttu-id="866c4-106">Si l’entrée dans le \_ champ composant du tableau de raccourcis est également indiquée dans la table MsiAssembly, le raccourci pointe vers un fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="866c4-106">If the entry in the Component\_ field of the Shortcut table is also listed in the MsiAssembly table, the shortcut points to an assembly file.</span></span> <span data-ttu-id="866c4-107">Si l’entrée dans le \_ champ application de fichier de la table MsiAssembly est vide, le fichier d’assembly se trouve dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="866c4-107">If the entry in the File\_Application field in the MsiAssembly table is empty, the assembly file is in the global assembly cache.</span></span>

## <a name="result"></a><span data-ttu-id="866c4-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="866c4-108">Result</span></span>

<span data-ttu-id="866c4-109">ICE94 publie l’avertissement suivant.</span><span class="sxs-lookup"><span data-stu-id="866c4-109">ICE94 posts the following warning.</span></span>



| <span data-ttu-id="866c4-110">AVERTISSEMENT ICE94</span><span class="sxs-lookup"><span data-stu-id="866c4-110">ICE94 warning</span></span>                                                                                | <span data-ttu-id="866c4-111">Description</span><span class="sxs-lookup"><span data-stu-id="866c4-111">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="866c4-112">Le raccourci' 2 'non publié \[ \] pointe vers un fichier d’assembly dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="866c4-112">The non-advertised shortcut '\[2\]' points to an assembly file in the global assembly cache.</span></span> | <span data-ttu-id="866c4-113">Un raccourci non publié pointe vers un fichier d’assembly dans le Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="866c4-113">An unadvertised shortcut is pointing to an assembly file in the global assembly cache.</span></span> |



 

## <a name="example"></a><span data-ttu-id="866c4-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="866c4-114">Example</span></span>

<span data-ttu-id="866c4-115">ICE94 signale l’erreur suivante pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="866c4-115">ICE94 reports the following error for the example:</span></span>

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

<span data-ttu-id="866c4-116">[Table de raccourcis](shortcut-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="866c4-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="866c4-117">Raccourci</span><span class="sxs-lookup"><span data-stu-id="866c4-117">Shortcut</span></span>  | <span data-ttu-id="866c4-118">-\_</span><span class="sxs-lookup"><span data-stu-id="866c4-118">Component\_</span></span> | <span data-ttu-id="866c4-119">Cible</span><span class="sxs-lookup"><span data-stu-id="866c4-119">Target</span></span>    |
|-----------|-------------|-----------|
| <span data-ttu-id="866c4-120">shortcut1</span><span class="sxs-lookup"><span data-stu-id="866c4-120">shortcut1</span></span> | <span data-ttu-id="866c4-121">c1</span><span class="sxs-lookup"><span data-stu-id="866c4-121">c1</span></span>          | <span data-ttu-id="866c4-122">\[file1\]</span><span class="sxs-lookup"><span data-stu-id="866c4-122">\[file1\]</span></span> |
| <span data-ttu-id="866c4-123">shortcut2</span><span class="sxs-lookup"><span data-stu-id="866c4-123">shortcut2</span></span> | <span data-ttu-id="866c4-124">c2</span><span class="sxs-lookup"><span data-stu-id="866c4-124">c2</span></span>          | <span data-ttu-id="866c4-125">Feature1</span><span class="sxs-lookup"><span data-stu-id="866c4-125">feature1</span></span>  |
| <span data-ttu-id="866c4-126">shortcut3</span><span class="sxs-lookup"><span data-stu-id="866c4-126">shortcut3</span></span> | <span data-ttu-id="866c4-127">c3</span><span class="sxs-lookup"><span data-stu-id="866c4-127">c3</span></span>          | <span data-ttu-id="866c4-128">\[fichier2\]</span><span class="sxs-lookup"><span data-stu-id="866c4-128">\[file2\]</span></span> |



 

<span data-ttu-id="866c4-129">[Table des fonctionnalités](feature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="866c4-129">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="866c4-130">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="866c4-130">Feature</span></span>  |
|----------|
| <span data-ttu-id="866c4-131">Feature1</span><span class="sxs-lookup"><span data-stu-id="866c4-131">feature1</span></span> |



 

<span data-ttu-id="866c4-132">[Table MsiAssembly](msiassembly-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="866c4-132">[MsiAssembly Table](msiassembly-table.md) (partial)</span></span>



| <span data-ttu-id="866c4-133">-\_</span><span class="sxs-lookup"><span data-stu-id="866c4-133">Component\_</span></span> | <span data-ttu-id="866c4-134">Application de fichier \_</span><span class="sxs-lookup"><span data-stu-id="866c4-134">File\_Application</span></span> |
|-------------|-------------------|
| <span data-ttu-id="866c4-135">c1</span><span class="sxs-lookup"><span data-stu-id="866c4-135">c1</span></span>          |                   |
| <span data-ttu-id="866c4-136">c2</span><span class="sxs-lookup"><span data-stu-id="866c4-136">c2</span></span>          |                   |
| <span data-ttu-id="866c4-137">c3</span><span class="sxs-lookup"><span data-stu-id="866c4-137">c3</span></span>          | <span data-ttu-id="866c4-138">fa1</span><span class="sxs-lookup"><span data-stu-id="866c4-138">fa1</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="866c4-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="866c4-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="866c4-140">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="866c4-140">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



