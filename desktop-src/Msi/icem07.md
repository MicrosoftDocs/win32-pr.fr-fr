---
description: ICEM07 vérifie que l’ordre des fichiers dans la table de séquences correspond à l’ordre des fichiers dans MergeModule.CABinet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865766"
---
# <a name="icem07"></a><span data-ttu-id="b4c55-103">ICEM07</span><span class="sxs-lookup"><span data-stu-id="b4c55-103">ICEM07</span></span>

<span data-ttu-id="b4c55-104">ICEM07 vérifie que l’ordre des fichiers dans la table de séquences correspond à l’ordre des fichiers dans [MergeModule.CABinet](mergemodule-cabinet.md).</span><span class="sxs-lookup"><span data-stu-id="b4c55-104">ICEM07 verifies that the order of files in the sequence table matches the order of files in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span>

<span data-ttu-id="b4c55-105">Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.</span><span class="sxs-lookup"><span data-stu-id="b4c55-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="b4c55-106">Résultats</span><span class="sxs-lookup"><span data-stu-id="b4c55-106">Result</span></span>

<span data-ttu-id="b4c55-107">ICEM07 publie une erreur si l’ordre des fichiers dans la table de fichiers ne correspond pas à l’ordre dans le fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="b4c55-107">ICEM07 posts an error if the order of files in the File table does not match the order in the cabinet file.</span></span>

## <a name="example"></a><span data-ttu-id="b4c55-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="b4c55-108">Example</span></span>

<span data-ttu-id="b4c55-109">IC0M07 publie le message d’erreur suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="b4c55-109">IC0M07 would post the following error message for the example shown.</span></span>

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[<span data-ttu-id="b4c55-110">Table de fichier</span><span class="sxs-lookup"><span data-stu-id="b4c55-110">File Table</span></span>](file-table.md)



| <span data-ttu-id="b4c55-111">Fichier</span><span class="sxs-lookup"><span data-stu-id="b4c55-111">File</span></span>          | <span data-ttu-id="b4c55-112">Séquence</span><span class="sxs-lookup"><span data-stu-id="b4c55-112">Sequence</span></span> |
|---------------|----------|
| <span data-ttu-id="b4c55-113">Filea. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="b4c55-113">FileA.*GUID1*</span></span> | <span data-ttu-id="b4c55-114">1</span><span class="sxs-lookup"><span data-stu-id="b4c55-114">1</span></span>        |
| <span data-ttu-id="b4c55-115">FileB. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="b4c55-115">FileB.*GUID1*</span></span> | <span data-ttu-id="b4c55-116">8</span><span class="sxs-lookup"><span data-stu-id="b4c55-116">8</span></span>        |
| <span data-ttu-id="b4c55-117">FileC. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="b4c55-117">FileC.*GUID1*</span></span> | <span data-ttu-id="b4c55-118">52</span><span class="sxs-lookup"><span data-stu-id="b4c55-118">52</span></span>       |



 

<span data-ttu-id="b4c55-119">Intégration [MergeModule.CABinet](mergemodule-cabinet.md)</span><span class="sxs-lookup"><span data-stu-id="b4c55-119">Embedded [MergeModule.CABinet](mergemodule-cabinet.md)</span></span>



| <span data-ttu-id="b4c55-120">Fichier</span><span class="sxs-lookup"><span data-stu-id="b4c55-120">File</span></span>          |
|---------------|
| <span data-ttu-id="b4c55-121">Filea. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="b4c55-121">FileA.*GUID1*</span></span> |
| <span data-ttu-id="b4c55-122">FileC. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="b4c55-122">FileC.*GUID1*</span></span> |
| <span data-ttu-id="b4c55-123">Classer. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="b4c55-123">FileD.*GUID1*</span></span> |
| <span data-ttu-id="b4c55-124">FileB. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="b4c55-124">FileB.*GUID1*</span></span> |



 

<span data-ttu-id="b4c55-125">Bien qu’il ne soit pas nécessaire que les numéros de séquence de fichier de la table de fichiers soient consécutifs, et que des fichiers supplémentaires puissent exister dans le fichier CAB, la séquence relative de tous les fichiers de la table de fichiers doit correspondre à l’ordre dans [MergeModule.CABinet](mergemodule-cabinet.md).</span><span class="sxs-lookup"><span data-stu-id="b4c55-125">Although the file sequence numbers in the file table do not have to be consecutive, and extra files can exist in the cabinet file, the relative sequence of all files in the File table must match the order in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span> <span data-ttu-id="b4c55-126">Pour corriger cette erreur, modifiez le numéro de séquence de FileB à venir après FileC pour qu’il corresponde à l’ordre des fichiers dans le CAB, ou régénérez le fichier CAB avec les fichiers dans l’ordre approprié.</span><span class="sxs-lookup"><span data-stu-id="b4c55-126">To fix this error, change the sequence number of FileB to come after FileC to match the file order in the CAB, or rebuild the CAB with the files in the correct order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4c55-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4c55-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4c55-128">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="b4c55-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



