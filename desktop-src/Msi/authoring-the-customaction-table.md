---
description: Entrez les enregistrements des cinq exemples d’actions personnalisées créés dans la section précédente dans la table CustomAction. Pour plus d’informations sur la façon de remplir la table CustomAction pour ce type d’action personnalisée, consultez action personnalisée type 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Création de la table CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951757"
---
# <a name="authoring-the-customaction-table"></a><span data-ttu-id="a1cc6-104">Création de la table CustomAction</span><span class="sxs-lookup"><span data-stu-id="a1cc6-104">Authoring the CustomAction Table</span></span>

<span data-ttu-id="a1cc6-105">Entrez les enregistrements des cinq exemples d’actions personnalisées créés dans la section précédente dans la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1cc6-105">Enter records for the five sample custom actions created in the previous section to the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="a1cc6-106">Pour plus d’informations sur la façon de remplir la table CustomAction pour ce type d’action personnalisée, consultez [action personnalisée type 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="a1cc6-106">For more information on how to populate the CustomAction table for this type of custom action see [Custom Action Type 1](custom-action-type-1.md).</span></span>

[<span data-ttu-id="a1cc6-107">Table CustomAction</span><span class="sxs-lookup"><span data-stu-id="a1cc6-107">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="a1cc6-108">Action</span><span class="sxs-lookup"><span data-stu-id="a1cc6-108">Action</span></span>            | <span data-ttu-id="a1cc6-109">Type</span><span class="sxs-lookup"><span data-stu-id="a1cc6-109">Type</span></span>  | <span data-ttu-id="a1cc6-110">Source</span><span class="sxs-lookup"><span data-stu-id="a1cc6-110">Source</span></span>      | <span data-ttu-id="a1cc6-111">Cible</span><span class="sxs-lookup"><span data-stu-id="a1cc6-111">Target</span></span>                |
|-------------------|-------|-------------|-----------------------|
| <span data-ttu-id="a1cc6-112">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="a1cc6-112">ProcessAccounts</span></span>   | <span data-ttu-id="a1cc6-113">1</span><span class="sxs-lookup"><span data-stu-id="a1cc6-113">1</span></span>     | <span data-ttu-id="a1cc6-114">Process.dll</span><span class="sxs-lookup"><span data-stu-id="a1cc6-114">Process.dll</span></span> | <span data-ttu-id="a1cc6-115">ProcessUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a1cc6-115">ProcessUserAccounts</span></span>   |
| <span data-ttu-id="a1cc6-116">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="a1cc6-116">UninstallAccounts</span></span> | <span data-ttu-id="a1cc6-117">1</span><span class="sxs-lookup"><span data-stu-id="a1cc6-117">1</span></span>     | <span data-ttu-id="a1cc6-118">Process.dll</span><span class="sxs-lookup"><span data-stu-id="a1cc6-118">Process.dll</span></span> | <span data-ttu-id="a1cc6-119">UninstallUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a1cc6-119">UninstallUserAccounts</span></span> |
| <span data-ttu-id="a1cc6-120">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="a1cc6-120">CreateAccount</span></span>     | <span data-ttu-id="a1cc6-121">11265</span><span class="sxs-lookup"><span data-stu-id="a1cc6-121">11265</span></span> | <span data-ttu-id="a1cc6-122">Create.dll</span><span class="sxs-lookup"><span data-stu-id="a1cc6-122">Create.dll</span></span>  | <span data-ttu-id="a1cc6-123">CreateUserAccount</span><span class="sxs-lookup"><span data-stu-id="a1cc6-123">CreateUserAccount</span></span>     |
| <span data-ttu-id="a1cc6-124">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="a1cc6-124">RemoveAccount</span></span>     | <span data-ttu-id="a1cc6-125">11265</span><span class="sxs-lookup"><span data-stu-id="a1cc6-125">11265</span></span> | <span data-ttu-id="a1cc6-126">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="a1cc6-126">Remove.dll</span></span>  | <span data-ttu-id="a1cc6-127">RemoveUserAccount</span><span class="sxs-lookup"><span data-stu-id="a1cc6-127">RemoveUserAccount</span></span>     |
| <span data-ttu-id="a1cc6-128">RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="a1cc6-128">RollbackAccount</span></span>   | <span data-ttu-id="a1cc6-129">9473</span><span class="sxs-lookup"><span data-stu-id="a1cc6-129">9473</span></span>  | <span data-ttu-id="a1cc6-130">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="a1cc6-130">Remove.dll</span></span>  | <span data-ttu-id="a1cc6-131">RemoveUserAccount</span><span class="sxs-lookup"><span data-stu-id="a1cc6-131">RemoveUserAccount</span></span>     |



 

<span data-ttu-id="a1cc6-132">Le code source C++ pour les bibliothèques de liens dynamiques est fourni dans le kit de développement logiciel (SDK) Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a1cc6-132">The C++ source code for the dynamic-link libraries are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="a1cc6-133">Utilisez Process. cpp pour créer le fichier Process.dll.</span><span class="sxs-lookup"><span data-stu-id="a1cc6-133">Use Process.cpp to create the file Process.dll.</span></span> <span data-ttu-id="a1cc6-134">Utilisez CREATE. cpp pour créer le fichier Create.dll.</span><span class="sxs-lookup"><span data-stu-id="a1cc6-134">Use Create.cpp to create the file Create.dll.</span></span> <span data-ttu-id="a1cc6-135">Utilisez Remove. cpp pour créer Remove.dll.</span><span class="sxs-lookup"><span data-stu-id="a1cc6-135">Use Remove.cpp to create Remove.dll.</span></span> <span data-ttu-id="a1cc6-136">Ajoutez ces fichiers de bibliothèque de liens dynamiques à la table binaire.</span><span class="sxs-lookup"><span data-stu-id="a1cc6-136">Add these dynamic-link library files to the Binary table.</span></span>

[<span data-ttu-id="a1cc6-137">Table binaire</span><span class="sxs-lookup"><span data-stu-id="a1cc6-137">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="a1cc6-138">Nom</span><span class="sxs-lookup"><span data-stu-id="a1cc6-138">Name</span></span>        | <span data-ttu-id="a1cc6-139">Données</span><span class="sxs-lookup"><span data-stu-id="a1cc6-139">Data</span></span>            |
|-------------|-----------------|
| <span data-ttu-id="a1cc6-140">Process.dll</span><span class="sxs-lookup"><span data-stu-id="a1cc6-140">Process.dll</span></span> | <span data-ttu-id="a1cc6-141">{*données binaires*}</span><span class="sxs-lookup"><span data-stu-id="a1cc6-141">{*binary data*}</span></span> |
| <span data-ttu-id="a1cc6-142">Create.dll</span><span class="sxs-lookup"><span data-stu-id="a1cc6-142">Create.dll</span></span>  | <span data-ttu-id="a1cc6-143">{*données binaires*}</span><span class="sxs-lookup"><span data-stu-id="a1cc6-143">{*binary data*}</span></span> |
| <span data-ttu-id="a1cc6-144">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="a1cc6-144">Remove.dll</span></span>  | <span data-ttu-id="a1cc6-145">{*données binaires*}</span><span class="sxs-lookup"><span data-stu-id="a1cc6-145">{*binary data*}</span></span> |



 

<span data-ttu-id="a1cc6-146">Continuez à [Ajouter une table CustomUserAccounts personnalisée](adding-a-custom-customuseraccounts-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1cc6-146">Continue to [Adding a Custom CustomUserAccounts Table](adding-a-custom-customuseraccounts-table.md).</span></span>

 

 



