---
description: La version 1,5 de COM+ ajoute de nouvelles fonctionnalités conçues pour augmenter l’extensibilité, la disponibilité et la facilité de gestion des applications COM+ à la fois pour les développeurs et pour les administrateurs système.
ms.assetid: e7073ba5-6b19-4d94-8cc0-b4e16bb44afd
title: Nouveautés de COM+ 1,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0fd6705775e84f49d3a60afd7d89b7a5412b4a87fd5d04f202fadc77fd850d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304880"
---
# <a name="whats-new-in-com-15"></a>Nouveautés de COM+ 1,5

La version 1,5 de COM+ ajoute de nouvelles fonctionnalités conçues pour augmenter l’extensibilité, la disponibilité et la facilité de gestion des applications COM+ à la fois pour les développeurs et pour les administrateurs système.

COM+ 1,5 est disponible à partir de Windows XP et Windows Server 2003. les nouvelles fonctionnalités COM+ 1,5 ne sont pas disponibles dans Windows 2000.

## <a name="application-level-access-checks-enabled-by-default"></a>Contrôles d’accès Application-Level activés par défaut

Dans le cadre de la sécurité améliorée du système, les vérifications d’accès sont activées par défaut lors de la création d’une application COM+. Dans les versions précédentes, les contrôles d’accès étaient désactivés par défaut au niveau de l’application et activés par défaut au niveau du composant. à compter de Windows Server 2003, les contrôles d’accès sont activés par défaut au niveau de l’application et désactivés par défaut au niveau du composant. Consultez [création d’une application com+](creating-a-new-com--application.md), [activation des vérifications d’accès pour une application](enabling-access-checks-for-an-application.md)et [activation des vérifications d’accès au niveau du composant](enabling-access-checks-at-the-component-level.md) pour plus d’informations et de procédures sur la façon de modifier les paramètres par défaut.

## <a name="application-pooling"></a>Regroupement d’applications

Avec la nouvelle propriété ConcurrentApps de l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection d' [**applications**](applications.md) , le regroupement d’applications COM+ ajoute une évolutivité pour les processus monothread et s’intègre au nouveau service de recyclage des applications com+. Pour plus d’informations, consultez [regroupement d’applications com+](com--application-pooling.md) .

## <a name="application-recycling"></a>Recyclage d’applications

Le recyclage des applications augmente considérablement la stabilité globale de vos applications. Étant donné que les performances de la plupart des applications peuvent se dégrader au fil du temps, en raison de facteurs tels que les fuites de mémoire, le recours à du code tiers et l’utilisation des ressources non évolutives, le recyclage des applications COM+ offre une solution simple pour arrêter de manière appropriée un processus associé à une application et le redémarrer. Pour plus d’informations, consultez [recyclage d’applications com+](com--application-recycling.md) . Pour une procédure pas à pas de configuration du recyclage de processus, voir également « configuration du recyclage de processus » dans l’aide sur l’administration des services de composants.

## <a name="com-partitions"></a>Partitions COM+

Dans cette version, COM+ introduit la prise en charge des partitions COM+, une fonctionnalité qui permet d’installer et de configurer plusieurs versions d’applications COM+ sur le même ordinateur. Cette fonctionnalité peut vous faire gagner du temps, en utilisant plusieurs serveurs pour gérer les différentes versions d’une application. Sur un ordinateur unique, chaque partition agit en fait en tant que serveur virtuel. Après l’installation de l’application dans chaque partition, vous créez des jeux de partitions qui mappent les utilisateurs aux serveurs logiques. Pour plus d’informations sur la configuration et la gestion des partitions COM+, consultez [partitions com+](com--partitions.md) . Pour obtenir des procédures pas à pas, consultez également « administration de partitions d’application » dans l’aide sur l’administration des services de composants.

## <a name="com-services-without-components"></a>Services COM+ sans composants

Avec COM+ 1,5, vous pouvez utiliser les services fournis par COM+ sans avoir à créer un composant pour contenir les méthodes qui appellent ces services. Cela permet aux développeurs qui n’utilisent pas généralement des composants d’utiliser des services COM+ tels que des transactions ou le dispositif de suivi COM+. En utilisant des services COM+ sans composants, les développeurs peuvent éviter la surcharge liée à la création d’un composant qui est utilisé pour accéder uniquement aux services COM+ dont ils ont besoin. Pour plus d’informations, consultez [services com+ sans composants](com--services-without-components.md) .

## <a name="com-soap-service"></a>Service SOAP COM+

Avec COM+ 1,5, vous pouvez désormais exposer une application COM+ en tant que service Web XML. Vous pouvez également utiliser de manière transparente un service Web XML, qu’il soit déployé à l’aide de COM+ ou non, en tant que composant COM. Cela signifie que vous pouvez facilement créer des services Web XML à partir d’applications COM+ existantes et incorporer facilement des services Web XML dans de nouvelles applications COM+. Pour plus d’informations, consultez [service SOAP com+](com--soap-service.md) .

## <a name="configurable-isolation-levels"></a>Niveaux d’isolement configurables

Les développeurs COM+ peuvent utiliser la nouvelle propriété TxIsolationLevel ou l’outil d’administration Services de composants pour configurer le niveau d’isolation d’une application en fonction des besoins, ce qui contribue à augmenter la concurrence, les performances et l’évolutivité. Cette flexibilité permet à ceux qui ont le bon niveau d’expertise de s’adapter à chaque dernier débit de leurs applications. Pour plus d’informations, consultez [Configuration des niveaux d’isolation des transactions](configuring-transaction-isolation-levels.md) .

## <a name="creating-private-components"></a>Création de composants privés

Dans les scénarios où vous avez plusieurs composants d’assistance dans une application destinés à être appelés uniquement à partir d’autres composants au sein de cette application, cette version de COM+ vous permet d’utiliser une nouvelle propriété, IsPrivateComponent, pour marquer ces composants comme privés. (Dans la version précédente de COM+, tous les composants devaient être publics pour pouvoir accéder aux services COM+, ce qui signifie que ces composants pouvaient être activés à partir d’autres applications.) Un composant privé peut être vu et activé uniquement par d’autres composants de la même application, ce qui vous permet de mieux contrôler les fonctionnalités à exposer. Vous avez uniquement besoin de documenter et de gérer les composants publics, tout en utilisant des composants privés qui ne sont pas accessibles à partir de l’extérieur de l’application, mais qui peuvent toujours tirer parti de tous les services COM+.

## <a name="dtc-security-settings"></a>Paramètres de sécurité DTC

Plusieurs nouveaux paramètres de sécurité ont été ajoutés pour le Distributed Transaction Coordinator Microsoft (DTC), ce qui vous permet de personnaliser vos niveaux de sécurité pour la gestion des transactions distribuées. Pour plus d’informations sur ces paramètres, consultez Considérations sur la sécurité DTC et comment les implémenter.

Pour faciliter l’authentification mutuelle, le DTC est limité à l’exécution sous le compte NetworkService. Pour plus d’informations, consultez Gestion des comptes et des privilèges.

Pour la récupération avec les bases de données XA, il est recommandé que le compte NetworkService fournisse les autorisations et les rôles nécessaires pour effectuer cette récupération. La méthode exacte pour ce faire est spécifique à chaque base de données. Pour plus d’informations, consultez Désactivation des transactions distribuées natives et désactivation des transactions TIP et XA.

pour fournir un système plus sécurisé lors de l’utilisation de transactions xa, Windows plateformes du serveur 2003 incluent une nouvelle entrée de registre pour la spécification des fichiers DLL xa. lors de la mise à niveau vers Windows Server 2003, vous pouvez utiliser les transactions XA comme avant en créant une entrée de registre sous **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ MSDTC \\ XADLL**, où le nom de la valeur est le nom de la dll (au format *dllname*.dll) et la valeur est le chemin d’accès complet du fichier dll. Vous devez créer une entrée pour chaque fichier DLL XA en cours d’utilisation. Si l’ordinateur qui exécute DTC fait partie d’un cluster, l’entrée de registre doit être effectuée pour chaque nœud du cluster. Pour plus d’informations, consultez Gestion des transactions XA.

## <a name="low-memory-activation-gates"></a>Low-Memory les portes d’activation

Avec cette version, COM+ vérifie automatiquement la mémoire avant de créer un serveur ou un objet COM+. Si le pourcentage de mémoire virtuelle disponible pour l’application tombe en dessous d’un seuil fixe, l’activation échoue avant la création de l’objet. En faisant échouer ces activations normalement exécutées, le service des [portes d’activation COM+ Low-Memory](com--low-memory-activation-gates.md) améliore la fiabilité du système.

## <a name="moving-and-copying-com-components"></a>Déplacement et copie de composants COM

Avec cette version, COM+ vous permet de déplacer et de copier vos composants. Cela signifie que vous pouvez configurer une implémentation physique unique d’un composant à de nombreuses heures différentes. Vous bénéficiez de la réutilisation des composants au niveau binaire plutôt qu’au niveau du code source, ce qui réduit le code, réduit les coûts de développement et accélère le délai de mise sur le marché. Pour plus d’informations, consultez [déplacement de composants](moving-components.md) et [copie de composants](copying-components.md) .

## <a name="network-access"></a>Accès réseau

l’accès réseau com+ est désactivé par défaut sur le serveur Windows 2003, ce qui signifie que COM+ ne peut être utilisé que localement par défaut. Utilisez la procédure suivante pour activer l’accès COM+ réseau.

**Pour activer l’accès COM+ réseau**

1.  Dans le menu **Démarrer** , pointez sur **panneau de configuration**, puis sélectionnez **Ajout/suppression de programmes**.

2.  cliquez sur **ajouter/supprimer des composants de Windows**.

3.  Sélectionnez **Serveur d'applications** et cliquez sur **Détails**.

4.  Cochez la case en regard de **activer l’accès com+ réseau**, puis cliquez sur **OK**.

5.  cliquez sur **suivant** pour terminer l’assistant composants de Windows.

6.  Cliquez sur **Terminer** pour fermer l'Assistant.

l’accès aux transactions réseau DTC est désactivé par défaut sur Windows Server 2003. Sur ces plateformes, le DTC peut uniquement effectuer des transactions locales par défaut. Utilisez la procédure suivante pour activer l’accès DTC réseau.

> [!NOTE]
> Vous pouvez également activer l’accès DTC réseau à l’aide de l’outil d’administration Services de composants ou par programme par le biais de la bibliothèque d’administration COM+. Pour plus d’informations sur les procédures, consultez « Configuration de la sécurité DTC » dans l’aide sur l’administration des services de composants.

**Pour activer l’accès DTC réseau**

1.  Dans le menu **Démarrer** , pointez sur **panneau de configuration**, puis sélectionnez **Ajout/suppression de programmes**.

2.  cliquez sur **ajouter/supprimer des composants de Windows**.

3.  Sélectionnez **Serveur d'applications** et cliquez sur **Détails**.

4.  Cochez la case en regard de **activer l’accès DTC réseau**, puis cliquez sur **OK**.

5.  cliquez sur **suivant** pour terminer l’assistant composants de Windows.

6.  Cliquez sur **Terminer** pour fermer l'Assistant.

## <a name="pausing-and-disabling-applications"></a>Suspension et désactivation d’applications

Les applications COM+ sont désormais plus gérables. Un administrateur peut suspendre et reprendre des applications serveur COM+, ou désactiver et activer des applications serveur ou de bibliothèque COM+, voire des composants configurés individuels. Les fonctionnalités de suspension et de désactivation empêchent les futures activations sans affecter les instances de composant existantes. Pour plus d’informations, consultez « administration des applications COM+ » dans l’aide sur l’administration des services de composants.

## <a name="process-dumping"></a>Vidage de processus

Il n’est pas facile de dépanner des applications dans un environnement de production. Comment rassembler des informations sur un problème sans perturber les processus en cours d’exécution ? COM+ fournit désormais une solution par le biais de sa nouvelle fonctionnalité de vidage de processus. Cette fonctionnalité permet à l’administrateur système de vider l’intégralité de l’état d’un processus sans l’arrêter. Pour plus d’informations, consultez « administration de l’outil de vidage de processus pour déboguer des applications COM+ » dans l’aide sur l’administration des services de composants.

## <a name="process-initialization"></a>Initialisation du processus

De nombreuses applications serveur doivent effectuer une initialisation et un nettoyage spécifiques lorsqu’elles sont démarrées et arrêtées. lors de l’exécution sur Windows Server 2003, vous pouvez créer une classe qui implémente l’interface [**IProcessInitializer**](/windows/desktop/api/ComSvcs/nn-comsvcs-iprocessinitializer) . Lorsque le processus démarre, il appelle [**IProcessInitializer :: Startup**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-startup) et, lors de l’arrêt, il appelle [**IProcessInitializer :: Shutdown**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-shutdown). Cela donne à votre composant la possibilité d’effectuer des tâches nécessaires, telles que l’initialisation des connexions, des fichiers et des caches.

## <a name="running-com-applications-as-nt-services"></a>Exécution d’applications COM+ en tant que services NT

Les développeurs COM+ peuvent désormais utiliser l’outil d’administration Services de composants pour configurer et implémenter une application serveur COM+ en tant que service NT. Cela signifie que le serveur peut être démarré ou redémarré automatiquement si votre application doit toujours être en cours d’exécution ; que votre application COM+ peut s’exécuter en tant que compte système local s’il doit effectuer des opérations privilégiées ; et que les services dépendants de votre application peuvent maintenant être démarrés automatiquement. Pour plus d’informations, consultez [applications com+ s’exécutant en tant qu’applications de service](com--applications-running-as-service-applications.md) .

## <a name="side-by-side-assemblies"></a>Assemblys côte à côte

Les assemblys côte à côte (SxS) permettent aux applications de spécifier la version d’une DLL système ou d’un composant COM classique à utiliser, par exemple MDAC, MFS, MSVCRT ou MSXML. par exemple, si une application ASP s’appuie sur MSXML version 2,0, vous pouvez vous assurer que cette application utilise toujours MSXML version 2,0 même après l’application des service packs au serveur. autrement dit, même lorsqu’une nouvelle version de MSXML est installée sur l’ordinateur, la version 2,0 reste et est utilisée par votre application.

Pour configurer des assemblys SxS, vous devez connaître le chemin d’accès à la DLL et le fichier manifeste COM+ existe dans chaque répertoire virtuel qui doit utiliser la DLL. Le manifeste COM+ est un fichier XML qui contient des informations sur l’emplacement d’installation d’une DLL. Le manifeste est utilisé pour créer un contexte d’activation pour l’application. Les contextes d’activation permettent à une application de charger une version de DLL particulière, une instance d’objet COM ou une version de fenêtre personnalisée. Vous pouvez utiliser l’outil d’administration Services de composants ou la propriété ApplicationDirectory pour entrer le chemin d’accès complet du répertoire racine de l’application qui contient un fichier manifeste de l’assembly SxS valide. Pour plus d’informations, consultez [applications isolées et assemblys côte à côte](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

## <a name="windows-error-reporting"></a>Rapport d’erreurs Windows

COM+ 1,5 prend en charge le composant Rapport d’erreurs Windows (WER), disponible à partir de Windows XP. WER permet aux utilisateurs de signaler à Microsoft les erreurs d’application, les erreurs de noyau et les applications qui ne répondent pas. Ces notifications permettent aux équipes de support technique Microsoft de résoudre plus efficacement les problèmes techniques. en outre, le composant Rapport d’erreurs Windows permet aux développeurs COM+ de recevoir des informations qui peuvent être utilisées pour améliorer leurs applications. Pour plus d’informations, voir [Rapport d’erreurs Windows](/windows/desktop/wer/windows-error-reporting).

 

 
