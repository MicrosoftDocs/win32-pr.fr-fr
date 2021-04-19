---
description: Cette table temporaire active l’option de désinstallation correctif de l’action personnalisée pour les actions personnalisées ajoutées ou mises à jour par un correctif.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536806"
---
# <a name="msitransformview"></a><span data-ttu-id="cc7c3-103">MsiTransformView</span><span class="sxs-lookup"><span data-stu-id="cc7c3-103">MsiTransformView</span></span>

<span data-ttu-id="cc7c3-104">Cette table temporaire active l' [option de désinstallation correctif de l’action personnalisée](custom-action-patch-uninstall-option.md) pour les actions personnalisées ajoutées ou mises à jour par un correctif.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-104">This temporary table enables the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) for custom actions added or updated by a patch.</span></span>

<span data-ttu-id="cc7c3-105">Si un correctif ajoute ou met à jour une action personnalisée ayant l’attribut **msidbCustomActionTypePatchUninstall** , Windows Installer exécute l’action personnalisée nouvelle ou mise à jour lorsque le correctif est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-105">If a patch adds or updates a custom action having the **msidbCustomActionTypePatchUninstall** attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="cc7c3-106">Windows Installer rend les mises à jour dans le correctif en cours de désinstallation disponibles pour l’action personnalisée de désinstallation des correctifs.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-106">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="cc7c3-107">Le correctif doit inclure une *<PatchGUID>* table MsiTransformView pour fournir ces informations à Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-107">The patch must include a MsiTransformView *<PatchGUID>* table to provide this information to Windows Installer.</span></span> <span data-ttu-id="cc7c3-108">Les informations contenues dans ce tableau sont disponibles pour toute action personnalisée immédiate et ne sont pas disponibles pour les actions personnalisées différées.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-108">The information in this table is available to any immediate custom action, and is unavailable to deferred custom actions.</span></span>

<span data-ttu-id="cc7c3-109">**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="cc7c3-110">L' [option de désinstallation corrective de l’action personnalisée](custom-action-patch-uninstall-option.md) est disponible à partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-110">The [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="cc7c3-111">Ce tableau doit être nommé MsiTransformView *<PatchGUID>* table, où *<PatchGUID>* est le GUID qui identifie de façon unique le correctif.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-111">This table should be named MsiTransformView *<PatchGUID>* Table, where *<PatchGUID>* is the GUID that uniquely identifies the patch.</span></span> <span data-ttu-id="cc7c3-112">La *<PatchGUID>* table MsiTransformView contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-112">The MsiTransformView *<PatchGUID>* Table has the following columns.</span></span>



| <span data-ttu-id="cc7c3-113">Colonne</span><span class="sxs-lookup"><span data-stu-id="cc7c3-113">Column</span></span>  | <span data-ttu-id="cc7c3-114">Type</span><span class="sxs-lookup"><span data-stu-id="cc7c3-114">Type</span></span>                         | <span data-ttu-id="cc7c3-115">Clé</span><span class="sxs-lookup"><span data-stu-id="cc7c3-115">Key</span></span> | <span data-ttu-id="cc7c3-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="cc7c3-116">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="cc7c3-117">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="cc7c3-117">Table</span></span>   | [<span data-ttu-id="cc7c3-118">Identificateur</span><span class="sxs-lookup"><span data-stu-id="cc7c3-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="cc7c3-119">O</span><span class="sxs-lookup"><span data-stu-id="cc7c3-119">Y</span></span>   | <span data-ttu-id="cc7c3-120">N</span><span class="sxs-lookup"><span data-stu-id="cc7c3-120">N</span></span>        |
| <span data-ttu-id="cc7c3-121">Colonne</span><span class="sxs-lookup"><span data-stu-id="cc7c3-121">Column</span></span>  | [<span data-ttu-id="cc7c3-122">Text</span><span class="sxs-lookup"><span data-stu-id="cc7c3-122">Text</span></span>](text.md)             | <span data-ttu-id="cc7c3-123">O</span><span class="sxs-lookup"><span data-stu-id="cc7c3-123">Y</span></span>   | <span data-ttu-id="cc7c3-124">N</span><span class="sxs-lookup"><span data-stu-id="cc7c3-124">N</span></span>        |
| <span data-ttu-id="cc7c3-125">Ligne</span><span class="sxs-lookup"><span data-stu-id="cc7c3-125">Row</span></span>     | [<span data-ttu-id="cc7c3-126">Text</span><span class="sxs-lookup"><span data-stu-id="cc7c3-126">Text</span></span>](text.md)             | <span data-ttu-id="cc7c3-127">O</span><span class="sxs-lookup"><span data-stu-id="cc7c3-127">Y</span></span>   | <span data-ttu-id="cc7c3-128">O</span><span class="sxs-lookup"><span data-stu-id="cc7c3-128">Y</span></span>        |
| <span data-ttu-id="cc7c3-129">Données</span><span class="sxs-lookup"><span data-stu-id="cc7c3-129">Data</span></span>    | [<span data-ttu-id="cc7c3-130">Text</span><span class="sxs-lookup"><span data-stu-id="cc7c3-130">Text</span></span>](text.md)             | <span data-ttu-id="cc7c3-131">N</span><span class="sxs-lookup"><span data-stu-id="cc7c3-131">N</span></span>   | <span data-ttu-id="cc7c3-132">O</span><span class="sxs-lookup"><span data-stu-id="cc7c3-132">Y</span></span>        |
| <span data-ttu-id="cc7c3-133">Actuel</span><span class="sxs-lookup"><span data-stu-id="cc7c3-133">Current</span></span> | [<span data-ttu-id="cc7c3-134">Text</span><span class="sxs-lookup"><span data-stu-id="cc7c3-134">Text</span></span>](text.md)             | <span data-ttu-id="cc7c3-135">N</span><span class="sxs-lookup"><span data-stu-id="cc7c3-135">N</span></span>   | <span data-ttu-id="cc7c3-136">O</span><span class="sxs-lookup"><span data-stu-id="cc7c3-136">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="cc7c3-137">Colonne</span><span class="sxs-lookup"><span data-stu-id="cc7c3-137">Column</span></span>

<dl> <dt>

<span data-ttu-id="cc7c3-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau</span><span class="sxs-lookup"><span data-stu-id="cc7c3-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="cc7c3-139">Nom d’une table de base de données modifiée.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-139">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="cc7c3-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Chronique</span><span class="sxs-lookup"><span data-stu-id="cc7c3-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="cc7c3-141">Nom d’une colonne de table modifiée ou d’une insertion, d’une suppression, d’une création ou d’une suppression.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-141">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="cc7c3-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Haut</span><span class="sxs-lookup"><span data-stu-id="cc7c3-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="cc7c3-143">Liste des valeurs de clé primaire séparées par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-143">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="cc7c3-144">Les valeurs de clé primaire NULL sont représentées par un caractère d’espace unique.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-144">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="cc7c3-145">Une valeur null dans cette colonne indique une modification de schéma.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-145">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="cc7c3-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée</span><span class="sxs-lookup"><span data-stu-id="cc7c3-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="cc7c3-147">Les données, le nom d’un flux de données ou une définition de colonne.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-147">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="cc7c3-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Actif</span><span class="sxs-lookup"><span data-stu-id="cc7c3-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="cc7c3-149">Valeur actuelle de la base de données de référence ou numéro de colonne.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-149">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc7c3-150">Notes</span><span class="sxs-lookup"><span data-stu-id="cc7c3-150">Remarks</span></span>

<span data-ttu-id="cc7c3-151">Les actions personnalisées de désinstallation des correctifs s’exécutent lorsque le correctif est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-151">Patch uninstall custom actions run when the patch is uninstalled.</span></span> <span data-ttu-id="cc7c3-152">Elles ne s’exécutent pas lorsque le produit est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-152">They do not run when the product is uninstalled.</span></span> <span data-ttu-id="cc7c3-153">Utilisez l' [option de désinstallation corrective action personnalisée](custom-action-patch-uninstall-option.md) et le tableau ci-dessous pour exécuter une opération personnalisée uniquement lorsque le correctif est en cours de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-153">Use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) and this table to run a custom only when the patch is being uninstalled.</span></span>

<span data-ttu-id="cc7c3-154">Un correctif peut mettre à jour une action personnalisée fournie dans le package d’origine (fichier. msi). Pour exécuter la version mise à jour de l’action personnalisée lorsque le correctif est désinstallé, marquez l’action personnalisée avec l’attribut **msidbCustomActionTypePatchUninstall** dans le package d’origine.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-154">A patch can update a custom action provided in the original package (.msi file.) To run the updated version of the custom action when the patch is uninstalled, mark the custom action with the **msidbCustomActionTypePatchUninstall** attribute in the original package.</span></span>

 

 



