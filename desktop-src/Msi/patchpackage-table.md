---
description: Le tableau PatchPackage décrit tous les packages de correctifs qui ont été appliqués à ce produit. Pour chaque package de correctifs, l’identificateur unique du correctif est fourni, ainsi que des informations sur l’image de support sur laquelle le correctif est situé.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Table PatchPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210770"
---
# <a name="patchpackage-table"></a><span data-ttu-id="673ed-104">Table PatchPackage</span><span class="sxs-lookup"><span data-stu-id="673ed-104">PatchPackage Table</span></span>

<span data-ttu-id="673ed-105">Le tableau PatchPackage décrit tous les packages de correctifs qui ont été appliqués à ce produit.</span><span class="sxs-lookup"><span data-stu-id="673ed-105">The PatchPackage table describes all patch packages that have been applied to this product.</span></span> <span data-ttu-id="673ed-106">Pour chaque package de correctifs, l’identificateur unique du correctif est fourni, ainsi que des informations sur l’image de support sur laquelle le correctif est situé.</span><span class="sxs-lookup"><span data-stu-id="673ed-106">For each patch package, the unique identifier for the patch is provided along with information about the media image the on which the patch is located.</span></span>

<span data-ttu-id="673ed-107">La table PatchPackage contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="673ed-107">The PatchPackage table has the following columns.</span></span>



| <span data-ttu-id="673ed-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="673ed-108">Column</span></span>  | <span data-ttu-id="673ed-109">Type</span><span class="sxs-lookup"><span data-stu-id="673ed-109">Type</span></span>                   | <span data-ttu-id="673ed-110">Clé</span><span class="sxs-lookup"><span data-stu-id="673ed-110">Key</span></span> | <span data-ttu-id="673ed-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="673ed-111">Nullable</span></span> |
|---------|------------------------|-----|----------|
| <span data-ttu-id="673ed-112">PatchId</span><span class="sxs-lookup"><span data-stu-id="673ed-112">PatchId</span></span> | [<span data-ttu-id="673ed-113">GUID</span><span class="sxs-lookup"><span data-stu-id="673ed-113">GUID</span></span>](guid.md)       | <span data-ttu-id="673ed-114">O</span><span class="sxs-lookup"><span data-stu-id="673ed-114">Y</span></span>   | <span data-ttu-id="673ed-115">N</span><span class="sxs-lookup"><span data-stu-id="673ed-115">N</span></span>        |
| <span data-ttu-id="673ed-116">Multimédia\_</span><span class="sxs-lookup"><span data-stu-id="673ed-116">Media\_</span></span> | [<span data-ttu-id="673ed-117">Integer</span><span class="sxs-lookup"><span data-stu-id="673ed-117">Integer</span></span>](integer.md) | <span data-ttu-id="673ed-118">N</span><span class="sxs-lookup"><span data-stu-id="673ed-118">N</span></span>   | <span data-ttu-id="673ed-119">N</span><span class="sxs-lookup"><span data-stu-id="673ed-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="673ed-120">Colonnes</span><span class="sxs-lookup"><span data-stu-id="673ed-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="673ed-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span><span class="sxs-lookup"><span data-stu-id="673ed-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span></span>
</dt> <dd>

<span data-ttu-id="673ed-122">Cette colonne contient un identificateur unique pour ce correctif.</span><span class="sxs-lookup"><span data-stu-id="673ed-122">This column contains a unique identifier for this particular patch.</span></span>

</dd> <dt>

<span data-ttu-id="673ed-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_</span><span class="sxs-lookup"><span data-stu-id="673ed-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_</span></span>
</dt> <dd>

<span data-ttu-id="673ed-124">Cette colonne est une clé étrangère de la colonne depatinages de la [table Media](media-table.md) et indique le disque contenant le package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="673ed-124">This column is a foreign key to the DiskId column of the [Media Table](media-table.md) and indicates the disk containing the patch package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="673ed-125">Notes</span><span class="sxs-lookup"><span data-stu-id="673ed-125">Remarks</span></span>

<span data-ttu-id="673ed-126">La table PatchPackage est requise dans chaque package correctif.</span><span class="sxs-lookup"><span data-stu-id="673ed-126">The PatchPackage table is required in every patch package.</span></span> <span data-ttu-id="673ed-127">Si la table est manquante, les tentatives d’installation du correctif échouent avec « erreur 2768 : la transformation dans le package correctif n’est pas valide. »</span><span class="sxs-lookup"><span data-stu-id="673ed-127">If the table is missing, attempts to install the patch fail with "Error 2768: Transform in patch package is invalid."</span></span> <span data-ttu-id="673ed-128">Cette table est généralement ajoutée au package d’installation par une transformation à partir d’un package correctif.</span><span class="sxs-lookup"><span data-stu-id="673ed-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="673ed-129">En général, il n’est pas directement créé dans un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="673ed-129">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="673ed-130">Validation</span><span class="sxs-lookup"><span data-stu-id="673ed-130">Validation</span></span>

<dl>

[<span data-ttu-id="673ed-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="673ed-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="673ed-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="673ed-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



