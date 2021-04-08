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
# <a name="com-administration-operations-within-transactions"></a>Opérations d’administration COM+ dans les transactions

La base de données d’inscription COM+ (RegDB) est un gestionnaire de ressources transactionnelles qui peut participer à des transactions COM+. Cela vous permet d’effectuer des opérations d’administration au sein d’une transaction et de faire en sorte que toutes les modifications de configuration soient validées ou abandonnées en tant qu’opération atomique, même sur plusieurs ordinateurs. Dans certains cas, il peut être très bénéfique pour cela, bien qu’il y ait un comportement d’isolation et de blocage que vous devez prendre en compte, et que l’exécution de tâches d’administration au sein des transactions implique de légères modifications du modèle de programmation d’administration normal.

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>Avantages de l’utilisation des opérations d’administration au sein des transactions

-   **Cohérence des données :** Les opérations d’administration effectuées au sein d’une transaction sont validées ou annulées dans leur ensemble, bien qu’il existe des ressources de catalogue COM+ non transactionnelles pour lesquelles cela peut ne pas être le cas. (Voir les ressources de catalogue COM+ non transactionnelles ci-dessous.)
-   **Déploiement cohérent sur plusieurs ordinateurs :** Si vous déployez des applications COM+ sur plusieurs serveurs, vous pouvez vous assurer que tous les serveurs sont conservés avec des configurations identiques.
-   **Évolutivité et performances :** Lorsque vous effectuez plusieurs opérations au sein d’une transaction, toutes les écritures dans RegDB sont exécutées en même temps. Les écritures persistantes dans RegDB sont une opération relativement coûteuse ; Si vous effectuez de nombreuses écritures dans RegDB, vous pouvez obtenir un gain de performances considérable en effectuant toutes les opérations à la fois au lieu de les appeler à chaque fois que vous appelez [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).

## <a name="isolation-behavior-of-regdb"></a>Comportement d’isolation de RegDB

Pour garantir une cohérence correcte des données et des transactions sérialisables, RegDB applique un comportement de blocage et d’isolation particulier lorsque les opérations d’administration sont effectuées au sein des transactions.

Chaque fois qu’un composant qui effectue son travail dans une transaction appelle une méthode qui entraîne une écriture dans le catalogue COM+ (par exemple, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)ou [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)), un verrou de writer est pris sur le code du serveur de catalogue COM+ qui bloquera les autres enregistreurs à partir du moment où la transaction en cours est validée ou abandonnée. Autrement dit, les enregistreurs peuvent se trouver dans uniquement s’ils ont l’affinité de transaction correcte et participent à la transaction actuelle.

Les lecteurs ne sont pas bloqués. Toutefois, les données que les lecteurs voient ne reflètent pas les modifications intermédiaires effectuées dans la transaction tant que la transaction n’est pas réellement validée. Tous les composants qui participent à cette transaction voient les États de données intermédiaires lorsqu’ils lisent les données, mais tous les composants en dehors de la transaction voient ces modifications uniquement après la fin de la transaction.

## <a name="savechanges-behavior"></a>Comportement SaveChanges

Pour obtenir le comportement d’isolation décrit ci-dessus, RegDB fournit efficacement un cache qui est traité par les composants de la transaction. Cela modifie le comportement de la méthode [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .

Normalement, sans la présence d’une transaction, toutes les modifications en attente sont écrites dans le catalogue lorsque vous appelez [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), et **SaveChanges** ne retourne pas tant que toutes les écritures ne sont pas terminées. Cela garantit que si un appel à **SaveChanges** est retourné avec succès, vous pouvez appeler [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) et activer l’application avec les nouvelles données.

Toutefois, au sein d’une transaction, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) affecte uniquement le cache, pas le RegDB lui-même, et **SaveChanges** retourne immédiatement si toutes les modifications ont été validées de manière transactionnelle sur RegDB. Il n’y a aucune garantie que [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) utilise des données actualisées après le retour de **SaveChanges** . Si vous devez appeler **StartApplication** dans ce contexte, il est recommandé d’attendre un certain temps avant de le faire.

## <a name="transaction-time-out-period"></a>Période de Time-Out de transaction

Si vous effectuez de nombreuses opérations d’administration au sein d’une transaction, il peut s’agir d’une transaction de longue durée. Dans ce cas, la valeur du délai d’attente de la transaction peut être un problème. Cela est déterminé par la valeur du délai d’expiration de la transaction définie pour le composant qui lance la transaction ou par le paramètre de délai d’attente à l’ensemble de l’ordinateur pour l’ordinateur sur lequel ce composant s’exécute. Si vous effectuez de nombreuses opérations au sein d’une transaction, il est recommandé de définir le délai d’expiration de transaction approprié sur une valeur suffisamment longue et, si nécessaire, de restaurer le paramètre d’origine une fois que vous avez terminé.

## <a name="non-transactional-com-catalog-resources"></a>Ressources de catalogue COM+ non transactionnelles

Le registre, le système de fichiers et le Windows Installer (MSI) sont des ressources de catalogue COM+ qui ne sont pas transactionnelles.

> [!Note]  
> En cas d’erreur qui interrompt une transaction, les modifications apportées à ces ressources peuvent ne pas être restaurées.

 

En cas d’erreur lors de l’installation d’une application COM+ existante à partir d’un fichier. msi, l’application n’apparaît pas dans le composant logiciel enfichable Services de composants, mais elle peut apparaître dans Ajout/suppression de programmes. dans ce cas, vous devez la supprimer manuellement.

## <a name="recovering-in-the-event-of-system-hangs"></a>Récupération en cas de blocages du système

Si un composant qui effectue des opérations d’administration au sein d’une transaction devait se bloquer pendant qu’il détient un verrou de writer sur le code du serveur de catalogue, il empêche tout autre utilisateur d’apporter des modifications au catalogue. Si cela se produit, vous pouvez effacer le verrou sur le catalogue en arrêtant et en redémarrant l’application système.

## <a name="scripting-with-a-transactioncontext-object"></a>Écriture de scripts avec un objet TransactionContext

Un moyen simple d’effectuer des opérations d’administration au sein des transactions consiste à utiliser un objet [**transactionContext**](transactioncontext.md) pour contrôler la transaction. Par exemple, le script de Visual Basic suivant montre comment ajouter de manière transactionnelle deux nouvelles applications afin que les deux applications ou aucune des applications soient créées :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs d’administration COM+](handling-com--administration-errors.md)
</dt> <dt>

[Exemple d’introduction utilisant le catalogue d’administration COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Vue d’ensemble des objets comadmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Récupération des regroupements sur le catalogue COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Définition des propriétés et enregistrement des modifications dans le catalogue COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



