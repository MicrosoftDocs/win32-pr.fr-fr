---
description: Utilisation de composants non transactionnels dans une transaction
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Utilisation de composants non transactionnels dans une transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75cd8ebc756971a56413e371cf23de2144e5816
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748989"
---
# <a name="using-non-transactional-components-in-a-transaction"></a><span data-ttu-id="9b350-103">Utilisation de composants non transactionnels dans une transaction</span><span class="sxs-lookup"><span data-stu-id="9b350-103">Using Non-Transactional Components in a Transaction</span></span>

<span data-ttu-id="9b350-104">Il est souvent utile de placer des composants non transactionnels dans une transaction pour tirer parti des [propriétés ACID](acid-properties.md) des transactions.</span><span class="sxs-lookup"><span data-stu-id="9b350-104">It is often useful to place non-transactional components into a transaction to take advantage of the [ACID properties](acid-properties.md) of transactions.</span></span> <span data-ttu-id="9b350-105">Par exemple, si vous avez des composants hérités non transactionnels que vous utilisez pour mettre à jour des mots de passe sur un réseau, vous pouvez placer ces composants dans une transaction pour vous assurer que les mises à jour de mot de passe sont cohérentes sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="9b350-105">For example, if you have non-transactional legacy components that you use to update passwords on a network, you can place those components in a transaction to ensure that password updates are consistent across the network.</span></span>

<span data-ttu-id="9b350-106">L' *objet de contexte de transaction* est un objet générique qui permet aux clients non transactionnels de combiner le travail de plusieurs objets com en une seule transaction, sans que vous ayez besoin de développer un nouveau composant spécifiquement à cet effet.</span><span class="sxs-lookup"><span data-stu-id="9b350-106">The *transaction context object* is a generic object that allows non-transactional clients to combine the work of multiple COM objects into a single transaction, without requiring you to develop a new component specifically for that purpose.</span></span> <span data-ttu-id="9b350-107">Contrairement à une transaction automatique, l’objet de contexte de transaction requiert que son client valide ou abandonne explicitement la transaction.</span><span class="sxs-lookup"><span data-stu-id="9b350-107">In contrast to an automatic transaction, the transaction context object requires its client to explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="9b350-108">Par défaut, la valeur d’attribut de transaction de l’objet de contexte de transaction est définie sur obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9b350-108">By default, the transaction attribute value of the transaction context object is set to Required.</span></span> <span data-ttu-id="9b350-109">COM+ abandonne la transaction si le client libère l’objet de contexte de transaction sans émettre explicitement un appel de validation ou d’abandon.</span><span class="sxs-lookup"><span data-stu-id="9b350-109">COM+ aborts the transaction if the client releases the transaction context object without explicitly issuing a commit or abort call.</span></span>

<span data-ttu-id="9b350-110">L’exemple de Visual Basic suivant montre comment un client non transactionnel peut composer le travail effectué par plusieurs objets en une seule transaction :</span><span class="sxs-lookup"><span data-stu-id="9b350-110">The following Visual Basic example shows how a non-transactional client can compose the work done by more than one object into a single transaction:</span></span>


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a><span data-ttu-id="9b350-111">Limitations de l’objet de contexte de transaction</span><span class="sxs-lookup"><span data-stu-id="9b350-111">Limitations of the Transaction Context Object</span></span>

<span data-ttu-id="9b350-112">Voici quelques limitations importantes de l’objet de contexte de transaction :</span><span class="sxs-lookup"><span data-stu-id="9b350-112">Following are some important limitations of the transaction context object:</span></span>

-   <span data-ttu-id="9b350-113">Lors de l’utilisation d’un objet de contexte de transaction, la logique d’application qui associe le travail de plusieurs objets dans une transaction unique est liée à une implémentation de client non transactionnelle spécifique et certains avantages de l’utilisation des composants COM sont perdus.</span><span class="sxs-lookup"><span data-stu-id="9b350-113">When using a transaction context object, the application logic that combines the work of multiple objects into a single transaction is tied to a specific non-transactional client implementation and some advantages of using COM components are lost.</span></span> <span data-ttu-id="9b350-114">Ces avantages sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="9b350-114">These lost advantages include the following:</span></span>
    -   <span data-ttu-id="9b350-115">Possibilité de réutiliser la logique d’application dans le cadre d’une transaction encore plus volumineuse</span><span class="sxs-lookup"><span data-stu-id="9b350-115">Ability to reuse the application logic as part of an even larger transaction</span></span>
    -   <span data-ttu-id="9b350-116">Disposition de la sécurité déclarative</span><span class="sxs-lookup"><span data-stu-id="9b350-116">Imposition of declarative security</span></span>
    -   <span data-ttu-id="9b350-117">Flexibilité pour exécuter la logique à distance à partir du client</span><span class="sxs-lookup"><span data-stu-id="9b350-117">Flexibility to run the logic remotely from the client</span></span>
-   <span data-ttu-id="9b350-118">L’objet de contexte de transaction s’exécute in-process avec le client non transactionnel, ce qui signifie que COM+ doit être disponible sur l’ordinateur client non transactionnel.</span><span class="sxs-lookup"><span data-stu-id="9b350-118">The transaction context object runs in-process with the non-transactional client, which means that COM+ must be available on the non-transactional client computer.</span></span> <span data-ttu-id="9b350-119">Cela peut ne pas être un problème, par exemple lorsque l’objet de contexte de transaction est utilisé à partir d’une page ASP (Active Server Pages) qui s’exécute sur le même serveur que COM+.</span><span class="sxs-lookup"><span data-stu-id="9b350-119">This might not be a problem, for example, when the transaction context object is used from an Active Server Pages (ASP) page that is running on the same server as COM+.</span></span>
-   <span data-ttu-id="9b350-120">Vous n’avez pas de contexte pour le client non transactionnel lorsque vous créez un objet de contexte de transaction.</span><span class="sxs-lookup"><span data-stu-id="9b350-120">You do not get a context for the non-transactional client when you create a transaction context object.</span></span> <span data-ttu-id="9b350-121">Le travail transactionnel ne peut être effectué indirectement que par le biais d’objets COM créés à l’aide de l’objet de contexte de transaction.</span><span class="sxs-lookup"><span data-stu-id="9b350-121">Transactional work can only be done indirectly, through COM objects created by using the transaction context object.</span></span> <span data-ttu-id="9b350-122">En particulier, le client non transactionnel ne peut pas utiliser les distributeurs de ressources COM+ (tels que ODBC) et faire en sorte que le travail soit inclus dans la transaction.</span><span class="sxs-lookup"><span data-stu-id="9b350-122">In particular, the non-transactional client cannot use COM+ resource dispensers (such as ODBC) and have the work included in the transaction.</span></span> <span data-ttu-id="9b350-123">Par exemple, les développeurs peuvent être familiarisés avec la syntaxe suivante pour le travail transactionnel sur des systèmes de base de données relationnelle :</span><span class="sxs-lookup"><span data-stu-id="9b350-123">For example, developers may be familiar with the following syntax for doing transactional work on relational database systems:</span></span>

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    <span data-ttu-id="9b350-124">L’utilisation de l’objet de contexte de transaction de façon similaire ne produit pas le résultat souhaité :</span><span class="sxs-lookup"><span data-stu-id="9b350-124">Using the transaction context object in a similar way does not yield the desired result:</span></span>

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    <span data-ttu-id="9b350-125">L’appel à la solution dans cet exemple n’est pas inscrit dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="9b350-125">The call to DoWork in this example is not enlisted in a transaction.</span></span> <span data-ttu-id="9b350-126">Au lieu de cela, vous devez créer un composant COM qui appelle le rôle de travail, créer une instance d’objet de ce composant à l’aide de l’objet de contexte de transaction, puis appeler cet objet à partir du client non transactionnel pour que le travail fasse partie de la transaction contrôlée par le client.</span><span class="sxs-lookup"><span data-stu-id="9b350-126">Instead, you must build a COM component that calls DoWork, create an object instance of that component using the transaction context object, and then call that object from the non-transactional client for the work to be part of the client-controlled transaction.</span></span>

 

 



