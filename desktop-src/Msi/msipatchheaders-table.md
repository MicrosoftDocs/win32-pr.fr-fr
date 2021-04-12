---
description: La table MsiPatchHeaders contient les flux d’en-tête de correctifs binaires utilisés pour la validation des correctifs.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Table MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203197"
---
# <a name="msipatchheaders-table"></a><span data-ttu-id="f96ac-103">Table MsiPatchHeaders</span><span class="sxs-lookup"><span data-stu-id="f96ac-103">MsiPatchHeaders Table</span></span>

<span data-ttu-id="f96ac-104">La table MsiPatchHeaders contient les flux d’en-tête de correctifs binaires utilisés pour la validation des correctifs.</span><span class="sxs-lookup"><span data-stu-id="f96ac-104">The MsiPatchHeaders table holds the binary patch header streams used for patch validation.</span></span>

<span data-ttu-id="f96ac-105">La table MsiPatchHeaders est utilisée lorsque les clés de [table de fichiers](file-table.md) longs entraînent l’échec de la génération du flux d’en-tête de correctif dans la [table des correctifs](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="f96ac-105">The MsiPatchHeaders table is used when long [File table](file-table.md) keys result in a failure to generate the patch header stream in the [Patch table](patch-table.md).</span></span> <span data-ttu-id="f96ac-106">Cela peut être dû à la limitation du nom de flux décrite dans [restrictions OLE sur les flux](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="f96ac-106">This can be due to the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="f96ac-107">Dans ce cas, la table de correctifs peut faire référence à la table MsiPatchHeaders pour créer le flux d’en-tête de correctif.</span><span class="sxs-lookup"><span data-stu-id="f96ac-107">In this case, the Patch table can reference the MsiPatchHeaders table to create the patch header stream.</span></span>

<span data-ttu-id="f96ac-108">La table MsiPatchHeaders contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f96ac-108">The MsiPatchHeaders table has the following columns.</span></span>



| <span data-ttu-id="f96ac-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="f96ac-109">Column</span></span>    | <span data-ttu-id="f96ac-110">Type</span><span class="sxs-lookup"><span data-stu-id="f96ac-110">Type</span></span>                         | <span data-ttu-id="f96ac-111">Clé</span><span class="sxs-lookup"><span data-stu-id="f96ac-111">Key</span></span> | <span data-ttu-id="f96ac-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="f96ac-112">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="f96ac-113">StreamRef</span><span class="sxs-lookup"><span data-stu-id="f96ac-113">StreamRef</span></span> | [<span data-ttu-id="f96ac-114">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f96ac-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="f96ac-115">O</span><span class="sxs-lookup"><span data-stu-id="f96ac-115">Y</span></span>   | <span data-ttu-id="f96ac-116">N</span><span class="sxs-lookup"><span data-stu-id="f96ac-116">N</span></span>        |
| <span data-ttu-id="f96ac-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f96ac-117">Header</span></span>    | [<span data-ttu-id="f96ac-118">Binaire</span><span class="sxs-lookup"><span data-stu-id="f96ac-118">Binary</span></span>](binary.md)         | <span data-ttu-id="f96ac-119">N</span><span class="sxs-lookup"><span data-stu-id="f96ac-119">N</span></span>   | <span data-ttu-id="f96ac-120">N</span><span class="sxs-lookup"><span data-stu-id="f96ac-120">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f96ac-121">Colonnes</span><span class="sxs-lookup"><span data-stu-id="f96ac-121">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f96ac-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span><span class="sxs-lookup"><span data-stu-id="f96ac-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span></span>
</dt> <dd>

<span data-ttu-id="f96ac-123">Clé primaire de la table qui identifie de façon unique un en-tête de correctif spécifique.</span><span class="sxs-lookup"><span data-stu-id="f96ac-123">The primary key for the table that uniquely identifies a particular patch header.</span></span>

</dd> <dt>

<span data-ttu-id="f96ac-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Titre</span><span class="sxs-lookup"><span data-stu-id="f96ac-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="f96ac-125">Cette colonne est l’en-tête de correctif de flux binaire utilisé pour la validation des correctifs.</span><span class="sxs-lookup"><span data-stu-id="f96ac-125">This column is the binary stream patch header used for patch validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f96ac-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f96ac-126">Remarks</span></span>

<span data-ttu-id="f96ac-127">Cette table est traitée par l' [action PatchFiles](patchfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="f96ac-127">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="f96ac-128">Cette table est généralement ajoutée au package d’installation par une transformation à partir d’un package correctif.</span><span class="sxs-lookup"><span data-stu-id="f96ac-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="f96ac-129">En général, il n’est pas directement créé dans un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="f96ac-129">It is usually not authored directly into an installation package.</span></span>

## <a name="validation"></a><span data-ttu-id="f96ac-130">Validation</span><span class="sxs-lookup"><span data-stu-id="f96ac-130">Validation</span></span>

<dl>

[<span data-ttu-id="f96ac-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="f96ac-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f96ac-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="f96ac-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f96ac-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="f96ac-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



