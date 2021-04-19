---
description: ICE48 recherche des répertoires qui sont codés en dur sur des chemins d’accès locaux dans la table de propriétés.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521032"
---
# <a name="ice48"></a><span data-ttu-id="46526-103">ICE48</span><span class="sxs-lookup"><span data-stu-id="46526-103">ICE48</span></span>

<span data-ttu-id="46526-104">ICE48 recherche des répertoires qui sont codés en dur sur des chemins d’accès locaux dans la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="46526-104">ICE48 checks for directories that are hard-coded to local paths in the [Property table](property-table.md).</span></span>

<span data-ttu-id="46526-105">Ne codez pas en dur les chemins d’accès aux lecteurs locaux, car les ordinateurs diffèrent au cours de l’installation du lecteur local.</span><span class="sxs-lookup"><span data-stu-id="46526-105">Do not hard-code directory paths to local drives because computers differ in the setup of the local drive.</span></span> <span data-ttu-id="46526-106">Cette pratique peut être acceptable si vous déployez une application sur un grand nombre d’ordinateurs sur lesquels les portions appropriées des lecteurs sont identiques.</span><span class="sxs-lookup"><span data-stu-id="46526-106">This practice may be acceptable if deploying an application to a large number of computers on which the relevant portions of the drives are all the same.</span></span>

## <a name="result"></a><span data-ttu-id="46526-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="46526-107">Result</span></span>

<span data-ttu-id="46526-108">ICE48 publie un message d’erreur s’il existe un répertoire codé en dur vers un chemin d’accès local dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="46526-108">ICE48 posts an error message if there is a directory that is hard-coded to a local path in the Property table.</span></span>

## <a name="example"></a><span data-ttu-id="46526-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="46526-109">Example</span></span>

<span data-ttu-id="46526-110">ICE48 signale l’avertissement suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="46526-110">ICE48 would report the following warning for the example shown.</span></span>

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

<span data-ttu-id="46526-111">[Table de répertoires](directory-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="46526-111">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="46526-112">Répertoire</span><span class="sxs-lookup"><span data-stu-id="46526-112">Directory</span></span> | <span data-ttu-id="46526-113">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="46526-113">Directory\_Parent</span></span> | <span data-ttu-id="46526-114">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="46526-114">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="46526-115">Dir1</span><span class="sxs-lookup"><span data-stu-id="46526-115">Dir1</span></span>      |                   | <span data-ttu-id="46526-116">SourceDir</span><span class="sxs-lookup"><span data-stu-id="46526-116">SourceDir</span></span>  |



 

<span data-ttu-id="46526-117">[Table de propriétés](property-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="46526-117">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="46526-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="46526-118">Property</span></span> | <span data-ttu-id="46526-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="46526-119">Value</span></span>      |
|----------|------------|
| <span data-ttu-id="46526-120">Dir1</span><span class="sxs-lookup"><span data-stu-id="46526-120">Dir1</span></span>     | <span data-ttu-id="46526-121">d : \\ source</span><span class="sxs-lookup"><span data-stu-id="46526-121">d:\\source</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="46526-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="46526-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46526-123">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="46526-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



