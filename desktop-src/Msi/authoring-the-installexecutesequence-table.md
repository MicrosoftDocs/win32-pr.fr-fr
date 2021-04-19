---
description: Les actions personnalisées ProcessAccounts et UninstallAccounts génèrent les actions personnalisées différées qui créent, suppriment ou restaurent des comptes d’utilisateur.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Création de la table InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527852"
---
# <a name="authoring-the-installexecutesequence-table"></a><span data-ttu-id="02e0f-103">Création de la table InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="02e0f-103">Authoring the InstallExecuteSequence Table</span></span>

<span data-ttu-id="02e0f-104">Les actions personnalisées ProcessAccounts et UninstallAccounts génèrent les actions personnalisées différées qui créent, suppriment ou restaurent des comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="02e0f-104">The custom actions ProcessAccounts and UninstallAccounts generate the deferred custom actions that create, remove, or rollback user accounts.</span></span> <span data-ttu-id="02e0f-105">Les actions personnalisées ProcessAccounts et UninstallAccounts doivent être entrées dans la [table InstallExecuteSequence](installexecutesequence-table.md) à exécuter.</span><span class="sxs-lookup"><span data-stu-id="02e0f-105">The custom actions ProcessAccounts and UninstallAccounts must be entered into the [InstallExecuteSequence table](installexecutesequence-table.md) to be executed.</span></span> <span data-ttu-id="02e0f-106">Ajoutez les entrées suivantes à la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="02e0f-106">Add the following entries to the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="02e0f-107">Étant donné que ces actions personnalisées doivent faire partie de la génération de script, les deux actions personnalisées doivent être séquencées après l' [action InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="02e0f-107">Because these custom actions must be a part of the script generation, both custom actions must be sequenced after the [InstallInitialize action](installinitialize-action.md).</span></span>

<span data-ttu-id="02e0f-108">La condition sur ProcessAccounts garantit ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="02e0f-108">The condition on ProcessAccounts ensures the following.</span></span> <span data-ttu-id="02e0f-109">Consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="02e0f-109">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

-   <span data-ttu-id="02e0f-110">ProcessAccounts s’exécute uniquement si le composant TestAccount est installé localement sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="02e0f-110">ProcessAccounts runs only if the component TestAccount is being installed locally on the computer.</span></span>
-   <span data-ttu-id="02e0f-111">Le compte de test de composant n’est actuellement pas installé ou est installé pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="02e0f-111">The component Test Account is currently not installed or is installed to run from the source.</span></span>

<span data-ttu-id="02e0f-112">La condition sur UninstallAccount garantit les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="02e0f-112">The condition on UninstallAccount ensures the following:</span></span>

-   <span data-ttu-id="02e0f-113">UninstallAccounts s’exécute uniquement si le composant TestAccount est installé localement sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="02e0f-113">UninstallAccounts runs only if the component TestAccount is installed locally on the computer.</span></span>
-   <span data-ttu-id="02e0f-114">Le compte de test de composant est en cours de suppression ou d’installation pour être exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="02e0f-114">The component Test Account is being removed or being installed to run from the source.</span></span>

[<span data-ttu-id="02e0f-115">Table InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="02e0f-115">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="02e0f-116">Action</span><span class="sxs-lookup"><span data-stu-id="02e0f-116">Action</span></span>            | <span data-ttu-id="02e0f-117">Condition</span><span class="sxs-lookup"><span data-stu-id="02e0f-117">Condition</span></span>                                                           | <span data-ttu-id="02e0f-118">Séquence</span><span class="sxs-lookup"><span data-stu-id="02e0f-118">Sequence</span></span> |
|-------------------|---------------------------------------------------------------------|----------|
| <span data-ttu-id="02e0f-119">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="02e0f-119">ProcessAccounts</span></span>   | <span data-ttu-id="02e0f-120">VersionNT et ( ? TestAccount = 2 ou ? TestAccount = 4) et $TestAccount = 3</span><span class="sxs-lookup"><span data-stu-id="02e0f-120">VersionNT AND (?TestAccount=2 OR ?TestAccount=4) AND $TestAccount=3</span></span> | <span data-ttu-id="02e0f-121">1550</span><span class="sxs-lookup"><span data-stu-id="02e0f-121">1550</span></span>     |
| <span data-ttu-id="02e0f-122">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="02e0f-122">UninstallAccounts</span></span> | <span data-ttu-id="02e0f-123">VersionNT et ? TestAccount = 3 et ($TestAccount = 4 ou $TestAccount = 2)</span><span class="sxs-lookup"><span data-stu-id="02e0f-123">VersionNT AND ?TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2)</span></span> | <span data-ttu-id="02e0f-124">1560</span><span class="sxs-lookup"><span data-stu-id="02e0f-124">1560</span></span>     |



 

<span data-ttu-id="02e0f-125">Continuez à [créer l’interface utilisateur pour l’entrée de mot de passe](authoring-the-user-interface-for-password-input.md).</span><span class="sxs-lookup"><span data-stu-id="02e0f-125">Continue to [Authoring the user interface for password input](authoring-the-user-interface-for-password-input.md).</span></span>

 

 



