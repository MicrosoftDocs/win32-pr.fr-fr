---
description: Une transaction est un objet qui définit une unité logique de travail.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transactions (gestionnaire de transactions du noyau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534480"
---
# <a name="transactions"></a><span data-ttu-id="00812-103">Transactions</span><span class="sxs-lookup"><span data-stu-id="00812-103">Transactions</span></span>

<span data-ttu-id="00812-104">Une transaction est un objet qui définit une unité logique de travail.</span><span class="sxs-lookup"><span data-stu-id="00812-104">A transaction is an object that defines a logical unit of work.</span></span> <span data-ttu-id="00812-105">La transaction est active tant qu’il existe un handle référençant la transaction et qu’elle est considérée comme active si la transaction n’a pas encore été validée ou restaurée.</span><span class="sxs-lookup"><span data-stu-id="00812-105">The transaction is alive as long as there is a handle referencing the transaction and it is considered active if the transaction has not yet been committed or rolled back.</span></span> <span data-ttu-id="00812-106">Si une transaction est créée et que tous ses descripteurs ont été fermés avant qu’une validation ou une restauration ne se produise, la transaction est restaurée.</span><span class="sxs-lookup"><span data-stu-id="00812-106">If a transaction is created and all handles to it have been closed before a commit or rollback occurs, the transaction will be rolled back.</span></span>

<span data-ttu-id="00812-107">Prenons le cas d’un client transactionnel en mode utilisateur qui crée une transaction pour l’étendue de ses opérations, puis effectue des mises à jour sur un ou plusieurs gestionnaires de ressources.</span><span class="sxs-lookup"><span data-stu-id="00812-107">Consider the case of a user-mode transactional client that creates a transaction to scope its operations, then performs updates on one or more resource managers.</span></span> <span data-ttu-id="00812-108">Il se produit ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="00812-108">The following occurs:</span></span>

1.  <span data-ttu-id="00812-109">Le client appelle la fonction [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) pour créer la transaction et reçoit un descripteur de cette transaction comme valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="00812-109">The client calls the [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) function to create the transaction and receives a handle to that transaction as the return value.</span></span>

    <span data-ttu-id="00812-110">La transaction peut être ouverte ou héritée par n’importe quel nombre de processus ; chaque processus est donc impliqué dans la transaction.</span><span class="sxs-lookup"><span data-stu-id="00812-110">The transaction can be opened or inherited by any number of processes; each process is thus involved in the transaction.</span></span> <span data-ttu-id="00812-111">L’échec de l’un de ces processus entraîne l’abandon de la transaction.</span><span class="sxs-lookup"><span data-stu-id="00812-111">The failure of any of these processes will cause the transaction to abort.</span></span>

    <span data-ttu-id="00812-112">Cette transaction n’est peut-être pas encore persistante.</span><span class="sxs-lookup"><span data-stu-id="00812-112">This transaction may not yet be persistent.</span></span> <span data-ttu-id="00812-113">Seules les transactions ayant atteint l’état préparé doivent être récupérées sur les défaillances du système si la transaction utilise la journalisation présumée-abandonner.</span><span class="sxs-lookup"><span data-stu-id="00812-113">Only transactions that have reached the prepared state must be recovered across system failures if the transaction uses presumed-abort logging.</span></span>

2.  <span data-ttu-id="00812-114">Le client doit transmettre une transaction au gestionnaire des ressources de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="00812-114">The client must pass a transaction to the resource manager explicitly.</span></span>
3.  <span data-ttu-id="00812-115">Le client effectue toutes ses opérations transactionnelles avec un ou plusieurs services RMs, tels que les systèmes de fichiers traités.</span><span class="sxs-lookup"><span data-stu-id="00812-115">The client performs all its transactional operations with one or more RMs, such as transacted file systems.</span></span>
4.  <span data-ttu-id="00812-116">Le client appelle la fonction [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) .</span><span class="sxs-lookup"><span data-stu-id="00812-116">The client calls the [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) function.</span></span>
5.  <span data-ttu-id="00812-117">Le gestionnaire des ressources reçoit les notifications de KTM pour préparer et valider ses données.</span><span class="sxs-lookup"><span data-stu-id="00812-117">The resource manager receives notifications from KTM to prepare and commit its data.</span></span>

## <a name="transactions-and-threads"></a><span data-ttu-id="00812-118">Transactions et threads</span><span class="sxs-lookup"><span data-stu-id="00812-118">Transactions and Threads</span></span>

<span data-ttu-id="00812-119">Les transactions ne sont pas les mêmes que les threads.</span><span class="sxs-lookup"><span data-stu-id="00812-119">Transactions are not the same as threads.</span></span> <span data-ttu-id="00812-120">Plusieurs threads ou processus peuvent faire partie d’une transaction unique.</span><span class="sxs-lookup"><span data-stu-id="00812-120">Multiple threads or processes can be a part of a single transaction.</span></span> <span data-ttu-id="00812-121">À l’inverse, un thread peut faire partie de plusieurs transactions différentes à différents moments.</span><span class="sxs-lookup"><span data-stu-id="00812-121">Conversely, a thread can be a part of several different transactions at different times.</span></span>

## <a name="transaction-functions"></a><span data-ttu-id="00812-122">Fonctions de transaction</span><span class="sxs-lookup"><span data-stu-id="00812-122">Transaction Functions</span></span>

<span data-ttu-id="00812-123">Les fonctions suivantes sont utilisées avec les transactions.</span><span class="sxs-lookup"><span data-stu-id="00812-123">The following functions are used with transactions.</span></span>



| <span data-ttu-id="00812-124">Fonction</span><span class="sxs-lookup"><span data-stu-id="00812-124">Function</span></span>                                                            | <span data-ttu-id="00812-125">Description</span><span class="sxs-lookup"><span data-stu-id="00812-125">Description</span></span>                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00812-126">**CommitTransaction**</span><span class="sxs-lookup"><span data-stu-id="00812-126">**CommitTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | <span data-ttu-id="00812-127">Demande que la transaction spécifiée soit validée.</span><span class="sxs-lookup"><span data-stu-id="00812-127">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="00812-128">**CommitTransactionAsync**</span><span class="sxs-lookup"><span data-stu-id="00812-128">**CommitTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | <span data-ttu-id="00812-129">Demande que la transaction spécifiée soit validée.</span><span class="sxs-lookup"><span data-stu-id="00812-129">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="00812-130">**CreateTransaction**</span><span class="sxs-lookup"><span data-stu-id="00812-130">**CreateTransaction**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | <span data-ttu-id="00812-131">Crée un nouvel objet de transaction.</span><span class="sxs-lookup"><span data-stu-id="00812-131">Creates a new transaction object.</span></span>                                                             |
| [<span data-ttu-id="00812-132">**GetTransactionInformation**</span><span class="sxs-lookup"><span data-stu-id="00812-132">**GetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | <span data-ttu-id="00812-133">Retourne les informations demandées sur la transaction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="00812-133">Returns the requested information about the specified transaction.</span></span>                            |
| [<span data-ttu-id="00812-134">**OpenTransaction**</span><span class="sxs-lookup"><span data-stu-id="00812-134">**OpenTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | <span data-ttu-id="00812-135">Ouvre une transaction existante.</span><span class="sxs-lookup"><span data-stu-id="00812-135">Opens an existing transaction.</span></span>                                                                |
| [<span data-ttu-id="00812-136">**RollbackTransaction**</span><span class="sxs-lookup"><span data-stu-id="00812-136">**RollbackTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | <span data-ttu-id="00812-137">Demande que la transaction spécifiée soit restaurée.</span><span class="sxs-lookup"><span data-stu-id="00812-137">Requests that the specified transaction be rolled back.</span></span>                                       |
| [<span data-ttu-id="00812-138">**RollbackTransactionAsync**</span><span class="sxs-lookup"><span data-stu-id="00812-138">**RollbackTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | <span data-ttu-id="00812-139">Demande que la transaction spécifiée soit restaurée.</span><span class="sxs-lookup"><span data-stu-id="00812-139">Requests that the specified transaction be rolled back.</span></span> <span data-ttu-id="00812-140">Cette fonction retourne de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="00812-140">This function returns asynchronously.</span></span> |
| [<span data-ttu-id="00812-141">**SetTransactionInformation**</span><span class="sxs-lookup"><span data-stu-id="00812-141">**SetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | <span data-ttu-id="00812-142">Définit les informations de transaction pour la transaction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="00812-142">Sets the transaction information for the specified transaction.</span></span>                               |



 

 

 



