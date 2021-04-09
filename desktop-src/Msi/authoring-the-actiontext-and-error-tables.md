---
description: Les exemples de spécifications incluent l’envoi de messages ActionData lorsqu’une action personnalisée crée ou supprime un compte d’utilisateur, et signale une erreur si un compte ne peut pas être créé.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Création des tables ActionText et Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864453"
---
# <a name="authoring-the-actiontext-and-error-tables"></a><span data-ttu-id="21686-103">Création des tables ActionText et Error</span><span class="sxs-lookup"><span data-stu-id="21686-103">Authoring the ActionText and Error Tables</span></span>

<span data-ttu-id="21686-104">Les exemples de spécifications incluent l’envoi de messages ActionData lorsqu’une action personnalisée crée ou supprime un compte d’utilisateur, et signale une erreur si un compte ne peut pas être créé.</span><span class="sxs-lookup"><span data-stu-id="21686-104">The sample specifications include sending ActionData messages when a custom action creates or removes a user account, and reporting an error if an account cannot be created.</span></span>

<span data-ttu-id="21686-105">Entrez les entrées suivantes dans la table ActionText pour fournir les informations utilisées par les messages ActionText.</span><span class="sxs-lookup"><span data-stu-id="21686-105">Enter the following entries into the ActionText table to provide information used by ActionText messages.</span></span>

[<span data-ttu-id="21686-106">Table ActionText</span><span class="sxs-lookup"><span data-stu-id="21686-106">ActionText Table</span></span>](actiontext-table.md)



| <span data-ttu-id="21686-107">Action</span><span class="sxs-lookup"><span data-stu-id="21686-107">Action</span></span>            | <span data-ttu-id="21686-108">Description</span><span class="sxs-lookup"><span data-stu-id="21686-108">Description</span></span>                                                       | <span data-ttu-id="21686-109">Modèle</span><span class="sxs-lookup"><span data-stu-id="21686-109">Template</span></span>                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="21686-110">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="21686-110">ProcessAccounts</span></span>   | <span data-ttu-id="21686-111">Génération d’actions pour créer des comptes d’utilisateur sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21686-111">Generating actions to create user accounts on the local computer.</span></span> | <span data-ttu-id="21686-112">Compte : \[ 1 \] , attributs : \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="21686-112">Account: \[1\], Attributes: \[2\]</span></span> |
| <span data-ttu-id="21686-113">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="21686-113">CreateAccount</span></span>     | <span data-ttu-id="21686-114">Création d’un compte d’utilisateur sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21686-114">Creating user account on the local computer.</span></span>                      | <span data-ttu-id="21686-115">Compte : \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="21686-115">Account: \[1\]</span></span>                    |
| <span data-ttu-id="21686-116">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="21686-116">RemoveAccount</span></span>     | <span data-ttu-id="21686-117">Suppression du compte d’utilisateur de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21686-117">Removing user account from the local computer.</span></span>                    | <span data-ttu-id="21686-118">Compte : \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="21686-118">Account: \[1\]</span></span>                    |
| <span data-ttu-id="21686-119">RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="21686-119">RollbackAccount</span></span>   | <span data-ttu-id="21686-120">Restauration de la création de comptes d’utilisateur sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21686-120">Rolling back the creation of user accounts on the local computer.</span></span> | <span data-ttu-id="21686-121">Compte : \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="21686-121">Account: \[1\]</span></span>                    |
| <span data-ttu-id="21686-122">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="21686-122">UninstallAccounts</span></span> | <span data-ttu-id="21686-123">Génération d’actions pour supprimer des comptes d’utilisateur sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21686-123">Generating actions to remove user accounts on the local computer.</span></span> | <span data-ttu-id="21686-124">Compte : \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="21686-124">Account: \[1\]</span></span>                    |



 

<span data-ttu-id="21686-125">Entrez les entrées suivantes dans la table d’erreurs pour fournir les informations utilisées par le rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="21686-125">Enter the following entries into the Error table to provide information used by error reporting.</span></span>

[<span data-ttu-id="21686-126">Table des erreurs</span><span class="sxs-lookup"><span data-stu-id="21686-126">Error Table</span></span>](error-table.md)



| <span data-ttu-id="21686-127">Error</span><span class="sxs-lookup"><span data-stu-id="21686-127">Error</span></span> | <span data-ttu-id="21686-128">Message</span><span class="sxs-lookup"><span data-stu-id="21686-128">Message</span></span>                                                                        |
|-------|--------------------------------------------------------------------------------|
| <span data-ttu-id="21686-129">25001</span><span class="sxs-lookup"><span data-stu-id="21686-129">25001</span></span> | <span data-ttu-id="21686-130">Impossible de créer le compte d’utilisateur « \[ 2 \] » sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21686-130">Unable to create user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="21686-131">Code d’erreur : \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="21686-131">Error Code: \[3\].</span></span> |
| <span data-ttu-id="21686-132">25002</span><span class="sxs-lookup"><span data-stu-id="21686-132">25002</span></span> | <span data-ttu-id="21686-133">Le compte d’utilisateur « \[ 2 \] » existe déjà sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21686-133">User account '\[2\]' already exists on the local machine.</span></span>                      |
| <span data-ttu-id="21686-134">25003</span><span class="sxs-lookup"><span data-stu-id="21686-134">25003</span></span> | <span data-ttu-id="21686-135">Impossible de supprimer le compte d’utilisateur' \[ 2 \] 'sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21686-135">Unable to remove user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="21686-136">Code d’erreur : \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="21686-136">Error Code: \[3\].</span></span> |
| <span data-ttu-id="21686-137">25004</span><span class="sxs-lookup"><span data-stu-id="21686-137">25004</span></span> | <span data-ttu-id="21686-138">Le compte d’utilisateur « \[ 2 \] » n’existe pas sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21686-138">User account '\[2\]' does not exist on the local machine.</span></span>                      |



 

<span data-ttu-id="21686-139">Passez à [la création de la table InstallExecuteSequence](authoring-the-installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="21686-139">Continue to [Authoring the InstallExecuteSequence Table](authoring-the-installexecutesequence-table.md).</span></span>

 

 



