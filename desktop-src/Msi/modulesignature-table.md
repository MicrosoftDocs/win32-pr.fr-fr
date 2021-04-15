---
description: La table ModuleSignature est une table obligatoire.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: ModuleSignature, table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529242"
---
# <a name="modulesignature-table"></a><span data-ttu-id="71ab7-103">ModuleSignature, table</span><span class="sxs-lookup"><span data-stu-id="71ab7-103">ModuleSignature Table</span></span>

<span data-ttu-id="71ab7-104">La table ModuleSignature est une table obligatoire.</span><span class="sxs-lookup"><span data-stu-id="71ab7-104">The ModuleSignature Table is a required table.</span></span> <span data-ttu-id="71ab7-105">Il contient toutes les informations nécessaires pour identifier un module de fusion.</span><span class="sxs-lookup"><span data-stu-id="71ab7-105">It contains all the information necessary to identify a merge module.</span></span> <span data-ttu-id="71ab7-106">L’outil de fusion ajoute cette table au fichier. msi s’il n’en existe pas déjà une.</span><span class="sxs-lookup"><span data-stu-id="71ab7-106">The merge tool adds this table to the .msi file if one does not already exist.</span></span> <span data-ttu-id="71ab7-107">La table ModuleSignature d’un module de fusion n’a qu’une seule ligne contenant le ModuleID, la langue et la version.</span><span class="sxs-lookup"><span data-stu-id="71ab7-107">The ModuleSignature table in a merge module has only one row containing the ModuleID, Language, and Version.</span></span> <span data-ttu-id="71ab7-108">Toutefois, la table ModuleSignature d’un fichier. msi contient une ligne contenant ces informations pour chaque fichier. msm qui a été fusionné dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="71ab7-108">However, the ModuleSignature table in an .msi file has a row containing this information for each .msm file that has been merged into it.</span></span>

<span data-ttu-id="71ab7-109">Les outils de fusion et de vérification vérifient la table ModuleSignature dans les fichiers. msi pour déterminer si elle contient tous les modules de fusion dépendants requis par le module de fusion actuel (consultez la [table ModuleDependency](moduledependency-table.md)) et si le package d’installation a été précédemment fusionné avec des modules de fusion en conflit (voir la [table ModuleExclusion](moduleexclusion-table.md)).</span><span class="sxs-lookup"><span data-stu-id="71ab7-109">Merge and verification tools check the ModuleSignature table in .msi files to determine if it has all of the dependent merge modules required by the current merge module (see [ModuleDependency Table](moduledependency-table.md)) and whether the installation package was previously merged with any conflicting merge modules (see [ModuleExclusion Table](moduleexclusion-table.md)).</span></span>

<span data-ttu-id="71ab7-110">La table ModuleSignature contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="71ab7-110">The ModuleSignature table has the following columns.</span></span>



| <span data-ttu-id="71ab7-111">Colonne</span><span class="sxs-lookup"><span data-stu-id="71ab7-111">Column</span></span>   | <span data-ttu-id="71ab7-112">Type</span><span class="sxs-lookup"><span data-stu-id="71ab7-112">Type</span></span>                         | <span data-ttu-id="71ab7-113">Clé</span><span class="sxs-lookup"><span data-stu-id="71ab7-113">Key</span></span> | <span data-ttu-id="71ab7-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="71ab7-114">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="71ab7-115">ModuleID</span><span class="sxs-lookup"><span data-stu-id="71ab7-115">ModuleID</span></span> | [<span data-ttu-id="71ab7-116">Identificateur</span><span class="sxs-lookup"><span data-stu-id="71ab7-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="71ab7-117">O</span><span class="sxs-lookup"><span data-stu-id="71ab7-117">Y</span></span>   | <span data-ttu-id="71ab7-118">N</span><span class="sxs-lookup"><span data-stu-id="71ab7-118">N</span></span>        |
| <span data-ttu-id="71ab7-119">Language</span><span class="sxs-lookup"><span data-stu-id="71ab7-119">Language</span></span> | [<span data-ttu-id="71ab7-120">Integer</span><span class="sxs-lookup"><span data-stu-id="71ab7-120">Integer</span></span>](integer.md)       | <span data-ttu-id="71ab7-121">O</span><span class="sxs-lookup"><span data-stu-id="71ab7-121">Y</span></span>   | <span data-ttu-id="71ab7-122">N</span><span class="sxs-lookup"><span data-stu-id="71ab7-122">N</span></span>        |
| <span data-ttu-id="71ab7-123">Version</span><span class="sxs-lookup"><span data-stu-id="71ab7-123">Version</span></span>  | [<span data-ttu-id="71ab7-124">Version</span><span class="sxs-lookup"><span data-stu-id="71ab7-124">Version</span></span>](version.md)       |     | <span data-ttu-id="71ab7-125">N</span><span class="sxs-lookup"><span data-stu-id="71ab7-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="71ab7-126">Colonnes</span><span class="sxs-lookup"><span data-stu-id="71ab7-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="71ab7-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="71ab7-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="71ab7-128">Identificateur qui identifie de façon unique le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="71ab7-128">An identifier that uniquely identifies the merge module.</span></span> <span data-ttu-id="71ab7-129">Deux modules de fusion ne peuvent pas avoir le même ModuleID, à moins que le module de fusion n’ait entièrement une compatibilité descendante avec son prédécesseur.</span><span class="sxs-lookup"><span data-stu-id="71ab7-129">Two merge modules cannot have the same ModuleID unless the merge module is entirely backward compatible with its predecessor.</span></span> <span data-ttu-id="71ab7-130">Vous pouvez créer un GUID pour ce champ à l’aide d’un utilitaire tel que GUIDGEN.</span><span class="sxs-lookup"><span data-stu-id="71ab7-130">You can create a GUID for this field using a utility such as GUIDGEN.</span></span> <span data-ttu-id="71ab7-131">La colonne ModuleID est une clé primaire pour la table et doit donc respecter la Convention d’affectation de noms pour [nommer les clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="71ab7-131">The ModuleID column is a primary key for the table and therefore it must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="71ab7-132">Par exemple, si le nom lisible du module de fusion est MyLibrary et que le GUID est {880DE2F0-CDD8-11D1-A849-006097ABDE17}, l’entrée dans la colonne ModuleID devient MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.</span><span class="sxs-lookup"><span data-stu-id="71ab7-132">For example, if the readable name of the merge module is MyLibrary and the GUID is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

</dd> <dt>

<span data-ttu-id="71ab7-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sous</span><span class="sxs-lookup"><span data-stu-id="71ab7-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="71ab7-134">L’identificateur de langue spécifie la langue par défaut pour le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="71ab7-134">The Language identifier specifies the default language for the merge module.</span></span> <span data-ttu-id="71ab7-135">L’identificateur de langue est au format décimal, par exemple, l’anglais des États-Unis est 1033.</span><span class="sxs-lookup"><span data-stu-id="71ab7-135">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="71ab7-136">Le langage utilisé par le module de fusion peut être modifié en appliquant une transformation au module de fusion avant la fusion.</span><span class="sxs-lookup"><span data-stu-id="71ab7-136">The language used by the merge module can be changed by applying a transform to the merge module before merging.</span></span>

</dd> <dt>

<span data-ttu-id="71ab7-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span><span class="sxs-lookup"><span data-stu-id="71ab7-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="71ab7-138">Le champ version contient une chaîne qui décrit les versions majeures et mineures du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="71ab7-138">The Version field contains a string that describes the major and minor versions of the merge module.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="71ab7-139">Validation</span><span class="sxs-lookup"><span data-stu-id="71ab7-139">Validation</span></span>

<dl>

[<span data-ttu-id="71ab7-140">ICE03</span><span class="sxs-lookup"><span data-stu-id="71ab7-140">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="71ab7-141">ICE06</span><span class="sxs-lookup"><span data-stu-id="71ab7-141">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="71ab7-142">ICE25</span><span class="sxs-lookup"><span data-stu-id="71ab7-142">ICE25</span></span>](ice25.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="71ab7-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71ab7-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71ab7-144">Modules de fusion multilingues</span><span class="sxs-lookup"><span data-stu-id="71ab7-144">Multiple Language Merge Modules</span></span>](multiple-language-merge-modules.md)
</dt> </dl>

 

 



