---
description: La procédure suivante décrit les étapes générales pour créer des modules de fusion.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Création de modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202549"
---
# <a name="authoring-merge-modules"></a><span data-ttu-id="2ea41-103">Création de modules de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-103">Authoring Merge Modules</span></span>

<span data-ttu-id="2ea41-104">La procédure suivante décrit les étapes générales pour créer des modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="2ea41-104">The following procedure describes the general steps to authoring merge modules.</span></span>

<span data-ttu-id="2ea41-105">**Pour créer un module de fusion**</span><span class="sxs-lookup"><span data-stu-id="2ea41-105">**To create a new merge module**</span></span>

1.  <span data-ttu-id="2ea41-106">Procurez-vous un outil logiciel que vous pouvez utiliser pour modifier la base de données des modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="2ea41-106">Obtain a software tool you can use to edit the merge module database.</span></span>
2.  <span data-ttu-id="2ea41-107">Obtenez une base de données de module de fusion vide.</span><span class="sxs-lookup"><span data-stu-id="2ea41-107">Obtain a blank merge module database.</span></span>
3.  <span data-ttu-id="2ea41-108">Générez un [GUID](guid.md) pour le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2ea41-108">Generate a [GUID](guid.md) for the merge module.</span></span> <span data-ttu-id="2ea41-109">Vous devez utiliser ce GUID lors de la création des clés primaires des tables de base de données dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2ea41-109">You need to use this GUID when authoring the primary keys of database tables in the merge module.</span></span>
4.  <span data-ttu-id="2ea41-110">Ajoutez un enregistrement à la [table des composants](component-table.md) pour chaque composant remis par la fusion.</span><span class="sxs-lookup"><span data-stu-id="2ea41-110">Add a record to the [Component table](component-table.md) for each component delivered by the merge.</span></span> <span data-ttu-id="2ea41-111">Une table de composants est requise dans chaque module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2ea41-111">A Component table is required in every merge module.</span></span> <span data-ttu-id="2ea41-112">Notez que les modules de fusion fonctionnent avec les composants et non avec les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="2ea41-112">Note that merge modules operate with components and not with features.</span></span> <span data-ttu-id="2ea41-113">Dans certains cas, toutefois, une entrée de table de base de données peut être amenée à référencer une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2ea41-113">In certain cases, however, a database table entry may need to reference a feature.</span></span> <span data-ttu-id="2ea41-114">Pour plus d’informations, consultez [référencement des fonctionnalités dans les modules de fusion](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="2ea41-114">For details, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>
5.  <span data-ttu-id="2ea41-115">Ajoutez une [table de répertoires](directory-table.md) au module de fusion qui spécifie la disposition des répertoires que le module de fusion ajoute à la base de données cible.</span><span class="sxs-lookup"><span data-stu-id="2ea41-115">Add a [Directory table](directory-table.md) to the merge module that specifies the layout of directories the merge module adds to the target database.</span></span> <span data-ttu-id="2ea41-116">Une table de répertoire est requise dans chaque module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2ea41-116">A Directory table is required in every merge module.</span></span>
6.  <span data-ttu-id="2ea41-117">Importez une [table FeatureComponents](featurecomponents-table.md) vide dans la base de données des modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="2ea41-117">Import a blank [FeatureComponents table](featurecomponents-table.md) into the merge module database.</span></span> <span data-ttu-id="2ea41-118">Cette table vide fournit une indication pour l’outil de fusion dans les cas où le fichier. msi ne contient pas sa propre table FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="2ea41-118">This empty table provides a guideline for the merge tool in cases where the .msi file does not contain its own FeatureComponents table.</span></span>
7.  <span data-ttu-id="2ea41-119">Collectez tous les fichiers remis par ce module de fusion et créez le fichier CAB [MergeModule.CABinet](mergemodule-cabinet.md) .</span><span class="sxs-lookup"><span data-stu-id="2ea41-119">Collect all the files delivered by this merge module and create the [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file.</span></span> <span data-ttu-id="2ea41-120">Ajoutez le fichier CAB au module de fusion sous la forme d’un flux à l’intérieur du fichier. msm.</span><span class="sxs-lookup"><span data-stu-id="2ea41-120">Add the cabinet to the merge module as a stream inside the .msm file.</span></span>
8.  <span data-ttu-id="2ea41-121">Ajoutez un enregistrement à la table de fichiers pour chaque fichier stocké dans MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="2ea41-121">Add a record to the File table for every file stored in MergeModule.CABinet.</span></span>
9.  <span data-ttu-id="2ea41-122">Ajoutez les informations nécessaires pour identifier le module de fusion dans la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ea41-122">Add the information necessary to identify the merge module in the [ModuleSignature table](modulesignature-table.md).</span></span> <span data-ttu-id="2ea41-123">Chaque module de fusion requiert une table ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="2ea41-123">Every merge module requires a ModuleSignature table.</span></span>
10. <span data-ttu-id="2ea41-124">Répertoriez les composants du module de fusion dans la [table ModuleComponents](modulecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ea41-124">List the components in the merge module in the [ModuleComponents table](modulecomponents-table.md).</span></span> <span data-ttu-id="2ea41-125">Chaque module de fusion requiert une table ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="2ea41-125">Every merge module requires a ModuleComponents table.</span></span>
11. <span data-ttu-id="2ea41-126">Ajoutez des tables de séquence de module de fusion au fichier. msm uniquement si le module de fusion doit modifier les [*tables de séquence*](s-gly.md) de la base de données d’installation cible.</span><span class="sxs-lookup"><span data-stu-id="2ea41-126">Add merge module sequence tables to the .msm file only if the merge module needs to modify the [*sequence tables*](s-gly.md) of the target installation database.</span></span>
12. <span data-ttu-id="2ea41-127">Ajoutez une \_ table de validation au module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2ea41-127">Add a \_Validation table to the merge module.</span></span> <span data-ttu-id="2ea41-128">Un module de fusion requiert une \_ table de validation pour réussir la validation.</span><span class="sxs-lookup"><span data-stu-id="2ea41-128">A merge module requires a \_Validation table to pass validation.</span></span>
13. <span data-ttu-id="2ea41-129">Les modules de fusion ne requièrent qu’une interface utilisateur dans de rares cas.</span><span class="sxs-lookup"><span data-stu-id="2ea41-129">Merge modules require a user interface in only rare cases.</span></span> <span data-ttu-id="2ea41-130">L’inclusion d’une interface utilisateur avec un module de fusion n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="2ea41-130">Including a UI with a merge module is not recommended.</span></span> <span data-ttu-id="2ea41-131">Dans les cas où une interface utilisateur est requise, les tables de l’interface utilisateur peuvent être fusionnées dans le fichier. msi de la même façon que les autres tables.</span><span class="sxs-lookup"><span data-stu-id="2ea41-131">In cases where a user interface is required, the UI tables can be merged into the .msi file the same as other tables.</span></span>
14. <span data-ttu-id="2ea41-132">Ajoutez des informations de Registre aux tables de Registre appropriées dans la base de données des modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="2ea41-132">Add registry information to the appropriate registry tables in the merge module database.</span></span> <span data-ttu-id="2ea41-133">Ajoutez des informations de Registre pour les bibliothèques de types, les classes, les extensions et les verbes dans les tables [TypeLib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [extension](extension-table.md), [verb](verb-table.md)ou [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2ea41-133">Add registry information for type libraries, classes, extensions, and verbs into the [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="2ea41-134">Toutes les autres informations de Registre peuvent être placées dans la [table du Registre](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ea41-134">All other registry information can go into the [Registry table](registry-table.md).</span></span> <span data-ttu-id="2ea41-135">L’utilisation de la table SelfReg n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="2ea41-135">The use of the SelfReg table is not recommended.</span></span>
15. <span data-ttu-id="2ea41-136">Ajoutez les informations de résumé au [flux de données Résumé du module de fusion](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2ea41-136">Add the summary information to the [Merge Module Summary Information Stream](merge-module-summary-information-stream-reference.md).</span></span>
16. <span data-ttu-id="2ea41-137">Exécutez la validation sur tous les modules de fusion avant d’effectuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="2ea41-137">Run validation on all merge modules before attempting to install.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ea41-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ea41-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ea41-139">Obtention de bases de données de module de fusion vides</span><span class="sxs-lookup"><span data-stu-id="2ea41-139">Obtaining Blank Merge Module Databases</span></span>](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="2ea41-140">Obtention d’outils de création de module de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-140">Obtaining Merge Module Authoring Tools</span></span>](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[<span data-ttu-id="2ea41-141">Attribution d’un nom aux clés primaires dans les bases de données de module de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-141">Naming Primary Keys in Merge Module Databases</span></span>](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="2ea41-142">Création de tables de composants de module de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-142">Authoring Merge Module Component Tables</span></span>](authoring-merge-module-component-tables.md)
</dt> <dt>

[<span data-ttu-id="2ea41-143">Création de tables de répertoires de module de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-143">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="2ea41-144">Création de tables FeatureComponents du module de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-144">Authoring Merge Module FeatureComponents Tables</span></span>](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="2ea41-145">Génération de fichiers CAB inet MergeModule.CAB</span><span class="sxs-lookup"><span data-stu-id="2ea41-145">Generating MergeModule.CABinet Cabinet Files</span></span>](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[<span data-ttu-id="2ea41-146">Création de tables de fichier de module de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-146">Authoring Merge Module File Tables</span></span>](authoring-merge-module-file-tables.md)
</dt> <dt>

[<span data-ttu-id="2ea41-147">Création de tables ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="2ea41-147">Authoring ModuleSignature Tables</span></span>](authoring-modulesignature-tables.md)
</dt> <dt>

[<span data-ttu-id="2ea41-148">Création de tables ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="2ea41-148">Authoring ModuleComponents Tables</span></span>](authoring-modulecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="2ea41-149">Création de tables de séquence de module de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-149">Authoring Merge Module Sequence Tables</span></span>](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[<span data-ttu-id="2ea41-150">Validation des modules de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-150">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="2ea41-151">Création d’interfaces utilisateur dans les modules de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-151">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="2ea41-152">Création de tables de registre de module de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-152">Authoring Merge Module Registry Tables</span></span>](authoring-merge-module-registry-tables.md)
</dt> <dt>

[<span data-ttu-id="2ea41-153">Création de flux d’informations de résumé du module de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-153">Authoring Merge Module Summary Information Streams</span></span>](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[<span data-ttu-id="2ea41-154">Référence du flux de données de résumé du module de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-154">Merge Module Summary Information Stream Reference</span></span>](merge-module-summary-information-stream-reference.md)
</dt> <dt>

<span data-ttu-id="2ea41-155">Validation des modules de fusion</span><span class="sxs-lookup"><span data-stu-id="2ea41-155">Validating Merge Modules</span></span>
</dt> <dt>

[<span data-ttu-id="2ea41-156">Utilisation des modules de fusion 64 bits</span><span class="sxs-lookup"><span data-stu-id="2ea41-156">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



