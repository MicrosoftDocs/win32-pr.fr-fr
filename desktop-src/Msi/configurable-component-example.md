---
description: Cet exemple permet au consommateur de module de configurer indépendamment un contrôle d’édition, l’attribut checksum et l’attribut Compressed.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Exemple de composant configurable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533759"
---
# <a name="configurable-component-example"></a><span data-ttu-id="953bd-103">Exemple de composant configurable</span><span class="sxs-lookup"><span data-stu-id="953bd-103">Configurable Component Example</span></span>

<span data-ttu-id="953bd-104">Dans cet exemple, les tables ModuleConfiguration et ModuleSubstitution suivantes permettent au consommateur de module de configurer indépendamment l’attribut de mot de passe pour un contrôle d’édition, l’attribut de somme de contrôle pour un fichier et l’attribut compressé pour le même fichier.</span><span class="sxs-lookup"><span data-stu-id="953bd-104">In this example, the following ModuleConfiguration and ModuleSubstitution tables allows the module consumer to independently configure the Password attribute for an edit control, the checksum attribute for a file, and the compressed attribute for the same file.</span></span>

[<span data-ttu-id="953bd-105">Table ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="953bd-105">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="953bd-106">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="953bd-106">Table</span></span>   | <span data-ttu-id="953bd-107">Ligne</span><span class="sxs-lookup"><span data-stu-id="953bd-107">Row</span></span>           | <span data-ttu-id="953bd-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="953bd-108">Column</span></span>     | <span data-ttu-id="953bd-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="953bd-109">Value</span></span>                        |
|---------|---------------|------------|------------------------------|
| <span data-ttu-id="953bd-110">Contrôler</span><span class="sxs-lookup"><span data-stu-id="953bd-110">Control</span></span> | <span data-ttu-id="953bd-111">Dialog1; Edit1</span><span class="sxs-lookup"><span data-stu-id="953bd-111">Dialog1;Edit1</span></span> | <span data-ttu-id="953bd-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="953bd-112">Attributes</span></span> | <span data-ttu-id="953bd-113">\[= Mot de passe\]</span><span class="sxs-lookup"><span data-stu-id="953bd-113">\[=Password\]</span></span>                |
| <span data-ttu-id="953bd-114">Fichier</span><span class="sxs-lookup"><span data-stu-id="953bd-114">File</span></span>    | <span data-ttu-id="953bd-115">Fichier1</span><span class="sxs-lookup"><span data-stu-id="953bd-115">File1</span></span>         | <span data-ttu-id="953bd-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="953bd-116">Attributes</span></span> | <span data-ttu-id="953bd-117">\[= Checksum \] \[ = Compressed\]</span><span class="sxs-lookup"><span data-stu-id="953bd-117">\[=Checksum\]\[=Compressed\]</span></span> |



 

[<span data-ttu-id="953bd-118">Table ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="953bd-118">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md)



| <span data-ttu-id="953bd-119">Nom</span><span class="sxs-lookup"><span data-stu-id="953bd-119">Name</span></span>       | <span data-ttu-id="953bd-120">Format</span><span class="sxs-lookup"><span data-stu-id="953bd-120">Format</span></span>   | <span data-ttu-id="953bd-121">Type</span><span class="sxs-lookup"><span data-stu-id="953bd-121">Type</span></span> | <span data-ttu-id="953bd-122">ContextData</span><span class="sxs-lookup"><span data-stu-id="953bd-122">ContextData</span></span>                              | <span data-ttu-id="953bd-123">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="953bd-123">DefaultValue</span></span> | <span data-ttu-id="953bd-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="953bd-124">Attributes</span></span> | <span data-ttu-id="953bd-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="953bd-125">DisplayName</span></span> | <span data-ttu-id="953bd-126">Description</span><span class="sxs-lookup"><span data-stu-id="953bd-126">Description</span></span> |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| <span data-ttu-id="953bd-127">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="953bd-127">Password</span></span>   | <span data-ttu-id="953bd-128">Champ</span><span class="sxs-lookup"><span data-stu-id="953bd-128">Bitfield</span></span> |      | <span data-ttu-id="953bd-129">2097152 ; True = 2097152 ; False = 0</span><span class="sxs-lookup"><span data-stu-id="953bd-129">2097152;True=2097152;False=0</span></span>             | <span data-ttu-id="953bd-130">0</span><span class="sxs-lookup"><span data-stu-id="953bd-130">0</span></span>            | <span data-ttu-id="953bd-131">0</span><span class="sxs-lookup"><span data-stu-id="953bd-131">0</span></span>          |             |             |
| <span data-ttu-id="953bd-132">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="953bd-132">Checksum</span></span>   | <span data-ttu-id="953bd-133">Champ</span><span class="sxs-lookup"><span data-stu-id="953bd-133">Bitfield</span></span> |      | <span data-ttu-id="953bd-134">1024 ; Somme de contrôle = 1024 ; Aucune somme de contrôle = 0</span><span class="sxs-lookup"><span data-stu-id="953bd-134">1024;Checksum=1024;No Checksum=0</span></span>         | <span data-ttu-id="953bd-135">0</span><span class="sxs-lookup"><span data-stu-id="953bd-135">0</span></span>            | <span data-ttu-id="953bd-136">0</span><span class="sxs-lookup"><span data-stu-id="953bd-136">0</span></span>          |             |             |
| <span data-ttu-id="953bd-137">Compressé</span><span class="sxs-lookup"><span data-stu-id="953bd-137">Compressed</span></span> | <span data-ttu-id="953bd-138">Champ</span><span class="sxs-lookup"><span data-stu-id="953bd-138">Bitfield</span></span> |      | <span data-ttu-id="953bd-139">24576 ; Compressed = 16384 ; Non compressé = 8192</span><span class="sxs-lookup"><span data-stu-id="953bd-139">24576;Compressed=16384;Uncompressed=8192</span></span> | <span data-ttu-id="953bd-140">8 192</span><span class="sxs-lookup"><span data-stu-id="953bd-140">8192</span></span>         | <span data-ttu-id="953bd-141">0</span><span class="sxs-lookup"><span data-stu-id="953bd-141">0</span></span>          |             |             |



 

 

 



