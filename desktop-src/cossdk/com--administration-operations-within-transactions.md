---
description: Opérations d’administration COM+ dans les transactions
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: Opérations d’administration COM+ dans les transactions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21612ffec1b9f082dc6a91861882a71f18fb07be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749093"
---
# <a name="com-administration-operations-within-transactions"></a><span data-ttu-id="b23d8-103">Opérations d’administration COM+ dans les transactions</span><span class="sxs-lookup"><span data-stu-id="b23d8-103">COM+ Administration Operations Within Transactions</span></span>

<span data-ttu-id="b23d8-104">La base de données d’inscription COM+ (RegDB) est un gestionnaire de ressources transactionnelles qui peut participer à des transactions COM+.</span><span class="sxs-lookup"><span data-stu-id="b23d8-104">The COM+ registration database (RegDB) is a transacted resource manager that can participate in COM+ transactions.</span></span> <span data-ttu-id="b23d8-105">Cela vous permet d’effectuer des opérations d’administration au sein d’une transaction et de faire en sorte que toutes les modifications de configuration soient validées ou abandonnées en tant qu’opération atomique, même sur plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="b23d8-105">This enables you to perform administration operations within a transaction and have all configuration changes committed or aborted as an atomic operation, even across multiple computers.</span></span> <span data-ttu-id="b23d8-106">Dans certains cas, il peut être très bénéfique pour cela, bien qu’il y ait un comportement d’isolation et de blocage que vous devez prendre en compte, et que l’exécution de tâches d’administration au sein des transactions implique de légères modifications du modèle de programmation d’administration normal.</span><span class="sxs-lookup"><span data-stu-id="b23d8-106">In some circumstances, it can be very beneficial to do this, although there is isolation and blocking behavior that you should take into account, and performing administration tasks within transactions does involve slight changes to the normal administration programming model.</span></span>

## <a name="benefits-of-doing-administration-operations-within-transactions"></a><span data-ttu-id="b23d8-107">Avantages de l’utilisation des opérations d’administration au sein des transactions</span><span class="sxs-lookup"><span data-stu-id="b23d8-107">Benefits of Doing Administration Operations Within Transactions</span></span>

-   <span data-ttu-id="b23d8-108">**Cohérence des données :** Les opérations d’administration effectuées au sein d’une transaction sont validées ou annulées dans leur ensemble, bien qu’il existe des ressources de catalogue COM+ non transactionnelles pour lesquelles cela peut ne pas être le cas.</span><span class="sxs-lookup"><span data-stu-id="b23d8-108">**Consistency of data—** Administration operations performed within a transaction are committed or aborted as a whole, although there are some non-transactional COM+ catalog resources for which this may not be the case.</span></span> <span data-ttu-id="b23d8-109">(Voir les ressources de catalogue COM+ non transactionnelles ci-dessous.)</span><span class="sxs-lookup"><span data-stu-id="b23d8-109">(See Non-Transactional COM+ Catalog Resources below.)</span></span>
-   <span data-ttu-id="b23d8-110">**Déploiement cohérent sur plusieurs ordinateurs :** Si vous déployez des applications COM+ sur plusieurs serveurs, vous pouvez vous assurer que tous les serveurs sont conservés avec des configurations identiques.</span><span class="sxs-lookup"><span data-stu-id="b23d8-110">**Consistent deployment across multiple machines—** If you are deploying COM+ applications across multiple servers, you can guarantee that all servers are left with identical configurations.</span></span>
-   <span data-ttu-id="b23d8-111">**Évolutivité et performances :** Lorsque vous effectuez plusieurs opérations au sein d’une transaction, toutes les écritures dans RegDB sont exécutées en même temps.</span><span class="sxs-lookup"><span data-stu-id="b23d8-111">**Scaling and performance—** When you do multiple operations within a transaction, all writes to RegDB are performed at once.</span></span> <span data-ttu-id="b23d8-112">Les écritures persistantes dans RegDB sont une opération relativement coûteuse ; Si vous effectuez de nombreuses écritures dans RegDB, vous pouvez obtenir un gain de performances considérable en effectuant toutes les opérations à la fois au lieu de les appeler à chaque fois que vous appelez [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span><span class="sxs-lookup"><span data-stu-id="b23d8-112">Persisted writes to RegDB are a relatively expensive operation; if you are making many writes to RegDB, you can get a big performance benefit from doing them all at once instead of every time you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span></span>

## <a name="isolation-behavior-of-regdb"></a><span data-ttu-id="b23d8-113">Comportement d’isolation de RegDB</span><span class="sxs-lookup"><span data-stu-id="b23d8-113">Isolation Behavior of RegDB</span></span>

<span data-ttu-id="b23d8-114">Pour garantir une cohérence correcte des données et des transactions sérialisables, RegDB applique un comportement de blocage et d’isolation particulier lorsque les opérations d’administration sont effectuées au sein des transactions.</span><span class="sxs-lookup"><span data-stu-id="b23d8-114">To ensure proper data consistency and serializable transactions, RegDB enforces particular blocking and isolation behavior when administration operations are being performed within transactions.</span></span>

<span data-ttu-id="b23d8-115">Chaque fois qu’un composant qui effectue son travail dans une transaction appelle une méthode qui entraîne une écriture dans le catalogue COM+ (par exemple, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)ou [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)), un verrou de writer est pris sur le code du serveur de catalogue COM+ qui bloquera les autres enregistreurs à partir du moment où la transaction en cours est validée ou abandonnée.</span><span class="sxs-lookup"><span data-stu-id="b23d8-115">Whenever a component that is doing work within a transaction calls any method that will cause a write to the COM+ catalog—such as [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication), or [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)—a writer lock is taken on COM+ catalog server code that will block any other writers from coming in until the current transaction commits or aborts.</span></span> <span data-ttu-id="b23d8-116">Autrement dit, les enregistreurs peuvent se trouver dans uniquement s’ils ont l’affinité de transaction correcte et participent à la transaction actuelle.</span><span class="sxs-lookup"><span data-stu-id="b23d8-116">That is, writers can come in only if they have the correct transaction affinity and are participating in the current transaction.</span></span>

<span data-ttu-id="b23d8-117">Les lecteurs ne sont pas bloqués.</span><span class="sxs-lookup"><span data-stu-id="b23d8-117">Readers are not blocked.</span></span> <span data-ttu-id="b23d8-118">Toutefois, les données que les lecteurs voient ne reflètent pas les modifications intermédiaires effectuées dans la transaction tant que la transaction n’est pas réellement validée.</span><span class="sxs-lookup"><span data-stu-id="b23d8-118">However, the data that readers see does not reflect any interim changes made within the transaction until that transaction actually commits.</span></span> <span data-ttu-id="b23d8-119">Tous les composants qui participent à cette transaction voient les États de données intermédiaires lorsqu’ils lisent les données, mais tous les composants en dehors de la transaction voient ces modifications uniquement après la fin de la transaction.</span><span class="sxs-lookup"><span data-stu-id="b23d8-119">Any components participating in that transaction sees interim data states when they read data, but all components outside the transaction see those changes only after the transaction has completed.</span></span>

## <a name="savechanges-behavior"></a><span data-ttu-id="b23d8-120">Comportement SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b23d8-120">SaveChanges Behavior</span></span>

<span data-ttu-id="b23d8-121">Pour obtenir le comportement d’isolation décrit ci-dessus, RegDB fournit efficacement un cache qui est traité par les composants de la transaction.</span><span class="sxs-lookup"><span data-stu-id="b23d8-121">To achieve the isolation behavior described above, RegDB effectively provides a cache that is acted on by components within the transaction.</span></span> <span data-ttu-id="b23d8-122">Cela modifie le comportement de la méthode [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .</span><span class="sxs-lookup"><span data-stu-id="b23d8-122">This changes the behavior of the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method.</span></span>

<span data-ttu-id="b23d8-123">Normalement, sans la présence d’une transaction, toutes les modifications en attente sont écrites dans le catalogue lorsque vous appelez [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), et **SaveChanges** ne retourne pas tant que toutes les écritures ne sont pas terminées.</span><span class="sxs-lookup"><span data-stu-id="b23d8-123">Normally, without the presence of a transaction, any pending changes are written to the catalog when you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), and **SaveChanges** doesn't return until all writes are completed.</span></span> <span data-ttu-id="b23d8-124">Cela garantit que si un appel à **SaveChanges** est retourné avec succès, vous pouvez appeler [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) et activer l’application avec les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="b23d8-124">This guarantees that if a call to **SaveChanges** returns successfully, you can call [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) and it will activate the application with fresh data.</span></span>

<span data-ttu-id="b23d8-125">Toutefois, au sein d’une transaction, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) affecte uniquement le cache, pas le RegDB lui-même, et **SaveChanges** retourne immédiatement si toutes les modifications ont été validées de manière transactionnelle sur RegDB.</span><span class="sxs-lookup"><span data-stu-id="b23d8-125">However, within a transaction, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) affects only the cache, not the RegDB itself, and **SaveChanges** returns immediately whether all changes have been transactionally committed to RegDB.</span></span> <span data-ttu-id="b23d8-126">Il n’y a aucune garantie que [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) utilise des données actualisées après le retour de **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="b23d8-126">There is no guarantee that [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) is using fresh data subsequent to **SaveChanges** returning.</span></span> <span data-ttu-id="b23d8-127">Si vous devez appeler **StartApplication** dans ce contexte, il est recommandé d’attendre un certain temps avant de le faire.</span><span class="sxs-lookup"><span data-stu-id="b23d8-127">If you need to call **StartApplication** in this context, it is advisable to wait for some period of time before doing so.</span></span>

## <a name="transaction-time-out-period"></a><span data-ttu-id="b23d8-128">Période de Time-Out de transaction</span><span class="sxs-lookup"><span data-stu-id="b23d8-128">Transaction Time-Out Period</span></span>

<span data-ttu-id="b23d8-129">Si vous effectuez de nombreuses opérations d’administration au sein d’une transaction, il peut s’agir d’une transaction de longue durée.</span><span class="sxs-lookup"><span data-stu-id="b23d8-129">If you are doing numerous administration operations within a transaction, it may be a long running transaction.</span></span> <span data-ttu-id="b23d8-130">Dans ce cas, la valeur du délai d’attente de la transaction peut être un problème.</span><span class="sxs-lookup"><span data-stu-id="b23d8-130">In this case, the transaction time-out value can be an issue.</span></span> <span data-ttu-id="b23d8-131">Cela est déterminé par la valeur du délai d’expiration de la transaction définie pour le composant qui lance la transaction ou par le paramètre de délai d’attente à l’ensemble de l’ordinateur pour l’ordinateur sur lequel ce composant s’exécute.</span><span class="sxs-lookup"><span data-stu-id="b23d8-131">This is determined either by the transaction time-out value set for the component initiating the transaction or by the machine-wide time-out setting for the machine where that component is running.</span></span> <span data-ttu-id="b23d8-132">Si vous effectuez de nombreuses opérations au sein d’une transaction, il est recommandé de définir le délai d’expiration de transaction approprié sur une valeur suffisamment longue et, si nécessaire, de restaurer le paramètre d’origine une fois que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="b23d8-132">If you are doing numerous operations within a transaction, it is advisable to set the appropriate transaction time-out period to a sufficiently long value and, if necessary, to restore the original setting when you are finished.</span></span>

## <a name="non-transactional-com-catalog-resources"></a><span data-ttu-id="b23d8-133">Ressources de catalogue COM+ non transactionnelles</span><span class="sxs-lookup"><span data-stu-id="b23d8-133">Non-Transactional COM+ Catalog Resources</span></span>

<span data-ttu-id="b23d8-134">Le registre, le système de fichiers et le Windows Installer (MSI) sont des ressources de catalogue COM+ qui ne sont pas transactionnelles.</span><span class="sxs-lookup"><span data-stu-id="b23d8-134">The registry, the file system, and Windows Installer (MSI) are COM+ catalog resources that are not transactional.</span></span>

> [!Note]  
> <span data-ttu-id="b23d8-135">En cas d’erreur qui interrompt une transaction, les modifications apportées à ces ressources peuvent ne pas être restaurées.</span><span class="sxs-lookup"><span data-stu-id="b23d8-135">If there is an error that aborts a transaction, changes to these resources may not be rolled back.</span></span>

 

<span data-ttu-id="b23d8-136">En cas d’erreur lors de l’installation d’une application COM+ existante à partir d’un fichier. msi, l’application n’apparaît pas dans le composant logiciel enfichable Services de composants, mais elle peut apparaître dans Ajout/suppression de programmes. dans ce cas, vous devez la supprimer manuellement.</span><span class="sxs-lookup"><span data-stu-id="b23d8-136">If there is an error while installing an existing COM+ application from an .msi file, the application doesn't appear in the Component Services snap-in but it might appear in Add/Remove programs, in which case you need to manually remove it.</span></span>

## <a name="recovering-in-the-event-of-system-hangs"></a><span data-ttu-id="b23d8-137">Récupération en cas de blocages du système</span><span class="sxs-lookup"><span data-stu-id="b23d8-137">Recovering in the Event of System Hangs</span></span>

<span data-ttu-id="b23d8-138">Si un composant qui effectue des opérations d’administration au sein d’une transaction devait se bloquer pendant qu’il détient un verrou de writer sur le code du serveur de catalogue, il empêche tout autre utilisateur d’apporter des modifications au catalogue.</span><span class="sxs-lookup"><span data-stu-id="b23d8-138">If a component doing administration operations within a transaction were to hang while it holds a writer lock on the catalog server code, it would block everyone else from making any changes to the catalog.</span></span> <span data-ttu-id="b23d8-139">Si cela se produit, vous pouvez effacer le verrou sur le catalogue en arrêtant et en redémarrant l’application système.</span><span class="sxs-lookup"><span data-stu-id="b23d8-139">Should this happen, you can clear the lock on the catalog by shutting down and restarting the System application.</span></span>

## <a name="scripting-with-a-transactioncontext-object"></a><span data-ttu-id="b23d8-140">Écriture de scripts avec un objet TransactionContext</span><span class="sxs-lookup"><span data-stu-id="b23d8-140">Scripting with a TransactionContext Object</span></span>

<span data-ttu-id="b23d8-141">Un moyen simple d’effectuer des opérations d’administration au sein des transactions consiste à utiliser un objet [**transactionContext**](transactioncontext.md) pour contrôler la transaction.</span><span class="sxs-lookup"><span data-stu-id="b23d8-141">A simple way to do administration operations within transactions is to use a [**TransactionContext**](transactioncontext.md) object to control the transaction.</span></span> <span data-ttu-id="b23d8-142">Par exemple, le script de Visual Basic suivant montre comment ajouter de manière transactionnelle deux nouvelles applications afin que les deux applications ou aucune des applications soient créées :</span><span class="sxs-lookup"><span data-stu-id="b23d8-142">For example, the following Visual Basic script demonstrates how to transactionally add two new applications so that either both applications or neither application is created:</span></span>


```VB
Dim txctx
Dim cat
Dim apps
Dim app1
Dim app2
  
WScript.Echo "Starting"
Set txctx = CreateObject("TxCtx.TransactionContext")
Set cat = txctx.CreateInstance("COMAdmin.COMAdminCatalog")
Set apps = cat.GetCollection("Applications")
Set app1 = apps.Add
app1.Value("Name") = "Test App #1"
apps.SaveChanges
Set app2 = apps.Add
app2.Value("Name") = "Test App #2"
apps.SaveChanges
  
WScript.Echo "Ending"
txctx.Commit

```



## <a name="related-topics"></a><span data-ttu-id="b23d8-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b23d8-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b23d8-144">Gestion des erreurs d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="b23d8-144">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="b23d8-145">Exemple d’introduction utilisant le catalogue d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="b23d8-145">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="b23d8-146">Vue d’ensemble des objets comadmin</span><span class="sxs-lookup"><span data-stu-id="b23d8-146">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="b23d8-147">Récupération des regroupements sur le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="b23d8-147">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="b23d8-148">Définition des propriétés et enregistrement des modifications dans le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="b23d8-148">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



