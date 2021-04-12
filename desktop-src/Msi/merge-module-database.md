---
description: La base de données d’un module de fusion contient toutes les propriétés d’installation et la logique de configuration pour le module.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Base de données de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319838"
---
# <a name="merge-module-database"></a><span data-ttu-id="cf29e-103">Base de données de module de fusion</span><span class="sxs-lookup"><span data-stu-id="cf29e-103">Merge Module Database</span></span>

<span data-ttu-id="cf29e-104">La base de données d’un module de fusion contient toutes les propriétés d’installation et la logique de configuration pour le module.</span><span class="sxs-lookup"><span data-stu-id="cf29e-104">The database of a merge module contains all the installation properties and setup logic for the module.</span></span> <span data-ttu-id="cf29e-105">Il s’agit essentiellement d’une [base de données de programme d’installation](installer-database.md) simplifiée ou d’un fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="cf29e-105">It is essentially a simplified [installer database](installer-database.md) or .msi file.</span></span> <span data-ttu-id="cf29e-106">Les fichiers de base de données de module de fusion standard sont indiqués par une extension. msm.</span><span class="sxs-lookup"><span data-stu-id="cf29e-106">Standard merge module database files are indicated by an .msm extension.</span></span> <span data-ttu-id="cf29e-107">Pour obtenir la liste de toutes les tables de base de données qui peuvent exister dans les modules de fusion, consultez [tables de base de données de module de fusion](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cf29e-107">For a list of all database tables that can exist in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span> <span data-ttu-id="cf29e-108">Les tables suivantes sont requises dans la base de données de chaque fichier. msm :</span><span class="sxs-lookup"><span data-stu-id="cf29e-108">The following tables are required in the database of every .msm file:</span></span>

[<span data-ttu-id="cf29e-109">Composant</span><span class="sxs-lookup"><span data-stu-id="cf29e-109">Component</span></span>](component-table.md)

[<span data-ttu-id="cf29e-110">Directory</span><span class="sxs-lookup"><span data-stu-id="cf29e-110">Directory</span></span>](directory-table.md)

[<span data-ttu-id="cf29e-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="cf29e-111">FeatureComponents</span></span>](featurecomponents-table.md)

[<span data-ttu-id="cf29e-112">File</span><span class="sxs-lookup"><span data-stu-id="cf29e-112">File</span></span>](file-table.md)

[<span data-ttu-id="cf29e-113">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="cf29e-113">ModuleSignature</span></span>](modulesignature-table.md)

[<span data-ttu-id="cf29e-114">ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="cf29e-114">ModuleComponents</span></span>](modulecomponents-table.md)

<span data-ttu-id="cf29e-115">Notez que le composant, le répertoire, FeatureComponents et les tables de fichiers sont également présents dans tous les fichiers. msi.</span><span class="sxs-lookup"><span data-stu-id="cf29e-115">Note that the Component, Directory, FeatureComponents, and File tables are also present in all .msi files.</span></span> <span data-ttu-id="cf29e-116">Une base de données de module de fusion ne contient pas de [table de fonctionnalités](feature-table.md) et le fichier. msm ne peut donc pas être installé seul.</span><span class="sxs-lookup"><span data-stu-id="cf29e-116">A merge module database does not contain a [Feature table](feature-table.md) and so the .msm file cannot be installed alone.</span></span> <span data-ttu-id="cf29e-117">Pour installer un module de fusion, il doit d’abord être fusionné à l’aide d’un outil de fusion dans un fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="cf29e-117">To install a merge module, it must first be merged by using a merge tool into an .msi file.</span></span>

<span data-ttu-id="cf29e-118">La [table ModuleSignature](modulesignature-table.md) est uniquement présente dans les fichiers. msi qui ont été fusionnés avec au moins un fichier. msm.</span><span class="sxs-lookup"><span data-stu-id="cf29e-118">The [ModuleSignature Table](modulesignature-table.md) is only present in .msi files that has been merged with at least one .msm file.</span></span> <span data-ttu-id="cf29e-119">Si cette table est présente dans un fichier. msi, elle contient un enregistrement pour chaque module de fusion précédemment fusionné dans la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="cf29e-119">If this table is present in an .msi file, it contains one record for each merge module that has been previously merged into the installation database.</span></span>

<span data-ttu-id="cf29e-120">Les modules de fusion peuvent contenir des tables de séquences MergeModule facultatives.</span><span class="sxs-lookup"><span data-stu-id="cf29e-120">Merge modules may contain optional MergeModule Sequence tables.</span></span> <span data-ttu-id="cf29e-121">Ces tables se produisent uniquement dans les fichiers. msm.</span><span class="sxs-lookup"><span data-stu-id="cf29e-121">These tables occur only in .msm files.</span></span> <span data-ttu-id="cf29e-122">Lorsque les fichiers. msm sont fusionnés dans un fichier. msi, ces tables modifient les [*tables de séquences*](s-gly.md) d’action du fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="cf29e-122">When the .msm files are merged into an .msi file, these tables modify the action [*sequence tables*](s-gly.md) of the .msi file.</span></span>

<span data-ttu-id="cf29e-123">Les modules de fusion peuvent contenir des tables personnalisées.</span><span class="sxs-lookup"><span data-stu-id="cf29e-123">Merge modules may contain custom tables.</span></span> <span data-ttu-id="cf29e-124">Ces tables sont utilisées par les [actions personnalisées](custom-actions.md) définies dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="cf29e-124">These tables are used by [custom actions](custom-actions.md) defined in the merge module.</span></span>

<span data-ttu-id="cf29e-125">Les modules de fusion requièrent rarement des tables d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf29e-125">Merge modules rarely require user interface tables.</span></span> <span data-ttu-id="cf29e-126">Ces tables doivent être présentes uniquement dans de rares cas où le module de fusion requiert une entrée de l’utilisateur pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="cf29e-126">These tables need to be present only in rare cases where the merge module requires input from the user during installation.</span></span> <span data-ttu-id="cf29e-127">Pour plus d’informations, consultez [création d’interfaces utilisateur dans les modules de fusion](authoring-user-interfaces-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="cf29e-127">For more information, see [Authoring User Interfaces in Merge Modules](authoring-user-interfaces-in-merge-modules.md).</span></span>

 

 



