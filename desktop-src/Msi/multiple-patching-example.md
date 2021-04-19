---
description: L’exemple suivant montre comment Windows Installer 3,0 et versions ultérieures peuvent être utilisés pour appliquer des correctifs dans l’ordre dans lequel ils sont créés.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Exemple de mise à jour corrective multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534455"
---
# <a name="multiple-patching-example"></a><span data-ttu-id="12084-103">Exemple de mise à jour corrective multiple</span><span class="sxs-lookup"><span data-stu-id="12084-103">Multiple Patching Example</span></span>

<span data-ttu-id="12084-104">L’exemple suivant montre comment Windows Installer 3,0 et versions ultérieures peuvent être utilisés pour appliquer des correctifs dans l’ordre dans lequel ils sont créés.</span><span class="sxs-lookup"><span data-stu-id="12084-104">The following example shows how Windows Installer 3.0 and later can be used to apply patches in the order in which they are authored.</span></span>

## <a name="example"></a><span data-ttu-id="12084-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="12084-105">Example</span></span>

<span data-ttu-id="12084-106">Dans cet exemple, il existe trois correctifs, QFE1, QFE2 et ServicePack1, et chacun d’eux a une table [MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="12084-106">In this example there are three patches, QFE1, QFE2, and ServicePack1, and they each have a [MsiPatchSequence](msipatchsequence-table.md) table.</span></span> <span data-ttu-id="12084-107">Ces correctifs ont été créés pour être appliqués à la version 1,0 de l’application.</span><span class="sxs-lookup"><span data-stu-id="12084-107">These patches have been authored to be applied to version 1.0 of the application.</span></span>



| <span data-ttu-id="12084-108">Nom du correctif</span><span class="sxs-lookup"><span data-stu-id="12084-108">Patch Name</span></span>   | <span data-ttu-id="12084-109">Type de correctif</span><span class="sxs-lookup"><span data-stu-id="12084-109">Patch Type</span></span>    | <span data-ttu-id="12084-110">Numéro de séquence</span><span class="sxs-lookup"><span data-stu-id="12084-110">Sequence Number</span></span> |
|--------------|---------------|-----------------|
| <span data-ttu-id="12084-111">QFE1</span><span class="sxs-lookup"><span data-stu-id="12084-111">QFE1</span></span>         | <span data-ttu-id="12084-112">Petite mise à jour</span><span class="sxs-lookup"><span data-stu-id="12084-112">Small Update</span></span>  | <span data-ttu-id="12084-113">1.1.0</span><span class="sxs-lookup"><span data-stu-id="12084-113">1.1.0</span></span>           |
| <span data-ttu-id="12084-114">QFE2</span><span class="sxs-lookup"><span data-stu-id="12084-114">QFE2</span></span>         | <span data-ttu-id="12084-115">Petite mise à jour</span><span class="sxs-lookup"><span data-stu-id="12084-115">Small Update</span></span>  | <span data-ttu-id="12084-116">1.2.0</span><span class="sxs-lookup"><span data-stu-id="12084-116">1.2.0</span></span>           |
| <span data-ttu-id="12084-117">ServicePack1</span><span class="sxs-lookup"><span data-stu-id="12084-117">ServicePack1</span></span> | <span data-ttu-id="12084-118">Mise à niveau mineure</span><span class="sxs-lookup"><span data-stu-id="12084-118">Minor Upgrade</span></span> | <span data-ttu-id="12084-119">1.3.0</span><span class="sxs-lookup"><span data-stu-id="12084-119">1.3.0</span></span>           |



 

<span data-ttu-id="12084-120">La table [MsiPatchSequence](msipatchsequence-table.md) de chaque correctif n’a qu’un seul enregistrement qui contient la famille des correctifs, le code du produit et le numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="12084-120">The [MsiPatchSequence](msipatchsequence-table.md) table of each patch has only one record that contains the patch family, product code, and sequence number.</span></span> <span data-ttu-id="12084-121">Les trois correctifs sont tous appliqués au même produit et appartiennent à la même famille de correctifs, nommée AppPatch.</span><span class="sxs-lookup"><span data-stu-id="12084-121">The three patches are all applied to the same product and belong to the same patch family, named AppPatch.</span></span> <span data-ttu-id="12084-122">Aucun des correctifs n’a l’attribut **msidbPatchSequenceSupersedeEarlier** .</span><span class="sxs-lookup"><span data-stu-id="12084-122">None of the patches have the **msidbPatchSequenceSupersedeEarlier** attribute.</span></span>

<span data-ttu-id="12084-123">[Table MsiPatchSequence](msipatchsequence-table.md) pour la [petite mise à jour](small-updates.md)qfe1.</span><span class="sxs-lookup"><span data-stu-id="12084-123">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE1 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="12084-124">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="12084-124">PatchFamily</span></span> | <span data-ttu-id="12084-125">ProductCode</span><span class="sxs-lookup"><span data-stu-id="12084-125">ProductCode</span></span>                            | <span data-ttu-id="12084-126">Séquence</span><span class="sxs-lookup"><span data-stu-id="12084-126">Sequence</span></span> | <span data-ttu-id="12084-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="12084-127">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="12084-128">AppPatch</span><span class="sxs-lookup"><span data-stu-id="12084-128">AppPatch</span></span>    | <span data-ttu-id="12084-129">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="12084-129">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="12084-130">1.1.0</span><span class="sxs-lookup"><span data-stu-id="12084-130">1.1.0</span></span>    |            |



 

<span data-ttu-id="12084-131">[Table MsiPatchSequence](msipatchsequence-table.md) pour la [petite mise à jour](small-updates.md)QFE2.</span><span class="sxs-lookup"><span data-stu-id="12084-131">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE2 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="12084-132">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="12084-132">PatchFamily</span></span> | <span data-ttu-id="12084-133">ProductCode</span><span class="sxs-lookup"><span data-stu-id="12084-133">ProductCode</span></span>                            | <span data-ttu-id="12084-134">Séquence</span><span class="sxs-lookup"><span data-stu-id="12084-134">Sequence</span></span> | <span data-ttu-id="12084-135">Attributs</span><span class="sxs-lookup"><span data-stu-id="12084-135">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="12084-136">AppPatch</span><span class="sxs-lookup"><span data-stu-id="12084-136">AppPatch</span></span>    | <span data-ttu-id="12084-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="12084-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="12084-138">1.2.0</span><span class="sxs-lookup"><span data-stu-id="12084-138">1.2.0</span></span>    |            |



 

<span data-ttu-id="12084-139">[Table MsiPatchSequence](msipatchsequence-table.md) pour la [mise à niveau mineure](minor-upgrades.md)ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="12084-139">[MsiPatchSequence Table](msipatchsequence-table.md) for ServicePack1 [minor upgrade](minor-upgrades.md).</span></span> 

| <span data-ttu-id="12084-140">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="12084-140">PatchFamily</span></span> | <span data-ttu-id="12084-141">ProductCode</span><span class="sxs-lookup"><span data-stu-id="12084-141">ProductCode</span></span>                            | <span data-ttu-id="12084-142">Séquence</span><span class="sxs-lookup"><span data-stu-id="12084-142">Sequence</span></span> | <span data-ttu-id="12084-143">Attributs</span><span class="sxs-lookup"><span data-stu-id="12084-143">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="12084-144">AppPatch</span><span class="sxs-lookup"><span data-stu-id="12084-144">AppPatch</span></span>    | <span data-ttu-id="12084-145">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="12084-145">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="12084-146">1.3.0</span><span class="sxs-lookup"><span data-stu-id="12084-146">1.3.0</span></span>    |            |



 

<span data-ttu-id="12084-147">Si un utilisateur installe la version 1,0 du produit, puis applique QFE2, puis qu’à une date ultérieure décide d’appliquer QFE1, Windows Installer garantit que la séquence effective de l’application de correctifs au produit est QFE1 appliquée avant QFE2.</span><span class="sxs-lookup"><span data-stu-id="12084-147">If a user installs version 1.0 of the product, and then applies QFE2, and then at a later date decides to apply QFE1, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 applied ahead of QFE2.</span></span> <span data-ttu-id="12084-148">Si l’utilisateur applique ServicePack1, puis applique QFE2 et QFE1 à une date ultérieure, Windows Installer garantit que la séquence effective de l’application de correctifs au produit est QFE1 en avance de QFE2 et en avance sur ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="12084-148">If the user applies ServicePack1, then applies QFE2 and QFE1 together at a later date, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 ahead of QFE2 and ahead of ServicePack1.</span></span>

<span data-ttu-id="12084-149">Si ServicePack1 a **msidbPatchSequenceSupersedeEarlier** défini dans la colonne attributs de sa table [MsiPatchSequence](msipatchsequence-table.md) , cela signifie que l’Service Pack contient toutes les modifications apportées à qfe1 et QFE2.</span><span class="sxs-lookup"><span data-stu-id="12084-149">If ServicePack1 has **msidbPatchSequenceSupersedeEarlier** set in the Attributes column of its [MsiPatchSequence](msipatchsequence-table.md) table, this means that the service pack contains all the changes in QFE1 and QFE2.</span></span> <span data-ttu-id="12084-150">Dans ce cas, QFE1 et QFE2 ne sont pas appliqués lorsque ServicePack1 est appliqué.</span><span class="sxs-lookup"><span data-stu-id="12084-150">In this case, QFE1 and QFE2 are not applied when ServicePack1 is applied.</span></span>

<span data-ttu-id="12084-151">**Windows Installer 2,0 :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="12084-151">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="12084-152">Les versions antérieures à Windows Installer 3,0 peuvent installer un seul correctif par transaction et les correctifs sont appliqués dans l’ordre dans lequel ils sont fournis.</span><span class="sxs-lookup"><span data-stu-id="12084-152">Versions earlier than Windows Installer 3.0 can install only one patch per transaction and patches are applied in the sequence that they are provided.</span></span> <span data-ttu-id="12084-153">Pour l’exemple précédent, si QFE2 est appliqué en premier, puis QFE1 est appliqué, il s’agit de deux transactions et les correctifs sont appliqués à la version 1,0 de l’application dans la séquence QFE2 suivie de QFE1.</span><span class="sxs-lookup"><span data-stu-id="12084-153">For the preceding example, if QFE2 is applied first and then QFE1 is applied, that is two transactions and the patches are applied to version 1.0 of the application in the sequence QFE2 followed by QFE1.</span></span> <span data-ttu-id="12084-154">Si ServicePack1 est appliqué en premier, QFE1 ou QFE2 ne peut pas être appliqué dans une transaction ultérieure, car ServicePack1 est une mise à niveau mineure qui modifie la version de l’application.</span><span class="sxs-lookup"><span data-stu-id="12084-154">If ServicePack1 is applied first, then QFE1 or QFE2 cannot be applied in a later transaction because ServicePack1 is a minor upgrade that changes the application version.</span></span> <span data-ttu-id="12084-155">QFE1 et QFE2 peuvent être appliqués uniquement à la version 1,0 de l’application.</span><span class="sxs-lookup"><span data-stu-id="12084-155">QFE1 and QFE2 can only be applied to version 1.0 of the application.</span></span>

 

 



