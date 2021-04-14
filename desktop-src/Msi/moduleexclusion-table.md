---
description: La table ModuleExclusion conserve une liste d’autres modules de fusion qui sont incompatibles dans la même base de données de programme d’installation.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Table ModuleExclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393740"
---
# <a name="moduleexclusion-table"></a><span data-ttu-id="1c1fd-103">Table ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="1c1fd-103">ModuleExclusion Table</span></span>

<span data-ttu-id="1c1fd-104">La table ModuleExclusion conserve une liste d’autres modules de fusion qui sont incompatibles dans la même base de données de programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-104">The ModuleExclusion table keeps a list of other merge modules that are incompatible in the same installer database.</span></span> <span data-ttu-id="1c1fd-105">Cette table active un outil de fusion ou de vérification pour vérifier que les modules de fusion en conflit ne sont pas fusionnés dans la base de données du programme d’installation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-105">This table enables a merge or verification tool to check that conflicting merge modules are not merged in the user's installer database.</span></span> <span data-ttu-id="1c1fd-106">L’outil vérifie en faisant référence croisée à cette table avec la table ModuleSignature dans la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-106">The tool checks by cross-referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="1c1fd-107">La table ModuleExclusion contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-107">The ModuleExclusion table has the following columns.</span></span>



| <span data-ttu-id="1c1fd-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="1c1fd-108">Column</span></span>             | <span data-ttu-id="1c1fd-109">Type</span><span class="sxs-lookup"><span data-stu-id="1c1fd-109">Type</span></span>                         | <span data-ttu-id="1c1fd-110">Clé</span><span class="sxs-lookup"><span data-stu-id="1c1fd-110">Key</span></span> | <span data-ttu-id="1c1fd-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="1c1fd-111">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="1c1fd-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="1c1fd-112">ModuleID</span></span>           | [<span data-ttu-id="1c1fd-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="1c1fd-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="1c1fd-114">O</span><span class="sxs-lookup"><span data-stu-id="1c1fd-114">Y</span></span>   | <span data-ttu-id="1c1fd-115">N</span><span class="sxs-lookup"><span data-stu-id="1c1fd-115">N</span></span>        |
| <span data-ttu-id="1c1fd-116">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="1c1fd-116">ModuleLanguage</span></span>     | [<span data-ttu-id="1c1fd-117">Integer</span><span class="sxs-lookup"><span data-stu-id="1c1fd-117">Integer</span></span>](integer.md)       | <span data-ttu-id="1c1fd-118">O</span><span class="sxs-lookup"><span data-stu-id="1c1fd-118">Y</span></span>   | <span data-ttu-id="1c1fd-119">N</span><span class="sxs-lookup"><span data-stu-id="1c1fd-119">N</span></span>        |
| <span data-ttu-id="1c1fd-120">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="1c1fd-120">ExcludedID</span></span>         | [<span data-ttu-id="1c1fd-121">Identificateur</span><span class="sxs-lookup"><span data-stu-id="1c1fd-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="1c1fd-122">O</span><span class="sxs-lookup"><span data-stu-id="1c1fd-122">Y</span></span>   | <span data-ttu-id="1c1fd-123">N</span><span class="sxs-lookup"><span data-stu-id="1c1fd-123">N</span></span>        |
| <span data-ttu-id="1c1fd-124">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="1c1fd-124">ExcludedLanguage</span></span>   | [<span data-ttu-id="1c1fd-125">Integer</span><span class="sxs-lookup"><span data-stu-id="1c1fd-125">Integer</span></span>](integer.md)       | <span data-ttu-id="1c1fd-126">O</span><span class="sxs-lookup"><span data-stu-id="1c1fd-126">Y</span></span>   | <span data-ttu-id="1c1fd-127">N</span><span class="sxs-lookup"><span data-stu-id="1c1fd-127">N</span></span>        |
| <span data-ttu-id="1c1fd-128">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="1c1fd-128">ExcludedMinVersion</span></span> | [<span data-ttu-id="1c1fd-129">Version</span><span class="sxs-lookup"><span data-stu-id="1c1fd-129">Version</span></span>](version.md)       |     | <span data-ttu-id="1c1fd-130">O</span><span class="sxs-lookup"><span data-stu-id="1c1fd-130">Y</span></span>        |
| <span data-ttu-id="1c1fd-131">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="1c1fd-131">ExcludedMaxVersion</span></span> | [<span data-ttu-id="1c1fd-132">Version</span><span class="sxs-lookup"><span data-stu-id="1c1fd-132">Version</span></span>](version.md)       |     | <span data-ttu-id="1c1fd-133">O</span><span class="sxs-lookup"><span data-stu-id="1c1fd-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1c1fd-134">Colonnes</span><span class="sxs-lookup"><span data-stu-id="1c1fd-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1c1fd-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="1c1fd-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="1c1fd-136">Identificateur du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-136">Identifier of the merge module.</span></span> <span data-ttu-id="1c1fd-137">Il s’agit d’une clé étrangère dans la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="1c1fd-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c1fd-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="1c1fd-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="1c1fd-139">ID de langue décimal du module de fusion dans ModuleID.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-139">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="1c1fd-140">Il s’agit d’une clé étrangère dans la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="1c1fd-140">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c1fd-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span><span class="sxs-lookup"><span data-stu-id="1c1fd-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span></span>
</dt> <dd>

<span data-ttu-id="1c1fd-142">Identificateur d’un module de fusion exclu.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-142">Identifier of an excluded merge module.</span></span>

</dd> <dt>

<span data-ttu-id="1c1fd-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="1c1fd-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span></span>
</dt> <dd>

<span data-ttu-id="1c1fd-144">ID de langue numérique du module de fusion dans ExcludedID.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-144">Numeric language ID of the merge module in ExcludedID.</span></span> <span data-ttu-id="1c1fd-145">La colonne ExcludedLanguage peut spécifier l’ID de langue pour une seule langue, par exemple 1033 pour l’anglais des États-Unis, ou spécifier l’ID de langue d’un groupe de langues, par exemple 9 pour l’anglais.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-145">The ExcludedLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="1c1fd-146">La colonne ExcludedLanguage peut accepter des ID de langue négatifs.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-146">The ExcludedLanguage column can accept negative language IDs.</span></span> <span data-ttu-id="1c1fd-147">La signification de la valeur dans la colonne ExcludedLanguage est la suivante.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-147">The meaning of the value in the ExcludedLanguage column is as follows.</span></span>



| <span data-ttu-id="1c1fd-148">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="1c1fd-148">ExcludedLanguage</span></span> | <span data-ttu-id="1c1fd-149">Signification</span><span class="sxs-lookup"><span data-stu-id="1c1fd-149">Meaning</span></span>                                                              |
|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="1c1fd-150">> 0</span><span class="sxs-lookup"><span data-stu-id="1c1fd-150">> 0</span></span>           | <span data-ttu-id="1c1fd-151">Excluez les ID de langue spécifiés par ExcludedLanguage.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-151">Exclude the language IDs specified by ExcludedLanguage.</span></span>              |
| <span data-ttu-id="1c1fd-152">= 0</span><span class="sxs-lookup"><span data-stu-id="1c1fd-152">= 0</span></span>              | <span data-ttu-id="1c1fd-153">Exclut aucun ID de langue.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-153">Exclude no language IDs.</span></span>                                             |
| <span data-ttu-id="1c1fd-154">< 0</span><span class="sxs-lookup"><span data-stu-id="1c1fd-154">< 0</span></span>           | <span data-ttu-id="1c1fd-155">Excluez tous les ID de langue, à l’exception de ceux spécifiés par ExcludedLanguage.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-155">Exclude all language IDs except those specified by ExcludedLanguage.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1c1fd-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="1c1fd-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span></span>
</dt> <dd>

<span data-ttu-id="1c1fd-157">Version minimale exclue d’une plage.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-157">Minimum version excluded from a range.</span></span> <span data-ttu-id="1c1fd-158">Si le champ ExcludedMinVersion a la valeur null, toutes les versions antérieures à ExcludedMaxVersion sont exclues.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-158">If the ExcludedMinVersion field is Null, all versions before ExcludedMaxVersion are excluded.</span></span> <span data-ttu-id="1c1fd-159">Si ExcludedMinVersion et ExcludedMaxVersion ont tous les deux la valeur null, il n’existe aucune exclusion basée sur la version.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-159">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> <dt>

<span data-ttu-id="1c1fd-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="1c1fd-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="1c1fd-161">Version maximale exclue d’une plage.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-161">Maximum version excluded from a range.</span></span> <span data-ttu-id="1c1fd-162">Si le champ ExcludedMaxVersion a la valeur null, toutes les versions après ExcludedMinVersion sont exclues.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-162">If the ExcludedMaxVersion field is Null, all versions after ExcludedMinVersion are excluded.</span></span> <span data-ttu-id="1c1fd-163">Si ExcludedMinVersion et ExcludedMaxVersion ont tous les deux la valeur null, il n’existe aucune exclusion basée sur la version.</span><span class="sxs-lookup"><span data-stu-id="1c1fd-163">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="1c1fd-164">Validation</span><span class="sxs-lookup"><span data-stu-id="1c1fd-164">Validation</span></span>

<dl>

[<span data-ttu-id="1c1fd-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="1c1fd-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1c1fd-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="1c1fd-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1c1fd-167">ICE25</span><span class="sxs-lookup"><span data-stu-id="1c1fd-167">ICE25</span></span>](ice25.md)  
</dl>

 

 



