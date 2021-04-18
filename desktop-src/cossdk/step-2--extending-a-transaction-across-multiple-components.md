---
description: 'Étape 2 : extension d’une transaction à travers plusieurs composants'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Étape 2 : extension d’une transaction à travers plusieurs composants'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104321350"
---
# <a name="step-2-extending-a-transaction-across-components"></a><span data-ttu-id="b945e-103">Étape 2 : extension d’une transaction à travers les composants</span><span class="sxs-lookup"><span data-stu-id="b945e-103">Step 2: Extending a Transaction Across Components</span></span>

## <a name="objectives"></a><span data-ttu-id="b945e-104">Objectifs</span><span class="sxs-lookup"><span data-stu-id="b945e-104">Objectives</span></span>

<span data-ttu-id="b945e-105">Au cours de cette étape, vous allez découvrir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b945e-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="b945e-106">Workflow de transaction</span><span class="sxs-lookup"><span data-stu-id="b945e-106">Transaction flow</span></span>
-   <span data-ttu-id="b945e-107">Vote de plusieurs objets dans une transaction</span><span class="sxs-lookup"><span data-stu-id="b945e-107">How multiple objects vote in a transaction</span></span>

## <a name="description"></a><span data-ttu-id="b945e-108">Description</span><span class="sxs-lookup"><span data-stu-id="b945e-108">Description</span></span>

<span data-ttu-id="b945e-109">[Étape 1 : la création d’un composant transactionnel](step-1--creating-a-transactional-component.md) montre comment écrire un composant transactionnel simple qui met à jour les informations sur l’auteur dans la base de données pubs Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b945e-109">[Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) shows how to write a simple transactional component that updates author information in the Microsoft SQL Server Pubs database.</span></span> <span data-ttu-id="b945e-110">L’étape 2 montre ce qui se passe lorsqu’une transaction est étendue sur plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="b945e-110">Step 2 shows what happens when a transaction is extended across multiple components.</span></span>

<span data-ttu-id="b945e-111">En conservant le modèle de programmation COM+, `UpdateAuthorAddress` appelle un autre composant au cours de l’exécution de son travail.</span><span class="sxs-lookup"><span data-stu-id="b945e-111">In keeping with the COM+ programming model, `UpdateAuthorAddress` calls another component in the course of completing its work.</span></span> <span data-ttu-id="b945e-112">Le deuxième composant, `ValidateAuthorAddress` , valide l’adresse de l’auteur et retourne les résultats à son appelant, `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="b945e-112">The second component, `ValidateAuthorAddress`, validates the author's address and returns the results to its caller, `UpdateAuthorAddress`.</span></span>

<span data-ttu-id="b945e-113">Contrairement à son appelant, `ValidateAuthorAddress` ne nécessite pas de transaction, mais il peut toujours participer à la transaction de son appelant.</span><span class="sxs-lookup"><span data-stu-id="b945e-113">Unlike its caller, `ValidateAuthorAddress` does not require a transaction, but it can still participate in its caller's transaction.</span></span> <span data-ttu-id="b945e-114">Dans cette étape, sa valeur d’attribut de transaction est définie sur **pris en charge**, comme indiqué dans l’illustration suivante, qui étend la transaction existante au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="b945e-114">In this step, its transaction attribute value is set to **Supported**, as shown in the following illustration, which extends the existing transaction to the new object.</span></span>

![Diagramme qui montre l’extension de la transaction existante au nouvel objet.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

<span data-ttu-id="b945e-116">La valeur d’attribut **prise en charge** étend (ou transmet) une transaction existante uniquement lorsque l’appelant est transactionnel.</span><span class="sxs-lookup"><span data-stu-id="b945e-116">The **Supported** attribute value extends (or flows) an existing transaction only when the caller is transactional.</span></span> <span data-ttu-id="b945e-117">Lorsque `UpdateAuthorAddress` appelle `ValidateAuthorAddress` , com+ examine d’abord le contexte de l’appelant pour voir s’il est transactionnel.</span><span class="sxs-lookup"><span data-stu-id="b945e-117">When `UpdateAuthorAddress` calls `ValidateAuthorAddress`, COM+ first looks at the caller's context to see whether it is transactional.</span></span> <span data-ttu-id="b945e-118">COM+ examine ensuite les attributs de service qui sont définis sur `ValidateAuthorAddress` et attribue au nouvel objet le même identificateur de transaction affecté à l’objet appelant.</span><span class="sxs-lookup"><span data-stu-id="b945e-118">COM+ then looks at the service attributes that are set on `ValidateAuthorAddress` and assigns the new object the same transaction identifier that is assigned to the caller object.</span></span> <span data-ttu-id="b945e-119">Pour mieux comprendre ce processus, consultez [activation du contexte](context-activation.md).</span><span class="sxs-lookup"><span data-stu-id="b945e-119">To better understand this process, see [Context Activation](context-activation.md).</span></span>

<span data-ttu-id="b945e-120">Étant donné qu’ils partagent le même identificateur de transaction, les deux objets doivent effectuer leur travail avec succès ou COM+ abandonne la transaction (annulation des modifications apportées à la base de données pubs).</span><span class="sxs-lookup"><span data-stu-id="b945e-120">Because they share the same transaction identifier, both objects must complete their work successfully or COM+ aborts the transaction (undoing any changes made to the Pubs database).</span></span>

<span data-ttu-id="b945e-121">Tous les objets participant à une transaction votent pour valider ou abandonner la transaction.</span><span class="sxs-lookup"><span data-stu-id="b945e-121">All objects participating in a transaction vote to either commit or abort the transaction.</span></span> <span data-ttu-id="b945e-122">Le vote se produit explicitement lorsque vous incluez des instructions de vote dans votre code, comme le montre l’extraction suivante à partir de l’exemple de code Step 1, qui crée le `UpdateAuthorAddress` composant :</span><span class="sxs-lookup"><span data-stu-id="b945e-122">Voting occurs explicitly when you include voting instructions in your code, as shown in the following extraction from the Step 1 Sample Code, which creates the `UpdateAuthorAddress` component:</span></span>


```VB
  ' Everything works.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
```



<span data-ttu-id="b945e-123">Le vote se produit également implicitement, comme c’est le cas dans le `ValidateAuthorAddress` composant.</span><span class="sxs-lookup"><span data-stu-id="b945e-123">Voting also occurs implicitly, as is done in the `ValidateAuthorAddress` component.</span></span> <span data-ttu-id="b945e-124">À moins que l’objet ne déclare autrement, COM+ suppose qu’un objet a terminé son travail, mais qu’il n’est pas prêt à être désactivé.</span><span class="sxs-lookup"><span data-stu-id="b945e-124">Unless the object declares otherwise, COM+ assumes an object has completed its work successfully but that it is not ready to be deactivated.</span></span> <span data-ttu-id="b945e-125">COM+ effectue l’hypothèse suivante :</span><span class="sxs-lookup"><span data-stu-id="b945e-125">COM+ makes the following assumption:</span></span>


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



<span data-ttu-id="b945e-126">Lorsque `ValidateAuthorAddress` retourne à son appelant, com+ lit son vote comme une validation.</span><span class="sxs-lookup"><span data-stu-id="b945e-126">When `ValidateAuthorAddress` returns to its caller, COM+ reads its vote as a commit.</span></span> <span data-ttu-id="b945e-127">COM+ ne compte pas les votes tant qu’il n’a pas désactivé l’objet racine, qui est le premier objet dans la transaction dans le cas présent, l' `UpdateAuthorAddress` objet.</span><span class="sxs-lookup"><span data-stu-id="b945e-127">COM+ doesn't count the votes until it deactivates the root object, which is the first object in the transaction in this case, the `UpdateAuthorAddress` object.</span></span>

## <a name="sample-code"></a><span data-ttu-id="b945e-128">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="b945e-128">Sample code</span></span>

<span data-ttu-id="b945e-129">Le `ValidateAuthorAddress` composant effectue une vérification simple de l’adresse de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="b945e-129">The `ValidateAuthorAddress` component makes a simple check of the author's address.</span></span> <span data-ttu-id="b945e-130">Étant donné que `UpdateAuthorAddress` ne vote pas explicitement, com+ utilise les paramètres de vote par défaut.</span><span class="sxs-lookup"><span data-stu-id="b945e-130">Because `UpdateAuthorAddress` does not vote explicitly, COM+ uses the default vote settings.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating an author's address
'              (presumably right before updating that address in the
'              database).
'
'   Notes:   This component could be in a transaction or not; it doesn't 
'            matter because it doesn't touch any data in a database.
'
Public Function ValidateAuthorAddress( _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String) As Boolean
  ' Default is to validate unless something is found to be wrong.
  ValidateAuthorAddress = True
                                                  
  '  Invalidate authors who live in New York City
  '  and authors who live in Montana.
  '
  If strCity = "New York" And strState = "New York" Then
    ValidateAuthorAddress = False
  ElseIf strState = "Montana" Then
    ValidateAuthorAddress = False
  End If
  ' Done
End Function
```



## <a name="summary"></a><span data-ttu-id="b945e-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="b945e-131">Summary</span></span>

-   <span data-ttu-id="b945e-132">La définition de l’attribut de transaction d’un composant sur **pris en charge** peut entraîner la création du nouvel objet dans la transaction de l’objet appelant.</span><span class="sxs-lookup"><span data-stu-id="b945e-132">Setting a component's transaction attribute to **Supported** can result in the new object being created in the calling object's transaction.</span></span> <span data-ttu-id="b945e-133">COM+ examine le contexte de l’appelant pour déterminer l’état transactionnel du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="b945e-133">COM+ looks at the caller's context to determine the transactional status of the new object.</span></span> <span data-ttu-id="b945e-134">Si l’appelant est transactionnel, COM+ transmet la transaction au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="b945e-134">If the caller is transactional, COM+ flows the transaction to the new object.</span></span>
-   <span data-ttu-id="b945e-135">Tous les objets qui participent à la même transaction partagent un identificateur de transaction commun, que COM+ lit à partir du contexte de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b945e-135">All objects participating in the same transaction share a common transaction identifier, which COM+ reads from the object's context.</span></span>
-   <span data-ttu-id="b945e-136">Chaque objet dans une transaction est vote indépendamment des autres objets.</span><span class="sxs-lookup"><span data-stu-id="b945e-136">Each object in a transaction votes independently of other objects.</span></span> <span data-ttu-id="b945e-137">COM+ compte les votes lorsque l’objet racine est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b945e-137">COM+ counts the votes when the root object is deactivated.</span></span>
-   <span data-ttu-id="b945e-138">Vous pouvez basculer le vote de transaction d’un objet entre commit et Abort jusqu’à ce que COM+ désactive l’objet ou jusqu’à ce que COM+ désactive l’objet racine et mette fin à la transaction.</span><span class="sxs-lookup"><span data-stu-id="b945e-138">You can toggle an object's transaction vote between commit and abort until COM+ deactivates the object or until COM+ deactivates the root object and ends the transaction.</span></span> <span data-ttu-id="b945e-139">Seul le dernier paramètre de vote compte.</span><span class="sxs-lookup"><span data-stu-id="b945e-139">Only the last vote setting counts.</span></span> <span data-ttu-id="b945e-140">Les interfaces [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) et [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) fournissent des méthodes et produisent des résultats de vote similaires, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b945e-140">The [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) and [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interfaces provide methods and that produce similar voting results as shown in the following table.</span></span> <span data-ttu-id="b945e-141">Vous pouvez utiliser l’une ou l’autre des interfaces pour voter de manière explicite dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="b945e-141">You can use either interface to vote explicitly in a transaction.</span></span> 

    | <span data-ttu-id="b945e-142">Méthodes de combinaison [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="b945e-142">[**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) combination methods</span></span>                                                                                                                                                      | <span data-ttu-id="b945e-143">Méthode équivalente [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="b945e-143">[**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) equivalent method</span></span>       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="b945e-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**</span><span class="sxs-lookup"><span data-stu-id="b945e-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="b945e-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="b945e-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>  | [<span data-ttu-id="b945e-146">**SetComplete**</span><span class="sxs-lookup"><span data-stu-id="b945e-146">**SetComplete**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | <span data-ttu-id="b945e-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**</span><span class="sxs-lookup"><span data-stu-id="b945e-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="b945e-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="b945e-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/> | [<span data-ttu-id="b945e-149">**EnableCommit**</span><span class="sxs-lookup"><span data-stu-id="b945e-149">**EnableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | <span data-ttu-id="b945e-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**</span><span class="sxs-lookup"><span data-stu-id="b945e-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="b945e-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="b945e-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>   | [<span data-ttu-id="b945e-152">**SetAbort**</span><span class="sxs-lookup"><span data-stu-id="b945e-152">**SetAbort**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | <span data-ttu-id="b945e-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**</span><span class="sxs-lookup"><span data-stu-id="b945e-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="b945e-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="b945e-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/>  | [<span data-ttu-id="b945e-155">**DisableCommit**</span><span class="sxs-lookup"><span data-stu-id="b945e-155">**DisableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   <span data-ttu-id="b945e-156">COM+ définit le vote d’un objet sur l’équivalent de [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) , sauf si le composant vote explicitement.</span><span class="sxs-lookup"><span data-stu-id="b945e-156">COM+ sets an object's vote to the equivalent of [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) unless the component votes explicitly.</span></span>
-   <span data-ttu-id="b945e-157">Le vote de manière explicite peut réduire la durée globale de la transaction et libérer des verrous de ressource coûteux.</span><span class="sxs-lookup"><span data-stu-id="b945e-157">Voting explicitly can reduce the overall duration of the transaction and release expensive resource locks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b945e-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b945e-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b945e-159">Étape 1 : création d’un composant transactionnel</span><span class="sxs-lookup"><span data-stu-id="b945e-159">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="b945e-160">Étape 3 : réutilisation des composants</span><span class="sxs-lookup"><span data-stu-id="b945e-160">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="b945e-161">Activation du contexte</span><span class="sxs-lookup"><span data-stu-id="b945e-161">Context Activation</span></span>](context-activation.md)
</dt> <dt>

[<span data-ttu-id="b945e-162">Gestion des transactions automatiques dans COM+</span><span class="sxs-lookup"><span data-stu-id="b945e-162">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




