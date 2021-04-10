---
description: ICE54 recherche les composants qui utilisent un fichier compagnon comme chemin d’accès de clé.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865477"
---
# <a name="ice54"></a><span data-ttu-id="244ee-103">ICE54</span><span class="sxs-lookup"><span data-stu-id="244ee-103">ICE54</span></span>

<span data-ttu-id="244ee-104">ICE54 recherche les composants qui utilisent un fichier compagnon comme chemin d’accès de clé.</span><span class="sxs-lookup"><span data-stu-id="244ee-104">ICE54 checks for components that use a companion file as their key path.</span></span>

<span data-ttu-id="244ee-105">Le fichier de chemin d’accès de clé d’un composant ne doit pas dériver sa version d’un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="244ee-105">The key path file of a component must not derive its version from a different file.</span></span> <span data-ttu-id="244ee-106">Cela peut entraîner l’échec de l’installation de certains fichiers.</span><span class="sxs-lookup"><span data-stu-id="244ee-106">This can cause some files to fail to install.</span></span> <span data-ttu-id="244ee-107">Pour plus d’informations sur les fichiers d’accompagnement, consultez la [table file](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="244ee-107">See the [File table](file-table.md) for more information about companion files.</span></span>

## <a name="result"></a><span data-ttu-id="244ee-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="244ee-108">Result</span></span>

<span data-ttu-id="244ee-109">ICE54 publie un avertissement si un composant a un fichier de chemin d’accès de clé qui dérive sa version d’un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="244ee-109">ICE54 posts a warning if any component has a key path file that derives its version from another file.</span></span>

## <a name="example"></a><span data-ttu-id="244ee-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="244ee-110">Example</span></span>

<span data-ttu-id="244ee-111">ICE54 retourne l’avertissement suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="244ee-111">ICE54 returns the following warning for the example shown.</span></span>

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

<span data-ttu-id="244ee-112">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="244ee-112">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="244ee-113">Composant</span><span class="sxs-lookup"><span data-stu-id="244ee-113">Component</span></span>  | <span data-ttu-id="244ee-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="244ee-114">Attribute</span></span> | <span data-ttu-id="244ee-115">KeyPath</span><span class="sxs-lookup"><span data-stu-id="244ee-115">KeyPath</span></span> |
|------------|-----------|---------|
| <span data-ttu-id="244ee-116">Composant1</span><span class="sxs-lookup"><span data-stu-id="244ee-116">Component1</span></span> | <span data-ttu-id="244ee-117">0</span><span class="sxs-lookup"><span data-stu-id="244ee-117">0</span></span>         | <span data-ttu-id="244ee-118">Fichier1</span><span class="sxs-lookup"><span data-stu-id="244ee-118">File1</span></span>   |



 

<span data-ttu-id="244ee-119">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="244ee-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="244ee-120">Fichier</span><span class="sxs-lookup"><span data-stu-id="244ee-120">File</span></span>  | <span data-ttu-id="244ee-121">Version</span><span class="sxs-lookup"><span data-stu-id="244ee-121">Version</span></span> | <span data-ttu-id="244ee-122">Language</span><span class="sxs-lookup"><span data-stu-id="244ee-122">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="244ee-123">Fichier1</span><span class="sxs-lookup"><span data-stu-id="244ee-123">File1</span></span> | <span data-ttu-id="244ee-124">Fichier2</span><span class="sxs-lookup"><span data-stu-id="244ee-124">File2</span></span>   |          |
| <span data-ttu-id="244ee-125">Fichier2</span><span class="sxs-lookup"><span data-stu-id="244ee-125">File2</span></span> | <span data-ttu-id="244ee-126">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="244ee-126">1.0.0.0</span></span> | <span data-ttu-id="244ee-127">1033</span><span class="sxs-lookup"><span data-stu-id="244ee-127">1033</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="244ee-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="244ee-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="244ee-129">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="244ee-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



