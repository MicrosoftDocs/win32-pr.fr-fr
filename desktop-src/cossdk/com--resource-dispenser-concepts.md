---
description: Les composants d’application utilisent le distributeur de ressources COM+ pour accéder et gérer les informations d’État partagées non durables, telles que les connexions entre les composants et un gestionnaire de ressources donné.
ms.assetid: 252c7180-61b1-485d-883d-36bf77357a29
title: Concepts du distributeur de ressources COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0fcf281d6d7b8ed0e087b6d77e4d686e28e1fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748068"
---
# <a name="com-resource-dispenser-concepts"></a>Concepts du distributeur de ressources COM+

Les composants d’application utilisent le distributeur de ressources COM+ pour accéder et gérer les informations d’État partagées non durables, telles que les connexions entre les composants et un gestionnaire de ressources donné. Lors de l’exécution, les pools dynamiques de ressources, tels que les connexions de base de données, les connexions réseau, les connexions aux files d’attente, les threads, les objets et les blocs de mémoire, sont mis à la disposition du distributeur de ressources. Le processus d’application atteint des performances élevées en utilisant un nombre minimal de ressources fréquemment utilisées. Le distributeur de ressources peut également automatiser les transactions et la récupération. (Pour plus d’informations sur cette fonctionnalité, consultez [récupération automatique des ressources](automatic-resource-reclamation.md) .)

> [!Note]  
> Une *ressource* est un tout ce que crée un distributeur de ressources. Par exemple, une connexion à un gestionnaire de ressources est une ressource commune. Les ressources résident dans la mémoire du distributeur de ressources et ne sont jamais copiées dans le gestionnaire de distribution. Une ressource est connue uniquement par un handle opaque (**RESID**) et peut ou ne peut pas être en capacité à effectuer des transactions. Bien que les ressources gérées soient souvent des connexions à un composant gérant un État durable, les connexions elles-mêmes ne sont pas durables. Un distributeur de ressources utilise souvent un gestionnaire de ressources associé pour conserver l’État durable.

 

Architecturale, le système de distribution de ressources COM+ est constitué de dispenseurs de ressources et d’un gestionnaire de distributeur. Les distributeurs de ressources sont des composants fournis par l’utilisateur qui fournissent aux applications des interfaces simples aux ressources partagées. Le gestionnaire du distributeur est un composant fourni par COM+ qui coordonne les activités des différents distributeurs de ressources.

Un distributeur de ressources est un composant de bibliothèque de liens dynamiques (DLL) qui fournit au moins deux interfaces. La première, [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver), fournit au gestionnaire de distribution des informations de base sur la création, la destruction et l’inscription des ressources qu’il gère. Le deuxième est exposé aux applications et peut être une interface COM ou un ensemble d’interfaces ou peut être une interface de programmation d’applications (API) à laquelle un composant est lié via une bibliothèque d’importation. Une application peut appeler n’importe quel distributeur de ressources, qui peut, à son tour, proposer toute API à l’application. Si le distributeur de ressources est un composant Automation, il est accessible à partir de Microsoft Visual Basic. Un distributeur de ressources est instancié lorsqu’un composant d’application y fait référence.

Le gestionnaire de distribution fourni par COM+ effectue le suivi des distributions et des coordonnées des ressources entre eux. Il implémente deux interfaces : [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) et [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder). les distributeurs de ressources s’inscrivent à l’aide de l’interface **IDispenserManager** . Le gestionnaire de distribution lui donne ensuite un pointeur vers un **IHolder** qu’il utilise pour notifier le responsable du distributeur de ses activités.

Un distributeur de ressources transactionnel doit s’inscrire dans une transaction Distributed Transaction Coordinator (DTC). Cela implique l’utilisation d’un gestionnaire de ressources interne ou externe (pour le distributeur de ressources) qui est compatible avec les transactions OLE.

> [!Note]  
> Le modèle de programmation COM+ comprend des *transactions déclaratives*, qui permettent de protéger le travail effectué par un objet d’application pendant sa durée de vie. Lorsqu’un objet d’application utilise un distributeur de ressources COM+, le travail qu’il effectue est automatiquement transactionnel ; autrement dit, le composant n’a pas besoin de déclarer explicitement des transactions. Ces transactions sont définies dans la spécification OLE Transactions, implémentée par le DTC et lancées pour le compte de l’objet d’application par COM+. Pour plus d’informations, consultez le Guide de développement DTC.

 

Les ressources n’ont pas besoin d’être transactionnelles. Un distributeur de ressources qui regroupe des ressources non transactionnelles peut toujours atteindre des performances élevées en permettant aux objets d’application d’accéder à un pool partagé de ces ressources. Ce type de distributeur de ressources retourne S \_ false à partir de la méthode [**IDispenserDriver :: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) , ce qui signifie que le distributeur de ressources n’a pas inscrit la ressource, car la ressource n’est pas transactionnelle.

Le distributeur de ressources peut également fonctionner indépendamment de COM+, en fournissant uniquement des fonctionnalités de mise en pool de ressources. Par exemple, si un distributeur de ressources expose une API (par exemple, ODBC), le distributeur de ressources peut être une DLL accessible par l’application via une bibliothèque d’importation (ou à l’aide des fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ). Un distributeur de ressources peut également être un composant COM auquel une application accède en appelant [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Sans COM+, la méthode [**EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) d’un distributeur de ressources ne peut jamais être appelée, car le gestionnaire du distributeur n’a aucune connaissance de la transaction du composant en cours.

Au démarrage, une DLL de distributeur de ressources doit s’inscrire auprès du gestionnaire du distributeur. Le gestionnaire du distributeur est le cadre de contrôle qui gère le chargement et le déchargement des distributeurs de ressources, fournit le contexte COM+ et contrôle le gestionnaire des statistiques d’inventaire. (Pour plus d’informations, consultez [Gestionnaire du distributeur com+](com--dispenser-manager.md).) Le distributeur de ressources appelle d’abord la fonction [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) , puis appelle la méthode [**IDispenserManager :: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser) , en passant le pointeur [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) implémenté par le distributeur de ressources. Cet appel retourne une référence à [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder).

Pour arrêter, un distributeur de ressources appelle [**IHolder :: Close**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-close). Pour garantir un arrêt correct du package, un distributeur de ressources doit être en mesure de gérer la situation dans laquelle les appels continuent d’arriver à partir des objets métier après que COM+ a demandé l’arrêt du distributeur.

Les rubriques suivantes de cette section fournissent des informations plus détaillées sur le service de distribution de ressources COM+ :

-   [Gestionnaire de distributeur COM+](com--dispenser-manager.md)
-   [Types de threads du distributeur de ressources COM+](com--resource-dispenser-thread-types.md)
-   [États des ressources regroupées accessibles au distributeur de ressources COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
-   [Inscription d’une ressource dans une transaction](enlisting-a-resource-in-a-transaction.md)
-   [Processus d’allocation des ressources du distributeur de ressources](resource-dispenser-resource-allocation-process.md)
-   [Suivi des ressources non allouées](tracking-non-allocated-resources.md)
-   [Récupération automatique des ressources](automatic-resource-reclamation.md)
-   [Types utilisés dans les interfaces de distributeur de ressources COM+](types-used-in-com--resource-dispenser-interfaces.md)
-   [Interfaces du distributeur de ressources COM+](com--resource-dispenser-interfaces.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches du distributeur de ressources COM+](com--resource-dispenser-tasks.md)
</dt> </dl>

 

 
