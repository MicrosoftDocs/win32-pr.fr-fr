---
description: La table PatchSequence est utilisée pour générer la table MsiPatchSequence dans un correctif. La table requiert la version de PATCHWIZ.DLL disponible avec Windows Installer&\# 160 ; 3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Table PatchSequence (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868846"
---
# <a name="patchsequence-table-patchwizdll"></a><span data-ttu-id="3aeca-104">Table PatchSequence (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="3aeca-104">PatchSequence Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="3aeca-105">La table PatchSequence est utilisée pour générer la [table MsiPatchSequence](msipatchsequence-table.md) dans un correctif.</span><span class="sxs-lookup"><span data-stu-id="3aeca-105">The PatchSequence Table is used to generate the [MsiPatchSequence Table](msipatchsequence-table.md) in a patch.</span></span> <span data-ttu-id="3aeca-106">La table requiert la version de [PATCHWIZ.DLL](patchwiz-dll.md) disponible avec Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="3aeca-106">The table requires the version of [PATCHWIZ.DLL](patchwiz-dll.md) that is available with Windows Installer 3.0.</span></span>

<span data-ttu-id="3aeca-107">Le tableau suivant identifie les colonnes de la table PatchSequence.</span><span class="sxs-lookup"><span data-stu-id="3aeca-107">The following table identifies the columns of the PatchSequence Table.</span></span>



| <span data-ttu-id="3aeca-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="3aeca-108">Column</span></span>      | <span data-ttu-id="3aeca-109">Type</span><span class="sxs-lookup"><span data-stu-id="3aeca-109">Type</span></span>       | <span data-ttu-id="3aeca-110">Clé</span><span class="sxs-lookup"><span data-stu-id="3aeca-110">Key</span></span> | <span data-ttu-id="3aeca-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="3aeca-111">Nullable</span></span> |
|-------------|------------|-----|----------|
| <span data-ttu-id="3aeca-112">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="3aeca-112">PatchFamily</span></span> | <span data-ttu-id="3aeca-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="3aeca-113">Identifier</span></span> | <span data-ttu-id="3aeca-114">O</span><span class="sxs-lookup"><span data-stu-id="3aeca-114">Y</span></span>   | <span data-ttu-id="3aeca-115">N</span><span class="sxs-lookup"><span data-stu-id="3aeca-115">N</span></span>        |
| <span data-ttu-id="3aeca-116">Cible</span><span class="sxs-lookup"><span data-stu-id="3aeca-116">Target</span></span>      | <span data-ttu-id="3aeca-117">Texte</span><span class="sxs-lookup"><span data-stu-id="3aeca-117">Text</span></span>       | <span data-ttu-id="3aeca-118">O</span><span class="sxs-lookup"><span data-stu-id="3aeca-118">Y</span></span>   | <span data-ttu-id="3aeca-119">O</span><span class="sxs-lookup"><span data-stu-id="3aeca-119">Y</span></span>        |
| <span data-ttu-id="3aeca-120">Séquence</span><span class="sxs-lookup"><span data-stu-id="3aeca-120">Sequence</span></span>    | <span data-ttu-id="3aeca-121">Version</span><span class="sxs-lookup"><span data-stu-id="3aeca-121">Version</span></span>    |     | <span data-ttu-id="3aeca-122">O</span><span class="sxs-lookup"><span data-stu-id="3aeca-122">Y</span></span>        |
| <span data-ttu-id="3aeca-123">Remplacent</span><span class="sxs-lookup"><span data-stu-id="3aeca-123">Supersede</span></span>   | <span data-ttu-id="3aeca-124">Integer</span><span class="sxs-lookup"><span data-stu-id="3aeca-124">Integer</span></span>    |     | <span data-ttu-id="3aeca-125">O</span><span class="sxs-lookup"><span data-stu-id="3aeca-125">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="3aeca-126">Colonnes</span><span class="sxs-lookup"><span data-stu-id="3aeca-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3aeca-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span><span class="sxs-lookup"><span data-stu-id="3aeca-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="3aeca-128">Identificateur qui indique les familles de séquence auxquelles ce correctif appartient.</span><span class="sxs-lookup"><span data-stu-id="3aeca-128">The identifier that indicates the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="3aeca-129">Les valeurs des colonnes Target et PatchFamily définissent ensemble la clé primaire de la table.</span><span class="sxs-lookup"><span data-stu-id="3aeca-129">The values in the Target and PatchFamily columns together define the primary key for the table.</span></span> <span data-ttu-id="3aeca-130">Un correctif qui appartient à plusieurs familles de séquences, ou qui a des séquences différentes en fonction du code de produit de la cible, peut avoir une ligne pour chaque jumelage.</span><span class="sxs-lookup"><span data-stu-id="3aeca-130">A patch that belongs to multiple sequence families, or has different sequences depending on the product code of the target, can have one row for each pairing.</span></span> <span data-ttu-id="3aeca-131">Cette valeur est utilisée pour remplir la colonne PatchFamily de la [table MsiPatchSequence](msipatchsequence-table.md) qui appartient au correctif.</span><span class="sxs-lookup"><span data-stu-id="3aeca-131">This value is used to populate the PatchFamily column of the [MsiPatchSequence Table](msipatchsequence-table.md) that belongs to the patch.</span></span>

</dd> <dt>

<span data-ttu-id="3aeca-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Indicatif</span><span class="sxs-lookup"><span data-stu-id="3aeca-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="3aeca-133">La colonne cible est utilisée pour filtrer les PatchFamily par code de produit.</span><span class="sxs-lookup"><span data-stu-id="3aeca-133">The Target column is used to filter the PatchFamily by product code.</span></span>

<span data-ttu-id="3aeca-134">Une valeur NULL dans cette colonne indique que ce PatchFamily s’applique à toutes les cibles du correctif.</span><span class="sxs-lookup"><span data-stu-id="3aeca-134">A NULL value in this column indicates that this PatchFamily applies to all targets of the patch.</span></span> <span data-ttu-id="3aeca-135">Si cette colonne contient une clé étrangère à la [table TargetImages](targetimages-table-patchwiz-dll-.md), le code de produit de l’image spécifiée est récupéré et utilisé pour remplir la valeur de code du produit dans la ligne du nouveau correctif de la [table MsiPatchSequence](msipatchsequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="3aeca-135">If this column contains a foreign key to the [TargetImages Table](targetimages-table-patchwiz-dll-.md), the product code of the specified image is retrieved and used to populate the product code value in the new patch's row of the [MsiPatchSequence Table](msipatchsequence-table.md).</span></span> <span data-ttu-id="3aeca-136">Si cette colonne contient un GUID, le GUID est utilisé pour remplir la valeur de code de produit de la ligne dans la table MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="3aeca-136">If this column contains a GUID, the GUID is used to populate the product code value of the row in the MsiPatchSequence Table.</span></span>

</dd> <dt>

<span data-ttu-id="3aeca-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="3aeca-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="3aeca-138">La valeur dans la colonne séquence est utilisée pour remplir la colonne de séquence de la [table MsiPatchSequence](msipatchsequence-table.md) du nouveau fichier correctif.</span><span class="sxs-lookup"><span data-stu-id="3aeca-138">The value in the Sequence column is used to populate the Sequence column of the [MsiPatchSequence Table](msipatchsequence-table.md) of the new patch file.</span></span>

<span data-ttu-id="3aeca-139">Si la valeur est NULL, un numéro de séquence est généré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="3aeca-139">If the value is NULL, a sequence number is generated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="3aeca-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Remplacent</span><span class="sxs-lookup"><span data-stu-id="3aeca-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Supersede</span></span>
</dt> <dd>

<span data-ttu-id="3aeca-141">La valeur **msidbPatchSequenceSupersedeEarlier** ou 1 dans ce champ indique que ce correctif remplace les [petites mises à jour](small-updates.md) antérieures dans les familles de séquence auxquelles ce correctif appartient.</span><span class="sxs-lookup"><span data-stu-id="3aeca-141">A value of **msidbPatchSequenceSupersedeEarlier** or 1 in this field indicates that this patch supersedes earlier [small updates](small-updates.md) in the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="3aeca-142">La valeur de cette colonne est utilisée pour définir la colonne d’attributs de la ligne du nouveau correctif dans la [table MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="3aeca-142">The value in this column is used to set the Attributes column of the new patch's row in the [MsiPatchSequence Table](msipatchsequence-table.md) .</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="3aeca-143">Notes</span><span class="sxs-lookup"><span data-stu-id="3aeca-143">Remarks</span></span>

<span data-ttu-id="3aeca-144">Disponible à partir de Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="3aeca-144">Available beginning in Windows Installer 3.0.</span></span>

 

 



