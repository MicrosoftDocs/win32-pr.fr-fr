---
description: La table ModuleDependency conserve une liste d’autres modules de fusion requis pour que ce module de fusion fonctionne correctement.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Table ModuleDependency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524284"
---
# <a name="moduledependency-table"></a><span data-ttu-id="8ac87-103">Table ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="8ac87-103">ModuleDependency Table</span></span>

<span data-ttu-id="8ac87-104">La table ModuleDependency conserve une liste d’autres modules de fusion requis pour que ce module de fusion fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="8ac87-104">The ModuleDependency table keeps a list of other merge modules that are required for this merge module to operate properly.</span></span> <span data-ttu-id="8ac87-105">Cette table active un outil de fusion ou de vérification pour s’assurer que les modules de fusion nécessaires sont en fait inclus dans la base de données du programme d’installation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8ac87-105">This table enables a merge or verification tool to ensure that the necessary merge modules are in fact included in the user's installer database.</span></span> <span data-ttu-id="8ac87-106">L’outil vérifie en faisant référence à cette table à l’aide de la table ModuleSignature dans la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="8ac87-106">The tool checks by cross referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="8ac87-107">La table ModuleDependency contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8ac87-107">The ModuleDependency table has the following columns.</span></span>



| <span data-ttu-id="8ac87-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="8ac87-108">Column</span></span>           | <span data-ttu-id="8ac87-109">Type</span><span class="sxs-lookup"><span data-stu-id="8ac87-109">Type</span></span>                         | <span data-ttu-id="8ac87-110">Clé</span><span class="sxs-lookup"><span data-stu-id="8ac87-110">Key</span></span> | <span data-ttu-id="8ac87-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="8ac87-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="8ac87-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="8ac87-112">ModuleID</span></span>         | [<span data-ttu-id="8ac87-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="8ac87-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="8ac87-114">O</span><span class="sxs-lookup"><span data-stu-id="8ac87-114">Y</span></span>   | <span data-ttu-id="8ac87-115">N</span><span class="sxs-lookup"><span data-stu-id="8ac87-115">N</span></span>        |
| <span data-ttu-id="8ac87-116">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="8ac87-116">ModuleLanguage</span></span>   | [<span data-ttu-id="8ac87-117">Integer</span><span class="sxs-lookup"><span data-stu-id="8ac87-117">Integer</span></span>](integer.md)       | <span data-ttu-id="8ac87-118">O</span><span class="sxs-lookup"><span data-stu-id="8ac87-118">Y</span></span>   | <span data-ttu-id="8ac87-119">N</span><span class="sxs-lookup"><span data-stu-id="8ac87-119">N</span></span>        |
| <span data-ttu-id="8ac87-120">RequiredID</span><span class="sxs-lookup"><span data-stu-id="8ac87-120">RequiredID</span></span>       | [<span data-ttu-id="8ac87-121">Identificateur</span><span class="sxs-lookup"><span data-stu-id="8ac87-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="8ac87-122">O</span><span class="sxs-lookup"><span data-stu-id="8ac87-122">Y</span></span>   | <span data-ttu-id="8ac87-123">N</span><span class="sxs-lookup"><span data-stu-id="8ac87-123">N</span></span>        |
| <span data-ttu-id="8ac87-124">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="8ac87-124">RequiredLanguage</span></span> | [<span data-ttu-id="8ac87-125">Integer</span><span class="sxs-lookup"><span data-stu-id="8ac87-125">Integer</span></span>](integer.md)       | <span data-ttu-id="8ac87-126">O</span><span class="sxs-lookup"><span data-stu-id="8ac87-126">Y</span></span>   | <span data-ttu-id="8ac87-127">N</span><span class="sxs-lookup"><span data-stu-id="8ac87-127">N</span></span>        |
| <span data-ttu-id="8ac87-128">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="8ac87-128">RequiredVersion</span></span>  | [<span data-ttu-id="8ac87-129">Version</span><span class="sxs-lookup"><span data-stu-id="8ac87-129">Version</span></span>](version.md)       |     | <span data-ttu-id="8ac87-130">O</span><span class="sxs-lookup"><span data-stu-id="8ac87-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8ac87-131">Colonnes</span><span class="sxs-lookup"><span data-stu-id="8ac87-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8ac87-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="8ac87-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="8ac87-133">Identificateur du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="8ac87-133">Identifier of the merge module.</span></span> <span data-ttu-id="8ac87-134">Il s’agit d’une clé étrangère dans la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ac87-134">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ac87-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="8ac87-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="8ac87-136">ID de langue décimal du module de fusion dans ModuleID.</span><span class="sxs-lookup"><span data-stu-id="8ac87-136">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="8ac87-137">Il s’agit d’une clé étrangère dans la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ac87-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ac87-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span><span class="sxs-lookup"><span data-stu-id="8ac87-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span></span>
</dt> <dd>

<span data-ttu-id="8ac87-139">Identificateur du module de fusion requis par le module de fusion dans ModuleID.</span><span class="sxs-lookup"><span data-stu-id="8ac87-139">Identifier of the merge module required by the merge module in ModuleID.</span></span>

</dd> <dt>

<span data-ttu-id="8ac87-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="8ac87-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span></span>
</dt> <dd>

<span data-ttu-id="8ac87-141">ID de langue numérique du module de fusion dans RequiredID.</span><span class="sxs-lookup"><span data-stu-id="8ac87-141">Numeric language ID of the merge module in RequiredID.</span></span> <span data-ttu-id="8ac87-142">La colonne RequiredLanguage peut spécifier l’ID de langue pour une seule langue, par exemple 1033 pour l’anglais des États-Unis, ou spécifier l’ID de langue d’un groupe de langues, par exemple 9 pour l’anglais.</span><span class="sxs-lookup"><span data-stu-id="8ac87-142">The RequiredLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="8ac87-143">Si le champ contient un ID de langue de groupe, tout module de fusion avec un code de langue dans ce groupe est conforme à la dépendance.</span><span class="sxs-lookup"><span data-stu-id="8ac87-143">If the field contains a group language ID, any merge module with having a language code in that group satisfies the dependency.</span></span> <span data-ttu-id="8ac87-144">Si RequiredLanguage a la valeur 0, tout module de fusion remplissant les autres conditions requises est conforme à la dépendance.</span><span class="sxs-lookup"><span data-stu-id="8ac87-144">If the RequiredLanguage is set to 0, any merge module filling the other requirements satisfies the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="8ac87-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="8ac87-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span></span>
</dt> <dd>

<span data-ttu-id="8ac87-146">Version du module de fusion dans RequiredID.</span><span class="sxs-lookup"><span data-stu-id="8ac87-146">Version of the merge module in RequiredID.</span></span> <span data-ttu-id="8ac87-147">Si ce champ a la valeur null, toute version remplit la dépendance.</span><span class="sxs-lookup"><span data-stu-id="8ac87-147">If this field is Null, any version fills the dependency.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="8ac87-148">Validation</span><span class="sxs-lookup"><span data-stu-id="8ac87-148">Validation</span></span>

<dl>

[<span data-ttu-id="8ac87-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="8ac87-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8ac87-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="8ac87-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8ac87-151">ICE25</span><span class="sxs-lookup"><span data-stu-id="8ac87-151">ICE25</span></span>](ice25.md)  
</dl>

 

 



