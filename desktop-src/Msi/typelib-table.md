---
description: La table TypeLib contient les informations qui doivent être placées dans l’enregistrement du registre des bibliothèques de types.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: Table TypeLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0aa8949df75162ffb7107b633ab766d276c4b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514773"
---
# <a name="typelib-table"></a><span data-ttu-id="15d0f-103">Table TypeLib</span><span class="sxs-lookup"><span data-stu-id="15d0f-103">TypeLib Table</span></span>

<span data-ttu-id="15d0f-104">La table TypeLib contient les informations qui doivent être placées dans l’enregistrement du registre des bibliothèques de types.</span><span class="sxs-lookup"><span data-stu-id="15d0f-104">The TypeLib table contains the information that needs to be placed in the registry registration of type libraries.</span></span>

<span data-ttu-id="15d0f-105">La table TypeLib contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="15d0f-105">The TypeLib table has the following columns.</span></span>



| <span data-ttu-id="15d0f-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="15d0f-106">Column</span></span>      | <span data-ttu-id="15d0f-107">Type</span><span class="sxs-lookup"><span data-stu-id="15d0f-107">Type</span></span>                               | <span data-ttu-id="15d0f-108">Clé</span><span class="sxs-lookup"><span data-stu-id="15d0f-108">Key</span></span> | <span data-ttu-id="15d0f-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="15d0f-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="15d0f-110">LibID</span><span class="sxs-lookup"><span data-stu-id="15d0f-110">LibID</span></span>       | [<span data-ttu-id="15d0f-111">GUID</span><span class="sxs-lookup"><span data-stu-id="15d0f-111">GUID</span></span>](guid.md)                   | <span data-ttu-id="15d0f-112">O</span><span class="sxs-lookup"><span data-stu-id="15d0f-112">Y</span></span>   | <span data-ttu-id="15d0f-113">N</span><span class="sxs-lookup"><span data-stu-id="15d0f-113">N</span></span>        |
| <span data-ttu-id="15d0f-114">Language</span><span class="sxs-lookup"><span data-stu-id="15d0f-114">Language</span></span>    | [<span data-ttu-id="15d0f-115">Integer</span><span class="sxs-lookup"><span data-stu-id="15d0f-115">Integer</span></span>](integer.md)             | <span data-ttu-id="15d0f-116">O</span><span class="sxs-lookup"><span data-stu-id="15d0f-116">Y</span></span>   | <span data-ttu-id="15d0f-117">N</span><span class="sxs-lookup"><span data-stu-id="15d0f-117">N</span></span>        |
| <span data-ttu-id="15d0f-118">-\_</span><span class="sxs-lookup"><span data-stu-id="15d0f-118">Component\_</span></span> | [<span data-ttu-id="15d0f-119">Identificateur</span><span class="sxs-lookup"><span data-stu-id="15d0f-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="15d0f-120">O</span><span class="sxs-lookup"><span data-stu-id="15d0f-120">Y</span></span>   | <span data-ttu-id="15d0f-121">N</span><span class="sxs-lookup"><span data-stu-id="15d0f-121">N</span></span>        |
| <span data-ttu-id="15d0f-122">Version</span><span class="sxs-lookup"><span data-stu-id="15d0f-122">Version</span></span>     | [<span data-ttu-id="15d0f-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="15d0f-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="15d0f-124">N</span><span class="sxs-lookup"><span data-stu-id="15d0f-124">N</span></span>   | <span data-ttu-id="15d0f-125">O</span><span class="sxs-lookup"><span data-stu-id="15d0f-125">Y</span></span>        |
| <span data-ttu-id="15d0f-126">Description</span><span class="sxs-lookup"><span data-stu-id="15d0f-126">Description</span></span> | [<span data-ttu-id="15d0f-127">Text</span><span class="sxs-lookup"><span data-stu-id="15d0f-127">Text</span></span>](text.md)                   | <span data-ttu-id="15d0f-128">N</span><span class="sxs-lookup"><span data-stu-id="15d0f-128">N</span></span>   | <span data-ttu-id="15d0f-129">O</span><span class="sxs-lookup"><span data-stu-id="15d0f-129">Y</span></span>        |
| <span data-ttu-id="15d0f-130">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="15d0f-130">Directory\_</span></span> | [<span data-ttu-id="15d0f-131">Identificateur</span><span class="sxs-lookup"><span data-stu-id="15d0f-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="15d0f-132">N</span><span class="sxs-lookup"><span data-stu-id="15d0f-132">N</span></span>   | <span data-ttu-id="15d0f-133">O</span><span class="sxs-lookup"><span data-stu-id="15d0f-133">Y</span></span>        |
| <span data-ttu-id="15d0f-134">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="15d0f-134">Feature\_</span></span>   | [<span data-ttu-id="15d0f-135">Identificateur</span><span class="sxs-lookup"><span data-stu-id="15d0f-135">Identifier</span></span>](identifier.md)       | <span data-ttu-id="15d0f-136">N</span><span class="sxs-lookup"><span data-stu-id="15d0f-136">N</span></span>   | <span data-ttu-id="15d0f-137">N</span><span class="sxs-lookup"><span data-stu-id="15d0f-137">N</span></span>        |
| <span data-ttu-id="15d0f-138">Coût</span><span class="sxs-lookup"><span data-stu-id="15d0f-138">Cost</span></span>        | [<span data-ttu-id="15d0f-139">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="15d0f-139">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="15d0f-140">N</span><span class="sxs-lookup"><span data-stu-id="15d0f-140">N</span></span>   | <span data-ttu-id="15d0f-141">O</span><span class="sxs-lookup"><span data-stu-id="15d0f-141">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="15d0f-142">Colonnes</span><span class="sxs-lookup"><span data-stu-id="15d0f-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="15d0f-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span><span class="sxs-lookup"><span data-stu-id="15d0f-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span></span>
</dt> <dd>

<span data-ttu-id="15d0f-144">GUID qui identifie la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="15d0f-144">The GUID that identifies the library.</span></span>

</dd> <dt>

<span data-ttu-id="15d0f-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sous</span><span class="sxs-lookup"><span data-stu-id="15d0f-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="15d0f-146">Langage de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="15d0f-146">The language of the type library.</span></span> <span data-ttu-id="15d0f-147">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="15d0f-147">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="15d0f-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="15d0f-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="15d0f-149">Clé externe dans la première colonne de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="15d0f-149">External key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="15d0f-150">Cette colonne identifie le composant appartenant à \_ la fonctionnalité dont le fichier de clé est la bibliothèque de types en cours d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="15d0f-150">This column identifies the component belonging to Feature\_ whose key file is the type library being registered.</span></span>

</dd> <dt>

<span data-ttu-id="15d0f-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span><span class="sxs-lookup"><span data-stu-id="15d0f-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="15d0f-152">Il s’agit de la version de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="15d0f-152">This is the version of the library.</span></span> <span data-ttu-id="15d0f-153">Les versions majeure et mineure sont encodées dans la valeur entière de quatre octets.</span><span class="sxs-lookup"><span data-stu-id="15d0f-153">The major and minor versions are encoded in the four byte integer value.</span></span> <span data-ttu-id="15d0f-154">La version mineure est dans les huit bits inférieurs.</span><span class="sxs-lookup"><span data-stu-id="15d0f-154">The minor version is in the lower eight bits.</span></span> <span data-ttu-id="15d0f-155">La version principale est au milieu de seize bits.</span><span class="sxs-lookup"><span data-stu-id="15d0f-155">The major version is in the middle sixteen bits.</span></span>

</dd> <dt>

<span data-ttu-id="15d0f-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="15d0f-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="15d0f-157">Description localisable de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="15d0f-157">A localizable description of the library.</span></span>

</dd> <dt>

<span data-ttu-id="15d0f-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span><span class="sxs-lookup"><span data-stu-id="15d0f-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="15d0f-159">Clé externe dans la première colonne de la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="15d0f-159">External key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="15d0f-160">Cette colonne identifie le chemin d’accès de l’aide pour la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="15d0f-160">This column identifies the Help path for the type library.</span></span> <span data-ttu-id="15d0f-161">Cette colonne est ignorée lors de la publicité.</span><span class="sxs-lookup"><span data-stu-id="15d0f-161">This column is ignored during advertising.</span></span>

</dd> <dt>

<span data-ttu-id="15d0f-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="15d0f-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="15d0f-163">Clé externe dans la première colonne du [tableau des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="15d0f-163">External key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="15d0f-164">Cette colonne spécifie la fonctionnalité qui doit être installée pour que la bibliothèque de types soit opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="15d0f-164">This column specifies the feature that must be installed for the type library to be operational.</span></span>

</dd> <dt>

<span data-ttu-id="15d0f-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Coûts</span><span class="sxs-lookup"><span data-stu-id="15d0f-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="15d0f-166">Coût associé à l’inscription de la bibliothèque de types en octets.</span><span class="sxs-lookup"><span data-stu-id="15d0f-166">The cost associated with the registration of the type library in bytes.</span></span> <span data-ttu-id="15d0f-167">Il doit s’agir d’un nombre non négatif ou d’une valeur null.</span><span class="sxs-lookup"><span data-stu-id="15d0f-167">This must be a non-negative number or null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15d0f-168">Notes</span><span class="sxs-lookup"><span data-stu-id="15d0f-168">Remarks</span></span>

<span data-ttu-id="15d0f-169">Cette table est référencée lorsque l' [action RegisterTypeLibraries](registertypelibraries-action.md) ou l' [action UnregisterTypeLibraries](unregistertypelibraries-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="15d0f-169">This table is referred to when the [RegisterTypeLibraries action](registertypelibraries-action.md) or the [UnregisterTypeLibraries action](unregistertypelibraries-action.md) is executed.</span></span>

<span data-ttu-id="15d0f-170">Le programme d’installation écrit toutes les informations d’inscription de la bibliothèque de types dans l' \_ emplacement de Registre HKEY local \_ machine (HKLM).</span><span class="sxs-lookup"><span data-stu-id="15d0f-170">The installer writes all type library registration information into the HKEY\_LOCAL\_MACHINE (HKLM) registry location.</span></span> <span data-ttu-id="15d0f-171">C’est le cas même pour les installations par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="15d0f-171">This is the case even for per-user installations.</span></span> <span data-ttu-id="15d0f-172">Les bibliothèques de types ne peuvent pas être inscrites dans des emplacements par utilisateur (HKCU).</span><span class="sxs-lookup"><span data-stu-id="15d0f-172">Type libraries cannot be registered in per-user locations (HKCU).</span></span>

<span data-ttu-id="15d0f-173">Les auteurs de packages d’installation sont fortement recommandés par rapport à l’utilisation de la table TypeLib.</span><span class="sxs-lookup"><span data-stu-id="15d0f-173">Installation package authors are strongly advised against using the TypeLib table.</span></span> <span data-ttu-id="15d0f-174">Au lieu de cela, ils doivent inscrire les bibliothèques de types à l’aide de la table [du Registre](registry-table.md) .</span><span class="sxs-lookup"><span data-stu-id="15d0f-174">Instead, they should register type libraries by using the [Registry](registry-table.md) table.</span></span> <span data-ttu-id="15d0f-175">Voici quelques raisons pour lesquelles éviter l’inscription automatique :</span><span class="sxs-lookup"><span data-stu-id="15d0f-175">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="15d0f-176">Si une installation qui utilise la table TypeLib échoue et doit être restaurée, la restauration peut ne pas restaurer l’état de l’ordinateur qui existait avant la restauration.</span><span class="sxs-lookup"><span data-stu-id="15d0f-176">If an installation using the TypeLib table fails and must be rolled back, the rollback may not restore the computer to the same state that existed prior to the rollback.</span></span> <span data-ttu-id="15d0f-177">Les bibliothèques de types inscrites avant la restauration ne peuvent pas être inscrites après la restauration.</span><span class="sxs-lookup"><span data-stu-id="15d0f-177">Type libraries registered prior to rollback may not be registered after rollback.</span></span>

## <a name="validation"></a><span data-ttu-id="15d0f-178">Validation</span><span class="sxs-lookup"><span data-stu-id="15d0f-178">Validation</span></span>

<dl>

[<span data-ttu-id="15d0f-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="15d0f-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="15d0f-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="15d0f-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="15d0f-181">ICE19</span><span class="sxs-lookup"><span data-stu-id="15d0f-181">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="15d0f-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="15d0f-182">ICE32</span></span>](ice32.md)  
</dl>

 

 



