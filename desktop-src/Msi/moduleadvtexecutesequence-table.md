---
description: Un outil de fusion évalue la table ModuleAdvtExecuteSequence, puis insère les actions calculées dans la table AdvtExecuteSequence avec un numéro de séquence correct.
ms.assetid: ed2d1159-da78-4dc5-98a2-2cc876380c43
title: Table ModuleAdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699e544df7e0a92b0fee92c753e36a8b9a86ee5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521132"
---
# <a name="moduleadvtexecutesequence-table"></a><span data-ttu-id="7983a-103">Table ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="7983a-103">ModuleAdvtExecuteSequence Table</span></span>

<span data-ttu-id="7983a-104">Un outil de fusion évalue la table ModuleAdvtExecuteSequence, puis insère les actions calculées dans la [table AdvtExecuteSequence](advtexecutesequence-table.md) avec un numéro de séquence correct.</span><span class="sxs-lookup"><span data-stu-id="7983a-104">A merge tool evaluates the ModuleAdvtExecuteSequence table and then inserts the calculated actions into the [AdvtExecuteSequence table](advtexecutesequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="7983a-105">La table ModuleAdvtExecuteSequence contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7983a-105">The ModuleAdvtExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="7983a-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="7983a-106">Column</span></span>     | <span data-ttu-id="7983a-107">Type</span><span class="sxs-lookup"><span data-stu-id="7983a-107">Type</span></span>                         | <span data-ttu-id="7983a-108">Clé</span><span class="sxs-lookup"><span data-stu-id="7983a-108">Key</span></span> | <span data-ttu-id="7983a-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="7983a-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="7983a-110">Action</span><span class="sxs-lookup"><span data-stu-id="7983a-110">Action</span></span>     | [<span data-ttu-id="7983a-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="7983a-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="7983a-112">O</span><span class="sxs-lookup"><span data-stu-id="7983a-112">Y</span></span>   | <span data-ttu-id="7983a-113">N</span><span class="sxs-lookup"><span data-stu-id="7983a-113">N</span></span>        |
| <span data-ttu-id="7983a-114">Séquence</span><span class="sxs-lookup"><span data-stu-id="7983a-114">Sequence</span></span>   | [<span data-ttu-id="7983a-115">Integer</span><span class="sxs-lookup"><span data-stu-id="7983a-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="7983a-116">O</span><span class="sxs-lookup"><span data-stu-id="7983a-116">Y</span></span>        |
| <span data-ttu-id="7983a-117">BaseAction</span><span class="sxs-lookup"><span data-stu-id="7983a-117">BaseAction</span></span> | [<span data-ttu-id="7983a-118">Identificateur</span><span class="sxs-lookup"><span data-stu-id="7983a-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="7983a-119">O</span><span class="sxs-lookup"><span data-stu-id="7983a-119">Y</span></span>        |
| <span data-ttu-id="7983a-120">After</span><span class="sxs-lookup"><span data-stu-id="7983a-120">After</span></span>      | [<span data-ttu-id="7983a-121">Integer</span><span class="sxs-lookup"><span data-stu-id="7983a-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="7983a-122">O</span><span class="sxs-lookup"><span data-stu-id="7983a-122">Y</span></span>        |
| <span data-ttu-id="7983a-123">Condition</span><span class="sxs-lookup"><span data-stu-id="7983a-123">Condition</span></span>  | [<span data-ttu-id="7983a-124">Condition</span><span class="sxs-lookup"><span data-stu-id="7983a-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="7983a-125">O</span><span class="sxs-lookup"><span data-stu-id="7983a-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7983a-126">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7983a-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7983a-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="7983a-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="7983a-128">Action à insérer dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="7983a-128">Action to insert into sequence.</span></span> <span data-ttu-id="7983a-129">Fait référence à l’une des [actions standard](standard-actions.md)du programme d’installation ou à une entrée de la table ou de la table de [boîtes de dialogue](dialog-table.md) [CustomAction](customaction-table.md) du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="7983a-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md) or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="7983a-130">Si une [action standard](standard-actions.md) est utilisée dans la colonne action d’une table de séquence de module de fusion, les colonnes BaseAction et after de cet enregistrement doivent avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="7983a-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be Null.</span></span>

</dd> <dt>

<span data-ttu-id="7983a-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="7983a-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="7983a-132">Numéro de séquence d’une action standard.</span><span class="sxs-lookup"><span data-stu-id="7983a-132">The sequence number of a standard action.</span></span> <span data-ttu-id="7983a-133">Si une action ou une boîte de dialogue personnalisée est entrée dans la colonne action de cette ligne, ce champ doit avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="7983a-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to Null.</span></span>

<span data-ttu-id="7983a-134">Lorsque vous utilisez des [actions standard](standard-actions.md) dans les tables de séquence de module de fusion, la valeur dans la colonne Sequence doit être le numéro de séquence d’action recommandé.</span><span class="sxs-lookup"><span data-stu-id="7983a-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="7983a-135">Si le numéro de séquence du module de fusion diffère de celui de la même action dans le tableau séquence de fichiers. msi, l’outil de fusion utilise le numéro de séquence du fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="7983a-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="7983a-136">Consultez les séquences suggérées dans [à l’aide d’une table de séquences](using-a-sequence-table.md) pour connaître les numéros de séquence recommandés pour les actions standard.</span><span class="sxs-lookup"><span data-stu-id="7983a-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="7983a-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span><span class="sxs-lookup"><span data-stu-id="7983a-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="7983a-138">La colonne BaseAction peut contenir une action standard, une action personnalisée spécifiée dans la table d’actions personnalisée du module de fusion ou une boîte de dialogue spécifiée dans la table de boîte de dialogue du module.</span><span class="sxs-lookup"><span data-stu-id="7983a-138">The BaseAction column can contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="7983a-139">La colonne BaseAction est une clé dans la colonne action de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="7983a-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="7983a-140">Il ne peut pas s’agir d’une clé étrangère dans une autre table ou table de fusion du fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="7983a-140">It cannot be a foreign key into another merge table or table in the .msi file.</span></span> <span data-ttu-id="7983a-141">Cela signifie que chaque action standard, action personnalisée ou boîte de dialogue figurant dans la colonne BaseAction doit également figurer dans la colonne action d’un autre enregistrement dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="7983a-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="7983a-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>Postérieur</span><span class="sxs-lookup"><span data-stu-id="7983a-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="7983a-143">Valeur booléenne indiquant si l’action vient avant ou après BaseAction.</span><span class="sxs-lookup"><span data-stu-id="7983a-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="7983a-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="7983a-144">Value</span></span> | <span data-ttu-id="7983a-145">Signification</span><span class="sxs-lookup"><span data-stu-id="7983a-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="7983a-146">0</span><span class="sxs-lookup"><span data-stu-id="7983a-146">0</span></span>     | <span data-ttu-id="7983a-147">Action à venir avant BaseAction</span><span class="sxs-lookup"><span data-stu-id="7983a-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="7983a-148">1</span><span class="sxs-lookup"><span data-stu-id="7983a-148">1</span></span>     | <span data-ttu-id="7983a-149">Action à venir après BaseAction</span><span class="sxs-lookup"><span data-stu-id="7983a-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="7983a-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="7983a-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="7983a-151">Instruction conditionnelle qui indique si l’action est exécutée.</span><span class="sxs-lookup"><span data-stu-id="7983a-151">A conditional statement that indicates if the action is be executed.</span></span> <span data-ttu-id="7983a-152">NULL prend la valeur true.</span><span class="sxs-lookup"><span data-stu-id="7983a-152">Null evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7983a-153">Notes</span><span class="sxs-lookup"><span data-stu-id="7983a-153">Remarks</span></span>

<span data-ttu-id="7983a-154">Si cette table est présente, la [table AdvtExecuteSequence](advtexecutesequence-table.md) doit également être présente dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="7983a-154">If this table is present the [AdvtExecuteSequence table](advtexecutesequence-table.md) must also be present in the merge module.</span></span>

 

 



