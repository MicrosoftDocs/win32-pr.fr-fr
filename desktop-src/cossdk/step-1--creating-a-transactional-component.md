---
description: 'Étape 1 : création d’un composant transactionnel'
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 'Étape 1 : création d’un composant transactionnel'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc378d85e628504e8724b765362b3397826f5e5
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104321349"
---
# <a name="step-1-creating-a-transactional-component"></a><span data-ttu-id="55f94-103">Étape 1 : création d’un composant transactionnel</span><span class="sxs-lookup"><span data-stu-id="55f94-103">Step 1: Creating a Transactional Component</span></span>

## <a name="objectives"></a><span data-ttu-id="55f94-104">Objectifs</span><span class="sxs-lookup"><span data-stu-id="55f94-104">Objectives</span></span>

<span data-ttu-id="55f94-105">Dans cette étape, vous allez apprendre ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="55f94-105">In this step, you will learn the following:</span></span>

-   <span data-ttu-id="55f94-106">Comment écrire un composant transactionnel dans Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="55f94-106">How to write a transactional component in Microsoft Visual Basic</span></span>
-   <span data-ttu-id="55f94-107">Les paramètres par défaut des services COM+</span><span class="sxs-lookup"><span data-stu-id="55f94-107">What the default settings for COM+ services are</span></span>
-   <span data-ttu-id="55f94-108">Comment configurer les services COM+</span><span class="sxs-lookup"><span data-stu-id="55f94-108">How to configure COM+ services</span></span>

## <a name="description"></a><span data-ttu-id="55f94-109">Description</span><span class="sxs-lookup"><span data-stu-id="55f94-109">Description</span></span>

<span data-ttu-id="55f94-110">Le composant UpdateAuthorAddress, le composant à créer dans cette section, met à jour l’adresse d’un auteur existant dans la base de données pubs.</span><span class="sxs-lookup"><span data-stu-id="55f94-110">The UpdateAuthorAddress component, the component to be created in this section, updates the address of an existing author in the Pubs database.</span></span> <span data-ttu-id="55f94-111">La base de données pubs est un exemple de base de données fourni avec Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="55f94-111">The Pubs database is a sample database that ships with Microsoft SQL Server.</span></span> <span data-ttu-id="55f94-112">Il contient des informations de publication telles que des noms d’auteur, des adresses et des titres de livres.</span><span class="sxs-lookup"><span data-stu-id="55f94-112">It contains publishing information such as author names, addresses, and book titles.</span></span>

> [!Note]  
> <span data-ttu-id="55f94-113">Pubs est le magasin de données utilisé dans ce premier.</span><span class="sxs-lookup"><span data-stu-id="55f94-113">Pubs is the data store that is used throughout this primer.</span></span>

 

<span data-ttu-id="55f94-114">Comme UpdateAuthorAddress met à jour un magasin de données, il est recommandé d’inclure le travail dans une transaction, comme indiqué dans l’illustration suivante, de sorte que lorsqu’un client appelle le composant, COM+ démarre automatiquement une transaction et inscrit la base de données (Resource Manager) dans cette transaction.</span><span class="sxs-lookup"><span data-stu-id="55f94-114">Because UpdateAuthorAddress updates a data store, it is advisable to include the work in a transaction, as shown in the following illustration, so that when a client calls the component, COM+ automatically starts a transaction and enlists the database (resource manager) in that transaction.</span></span> <span data-ttu-id="55f94-115">(Pour plus d’informations sur les transactions dans COM+, consultez [transactions com+](com--transactions.md).)</span><span class="sxs-lookup"><span data-stu-id="55f94-115">(For detailed information about transactions in COM+, see [COM+ Transactions](com--transactions.md).)</span></span>

![Diagramme illustrant une transaction COM+ avec UpdateAuthorAddress.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

<span data-ttu-id="55f94-117">Pour faire de UpdateAuthorAddress un composant transactionnel, les étapes suivantes sont requises :</span><span class="sxs-lookup"><span data-stu-id="55f94-117">To make UpdateAuthorAddress a transactional component, the following steps are required:</span></span>

1.  <span data-ttu-id="55f94-118">Le composant doit être écrit.</span><span class="sxs-lookup"><span data-stu-id="55f94-118">The component must be written.</span></span> <span data-ttu-id="55f94-119">Pour une protection supplémentaire, une sous-routine est ajoutée, en vérifiant que COM+ a créé l’objet dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="55f94-119">For extra protection, a subroutine is added, verifying that COM+ created the object in a transaction.</span></span> <span data-ttu-id="55f94-120">En outre, la gestion des erreurs de base est incluse dans le composant pour simplifier la récupération des erreurs.</span><span class="sxs-lookup"><span data-stu-id="55f94-120">Also, basic error handling is included in the component to simplify error recovery.</span></span> <span data-ttu-id="55f94-121">La vérification des transactions et la gestion des erreurs améliorent la fiabilité du composant.</span><span class="sxs-lookup"><span data-stu-id="55f94-121">Transaction verification and error handling enhance the reliability of the component.</span></span> <span data-ttu-id="55f94-122">(Pour obtenir une liste complète du composant UpdateAuthorAddress, consultez l’exemple de code de l’étape 1.)</span><span class="sxs-lookup"><span data-stu-id="55f94-122">(See Step 1 Sample Code for a complete listing of the UpdateAuthorAddress component.)</span></span>
2.  <span data-ttu-id="55f94-123">Après l’ajout du composant à une application COM+ et l’installation de l’application, l’attribut de transaction doit être défini sur **obligatoire**, ce qui garantit que com+ crée chaque objet UpdateAuthorAddress dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="55f94-123">After adding the component to a COM+ application and installing the application, the transaction attribute must be set to **Required**, which guarantees that COM+ creates each UpdateAuthorAddress object in a transaction.</span></span> <span data-ttu-id="55f94-124">Pour obtenir des instructions sur la façon de définir l’attribut de transaction pour un composant, consultez [définition de l’attribut de transaction](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="55f94-124">For instructions on how to set the transaction attribute for a component, see [Setting the Transaction Attribute](setting-the-transaction-attribute.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="55f94-125">La définition de l’attribut de transaction sur un composant définit la manière dont COM+ crée chaque objet en ce qui concerne les transactions.</span><span class="sxs-lookup"><span data-stu-id="55f94-125">Setting the transaction attribute on a component defines how COM+ creates each object with regard to transactions.</span></span> <span data-ttu-id="55f94-126">Les valeurs d’attribut de transaction sont **ignorées**, **non prises en** charge, **prises en charge**, **obligatoires** et **nouvelles**.</span><span class="sxs-lookup"><span data-stu-id="55f94-126">Transaction attribute values are **Ignored**, **Not Supported**, **Supported**, **Required**, and **Requires New**.</span></span> <span data-ttu-id="55f94-127">La valeur **requise** n’est pas l’une des valeurs d’attribut par défaut d’un composant.</span><span class="sxs-lookup"><span data-stu-id="55f94-127">The **Required** value is not one of a component's default attribute values.</span></span>

     

<span data-ttu-id="55f94-128">COM+ lie le service de transactions avec l’activation juste-à-temps (JIT) et l’accès concurrentiel.</span><span class="sxs-lookup"><span data-stu-id="55f94-128">COM+ binds the transaction service with just-in-time (JIT) activation and concurrency.</span></span> <span data-ttu-id="55f94-129">Lorsque vous déclarez un composant comme étant transactionnel, COM+ applique également l’activation JIT et la protection d’accès concurrentiel (synchronisation).</span><span class="sxs-lookup"><span data-stu-id="55f94-129">When you declare a component to be transactional, COM+ also enforces JIT activation and concurrency protection (synchronization).</span></span>

## <a name="sample-code"></a><span data-ttu-id="55f94-130">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="55f94-130">Sample code</span></span>

<span data-ttu-id="55f94-131">Le composant UpdateAuthorAddress ouvre une connexion à la base de données pubs, ce qui permet à l’utilisateur de modifier le nom, l’adresse ou le statut du contrat d’un auteur.</span><span class="sxs-lookup"><span data-stu-id="55f94-131">The UpdateAuthorAddress component opens a connection to the Pubs database, allowing the user to modify an author's name, address, or contract status.</span></span> <span data-ttu-id="55f94-132">Il appelle également un deuxième composant, qui est abordé à l' [étape 2 : extension d’une transaction sur plusieurs composants](step-2--extending-a-transaction-across-multiple-components.md).</span><span class="sxs-lookup"><span data-stu-id="55f94-132">It also calls a second component, which is discussed in [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md).</span></span>

<span data-ttu-id="55f94-133">Pour utiliser le code suivant dans un projet Microsoft Visual Basic, ouvrez un nouveau projet ActiveX.dll et ajoutez des références à la bibliothèque Microsoft ActiveX Data Objects et à la bibliothèque de types services COM+.</span><span class="sxs-lookup"><span data-stu-id="55f94-133">To use the following code in a Microsoft Visual Basic project, open a new ActiveX.dll project and add references to the Microsoft ActiveX Data Objects Library and the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="55f94-134">L’exemple de code de ce premier plan est à des fins d’illustration et peut ne pas être le plus efficace pour la mise en lots et la production réelles.</span><span class="sxs-lookup"><span data-stu-id="55f94-134">The sample code in this primer is for purposes of illustration and may not be the most efficient for actual staging and production.</span></span>

 


```VB
Option Explicit
'
'  Purpose:   This class is used for updating an author's address.
'
'  Notes:     IMPT:  This component implicitly assumes that it will 
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'

'----------------------------------------------------------
'  VerifyInTxn subroutine
'      Verifies that this component is in a transaction.
'      Throws an error if it is not.
'
Private Sub VerifyInTxn()
  If Not GetObjectContext.IsInTransaction Then
    ' Transactions turned off. 
    Err.Raise 99999, "This component", "I need a transaction!"
  End If
  ' Component is in a transaction.
End Sub

'----------------------------------------------------------
'  UpdateAuthorAddress subroutine
'      Procedure to update an author's address.
'
Public Sub UpdateAuthorAddress( _
                        ByVal strAuthorID As String, _
                        ByVal strPhone As String, _
                       ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String)
  ' Handle any errors.
  On Error GoTo UnexpectedError
  
  ' Verify that component is in a transaction.
  VerifyInTxn
  
  ' Get object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext
  
  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext
  
  ' Validate the new address information.
  ' The ValidateAuthorAddress function is described in Step 2.
  Dim oValidateAuthAddr As Object
  Dim bValidAddr As Boolean
  Set oValidateAuthAddr = _
    CreateObject("ComplusPrimer.ValidateAuthorAddress") 
  bValidAddr = oValidateAuthAddr.ValidateAuthorAddress( _
    strAddress, strCity, strState, strZip)
  If Not bValidAddr Then
    Err.Raise 99999, "The UpdateAuthorAddress component", _
      "The address of the author is incorrect!"
  End If
  
  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Execute the query.
  conn.Execute "update authors set phone= '" & strPhone & "'" & _
               " set address= '" & strAddress & "'" & _
               " set city= '" & strCity & "'" & _
               " set state= '" & strState & "'" & _
               " set zip= '" & strZip & "'" & _
               " where au_id = '" & strAuthorID & "'"
               
  ' Close the connection.
  conn.Close
  
  ' Get rid of the connection.
  Set conn = Nothing
                 
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
End Sub

```



## <a name="summary"></a><span data-ttu-id="55f94-135">Résumé</span><span class="sxs-lookup"><span data-stu-id="55f94-135">Summary</span></span>

-   <span data-ttu-id="55f94-136">COM+ affecte des valeurs d’attribut par défaut.</span><span class="sxs-lookup"><span data-stu-id="55f94-136">COM+ assigns default attribute values.</span></span> <span data-ttu-id="55f94-137">Vous pouvez reconfigurer la plupart des attributs de service.</span><span class="sxs-lookup"><span data-stu-id="55f94-137">You can reconfigure most service attributes.</span></span>
-   <span data-ttu-id="55f94-138">L’affectation de la valeur **obligatoire** à l’attribut de transaction d’un composant garantit que com+ doit créer chaque instance de ce composant dans une transaction, mais ne démarre pas nécessairement une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="55f94-138">Setting a component's transaction attribute to **Required** guarantees that COM+ must create each instance of that component in a transaction but doesn't necessarily start a new transaction.</span></span>
-   <span data-ttu-id="55f94-139">La vérification de la présence d’une transaction confirme que la valeur de l’attribut de transaction du composant n’a pas été réinitialisée par inadvertance à une valeur non transactionnelle, telle que **Ignorer** ou **non prise en charge**.</span><span class="sxs-lookup"><span data-stu-id="55f94-139">Verifying the presence of a transaction confirms that the component's transaction attribute value wasn't inadvertently reset to a non-transactional value, such as **Ignore** or **Not Supported**.</span></span>
-   <span data-ttu-id="55f94-140">La gestion des erreurs rend votre composant plus fiable et plus facile à dépanner.</span><span class="sxs-lookup"><span data-stu-id="55f94-140">Handling errors makes your component more reliable and easier to troubleshoot.</span></span>
-   <span data-ttu-id="55f94-141">COM+ applique [l’activation JIT](com--just-in-time-activation.md) et les services de [protection d’accès concurrentiel](com--synchronization.md) pour les composants transactionnels.</span><span class="sxs-lookup"><span data-stu-id="55f94-141">COM+ enforces [JIT activation](com--just-in-time-activation.md) and [concurrency protection](com--synchronization.md) services for transactional components.</span></span>
-   <span data-ttu-id="55f94-142">La fermeture de la connexion de base de données lorsque vous avez terminé, permet à un autre composant de la même transaction de réutiliser la connexion à partir du pool de connexions.</span><span class="sxs-lookup"><span data-stu-id="55f94-142">Closing the database connection when you are done with it allows another component in the same transaction to reuse the connection from the connection pool.</span></span> <span data-ttu-id="55f94-143">(Le regroupement de connexions ne doit pas être confondu avec le [regroupement d’objets](com--object-pooling.md).)</span><span class="sxs-lookup"><span data-stu-id="55f94-143">(Connection pooling should not be confused with [object pooling](com--object-pooling.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="55f94-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55f94-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55f94-145">Étape 2 : extension d’une transaction à travers plusieurs composants</span><span class="sxs-lookup"><span data-stu-id="55f94-145">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="55f94-146">Étape 3 : réutilisation des composants</span><span class="sxs-lookup"><span data-stu-id="55f94-146">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="55f94-147">Activation juste-à-temps de COM+</span><span class="sxs-lookup"><span data-stu-id="55f94-147">COM+ Just-in-Time Activation</span></span>](com--just-in-time-activation.md)
</dt> <dt>

[<span data-ttu-id="55f94-148">Synchronisation COM+</span><span class="sxs-lookup"><span data-stu-id="55f94-148">COM+ Synchronization</span></span>](com--synchronization.md)
</dt> <dt>

[<span data-ttu-id="55f94-149">Configuration des transactions</span><span class="sxs-lookup"><span data-stu-id="55f94-149">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="55f94-150">Création d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="55f94-150">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="55f94-151">Définition de l’attribut de transaction</span><span class="sxs-lookup"><span data-stu-id="55f94-151">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



