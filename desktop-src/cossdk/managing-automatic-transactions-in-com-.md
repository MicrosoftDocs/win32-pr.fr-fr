---
description: Dans le modèle de programmation COM+, vous pouvez concevoir vos composants pour faire ce qu’ils font le mieux&\# 8212, en activant la logique métier ou en établissant une connexion de base de données&\# 8212 ; et s’appuient sur l’infrastructure de traitement des transactions de Microsoft Windows pour automatiser les transactions.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Gestion des transactions automatiques dans COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524055"
---
# <a name="managing-automatic-transactions-in-com"></a><span data-ttu-id="8a118-103">Gestion des transactions automatiques dans COM+</span><span class="sxs-lookup"><span data-stu-id="8a118-103">Managing Automatic Transactions in COM+</span></span>

<span data-ttu-id="8a118-104">Dans le modèle de programmation COM+, vous pouvez concevoir vos composants pour faire ce qu’ils font le mieux, en activant la logique métier ou en établissant une connexion de base de données, et s’appuyant sur l’infrastructure de traitement des transactions de Microsoft Windows pour automatiser les transactions.</span><span class="sxs-lookup"><span data-stu-id="8a118-104">In the COM+ programming model, you can design your components to do what they do best—enabling business logic or establishing a database connection—and rely on the transaction processing framework of Microsoft Windows to automate transactions.</span></span>

## <a name="starting-a-transaction"></a><span data-ttu-id="8a118-105">Démarrage d'une transaction</span><span class="sxs-lookup"><span data-stu-id="8a118-105">Starting a Transaction</span></span>

<span data-ttu-id="8a118-106">COM+ commence automatiquement une transaction lorsqu’il rencontre l’une des conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a118-106">COM+ automatically begins a transaction when it encounters either of the following conditions:</span></span>

-   <span data-ttu-id="8a118-107">Lorsqu’un client non transactionnel appelle un composant qui requiert une transaction ou nécessite une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="8a118-107">When a non-transactional client calls a component that requires a transaction or requires a new transaction.</span></span>
-   <span data-ttu-id="8a118-108">Lorsqu’un client transactionnel appelle un composant qui requiert une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="8a118-108">When a transactional client calls a component that requires a new transaction.</span></span>

<span data-ttu-id="8a118-109">Si COM+ détermine qu’un objet doit avoir une nouvelle transaction, il commence par commencer la transaction, puis place l’objet dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="8a118-109">If COM+ determines that an object should have a new transaction, it begins the transaction first and then places the object in it.</span></span> <span data-ttu-id="8a118-110">Le processus comporte les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a118-110">The process includes the following steps:</span></span>

1.  <span data-ttu-id="8a118-111">COM+ crée un objet de contexte, définit les attributs d' [activation](com--just-in-time-activation.md) et de [synchronisation](com--synchronization.md) JIT sur obligatoire, puis définit les [indicateurs consistent et Done](consistent-and-done-flags.md) sur true et false, respectivement.</span><span class="sxs-lookup"><span data-stu-id="8a118-111">COM+ creates a context object, sets both the [JIT activation](com--just-in-time-activation.md) and [Synchronization](com--synchronization.md) attributes to Required, and sets the [consistent and done flags](consistent-and-done-flags.md) to True and False, respectively.</span></span>
2.  <span data-ttu-id="8a118-112">COM+ communique avec le Distributed Transaction Coordinator (DTC) pour commencer une transaction.</span><span class="sxs-lookup"><span data-stu-id="8a118-112">COM+ communicates with the Distributed Transaction Coordinator (DTC) to begin a transaction.</span></span> <span data-ttu-id="8a118-113">Le DTC coordonne la transaction physique.</span><span class="sxs-lookup"><span data-stu-id="8a118-113">The DTC coordinates the physical transaction.</span></span>
3.  <span data-ttu-id="8a118-114">Le DTC génère un identificateur de transaction et le retourne à COM+.</span><span class="sxs-lookup"><span data-stu-id="8a118-114">The DTC generates a transaction identifier and passes it back to COM+.</span></span> <span data-ttu-id="8a118-115">L’identificateur de transaction établit une limite de transaction.</span><span class="sxs-lookup"><span data-stu-id="8a118-115">The transaction identifier establishes a transaction boundary.</span></span> <span data-ttu-id="8a118-116">Tous les objets participant à la transaction partagent le même identificateur.</span><span class="sxs-lookup"><span data-stu-id="8a118-116">All objects participating in the transaction share the same identifier.</span></span>
4.  <span data-ttu-id="8a118-117">Lorsque le client crée l’objet, COM+ l’active dans la limite de la transaction.</span><span class="sxs-lookup"><span data-stu-id="8a118-117">When the client creates the object, COM+ activates it within the transaction boundary.</span></span>

## <a name="ending-a-transaction"></a><span data-ttu-id="8a118-118">Fin d’une transaction</span><span class="sxs-lookup"><span data-stu-id="8a118-118">Ending a Transaction</span></span>

<span data-ttu-id="8a118-119">COM+ met fin à une transaction automatique en la validant ou en l’abandonnant lorsque l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="8a118-119">COM+ ends an automatic transaction by committing or aborting it when one of the following conditions occurs:</span></span>

-   <span data-ttu-id="8a118-120">L’objet racine de la transaction termine son travail et COM+ le libère.</span><span class="sxs-lookup"><span data-stu-id="8a118-120">The root object of the transaction completes its work and COM+ releases it.</span></span> <span data-ttu-id="8a118-121">Après la désactivation de l’objet racine, la transaction tente de valider.</span><span class="sxs-lookup"><span data-stu-id="8a118-121">After the root object deactivates, the transaction attempts to commit.</span></span>
-   <span data-ttu-id="8a118-122">Le client libère l’objet racine.</span><span class="sxs-lookup"><span data-stu-id="8a118-122">The client releases the root object.</span></span> <span data-ttu-id="8a118-123">Sans référence, l’objet racine est désactivé et la transaction tente de valider.</span><span class="sxs-lookup"><span data-stu-id="8a118-123">Without a reference, the root object deactivates and the transaction attempts to commit.</span></span>
-   <span data-ttu-id="8a118-124">La transaction dépasse son seuil de délai d’expiration.</span><span class="sxs-lookup"><span data-stu-id="8a118-124">The transaction exceeds its time-out threshold.</span></span> <span data-ttu-id="8a118-125">La transaction est automatiquement abandonnée si elle n’est pas validée dans le délai d’expiration de la transaction, ce qui désactive tous les objets associés à la transaction.</span><span class="sxs-lookup"><span data-stu-id="8a118-125">The transaction aborts automatically if not committed within the transaction time-out period, deactivating all objects associated with the transaction.</span></span> <span data-ttu-id="8a118-126">Le délai d’expiration de la transaction par défaut est de 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="8a118-126">The default transaction time-out period is 60 seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a118-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a118-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a118-128">Indicateurs cohérents et terminés</span><span class="sxs-lookup"><span data-stu-id="8a118-128">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="8a118-129">Accélération des transactions en avertissant l’objet racine</span><span class="sxs-lookup"><span data-stu-id="8a118-129">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[<span data-ttu-id="8a118-130">Fin d’une transaction automatique en appelant SetComplete</span><span class="sxs-lookup"><span data-stu-id="8a118-130">Terminating an Automatic Transaction by Calling SetComplete</span></span>](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



