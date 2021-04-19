---
title: Cycle de vie d’une tâche BITS
description: Le cycle de vie d’un travail BITS commence lorsque vous créez un travail.
ms.assetid: b765a8ef-74bd-475e-9cd9-e9e2cf4f0305
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c6ac23c598d28681968e9c0cbed776ba24c57e98
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106537183"
---
# <a name="bits-job-states"></a>États du travail BITS
Il existe quatre classes d' [**États**](/windows/desktop/api/Bits/ne-bits-bg_job_state)bits : Starting, action, transfered et final. Lorsqu’un travail s’exécute, il passe d’un État à l’autre dans les différentes classes d’État. Une fois qu’un travail est dans un état final, il ne quitte pas l’état final et ne s’affiche pas dans une [énumération de travaux](/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs).

## <a name="state-changing-methods"></a>Méthodes de modification d’État
Il existe quatre méthodes de modification de l’état d’un travail : [**Annuler**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel), [**Terminer**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete), [**reprendre**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)et [**suspendre**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend). Tant qu’un travail n’est pas dans un état final, vous pouvez appeler n’importe quelle méthode de modification de l’État. 

La méthode [**suspend**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend) est utilisée pour faire passer un travail à l’État Suspended. Lorsqu’un travail est suspendu, tous ses transferts sont arrêtés et ne reprennent pas tant que vous n’appelez pas Resume.
Un travail qui est déjà suspendu reste simplement suspendu.

La méthode [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) est utilisée pour démarrer un travail qui est suspendu. Les travaux en état d’erreur ou d’erreur temporaire seront configurés pour une nouvelle tentative. Les travaux qui sont actuellement dans un état d’action restent dans cet État.

La méthode [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) est utilisée pour annuler un travail. L’état passe à annulé. Les fichiers en cours de transfert ne seront pas terminés. Tous les fichiers entièrement transférés et transférés partiellement seront supprimés.

La méthode [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) termine un transfert. Tous les fichiers entièrement téléchargés sont conservés. les fichiers qui ne sont pas entièrement transférés seront supprimés.

Vous devez appeler annuler ou terminer pour déplacer votre travail vers un état final et le nettoyer. Les tâches qui ne sont pas transférées vers un état final gaspillent les ressources système. Le service BITS annule ensuite automatiquement les anciens travaux. Le [paramètre jobinactivitytimeout](/windows/desktop/Bits/group-policies) par défaut consiste à annuler les travaux au bout de 90 jours.


## <a name="starting-state"></a>État initial 
L’état de démarrage est **suspendu**. À partir de là, vous pouvez ajouter des fichiers au travail et définir les propriétés des travaux et des fichiers. Pour démarrer un travail de transfert, appelez Resume sur le travail. Si vous reprenez un travail sans fichier, il renverra un code d’erreur BG_E_EMPTY et le travail restera suspendu.

## <a name="action-states"></a>États d’action
Les États de mise en **file d’attente**, de **connexion** et de **transfert** affichent l’activité interne actuelle de votre travail. Un travail mis en file d’attente est prêt à être planifié, probablement en attente du planificateur BITS ou en attente de connexion de l’utilisateur. Un travail qui se CONNECTe tente de se connecter au serveur pour commencer à transférer des fichiers. Un travail qui transfère est en train de charger ou de télécharger vos fichiers.

L’état d' **erreur temporaire** signifie que la tâche a été tentée et qu’elle n’a pas réussi à transférer le fichier. Cela peut être pour des raisons de stratégie réseau. le travail est peut-être bloqué, car le réseau actuel est trop onéreux. Elle peut également être bloquée pour des raisons de système telles que le système se trouve dans l’économiseur de batterie ou le mode jeu, ou parce qu’il n’y a pas de connectivité Internet. 

Les travaux en état d’erreur temporaire sont retentés automatiquement par BITS, le cas échéant. BITS comprend une valeur [MinimumRetryDelay](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) et [NoProgressTimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) pour contrôler le moment auquel un travail est relancé et le moment où bits arrête la nouvelle tentative.


## <a name="transferred-states"></a>États transférés
Les États transférés se produisent lorsqu’il n’y a plus de transfert à effectuer. Vous devez annuler ou terminer un travail dans cet État. Vous pouvez également ajouter d’autres fichiers à transférer et appeler RESUME (), mais ce n’est pas une pratique courante.

L’état d' **erreur** se produit lorsqu’un transfert est effectué (il ne sera pas retenté), mais ne s’est pas terminé correctement. Tous les fichiers doivent être transférés pour réussir. en cas d’échec définitif du travail, le travail est erroné. En général, vous appelez la fonction CANCEL ou Complete pour déplacer le travail vers un état final. La différence pratique est que lorsque vous appelez Cancel, tout fichier transféré avec succès sera supprimé, mais si vous appelez Complete, aucun fichier transféré avec succès ne sera supprimé.

Les raisons de l’état d’erreur sont les suivants : 
* Rester trop longtemps dans un état d’erreur temporaire (au-delà du paramètre [NoProgressTimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) ).
* Obtenir une erreur de BG_E_TOKEN_REQUIRED et avoir besoin d’aide avec les [jetons d’assistance](/windows/desktop/Bits/helper-tokens-for-bits-transfer-jobs)

Il est courant de reconfigurer un travail d’erreur, puis d’appeler Resume pour retenter la tâche. Par exemple, votre application peut avoir besoin de mettre à jour le nom distant d’un fichier via [SetRemoteName](/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename).

L’état **transféré** se produit lorsqu’un transfert est terminé et qu’il a réussi. Vous devez appeler Complete pour finaliser le travail ; pour les tâches de téléchargement, les fichiers téléchargés ne sont pas disponibles tant que vous n’avez pas terminé l’appel. La seule exception à cette règle concerne les tâches à haut niveau de performances (et vous devez toujours appeler Complete).

## <a name="final-states"></a>États finaux
Une fois qu’un travail est dans un état final, vous ne pouvez pas appeler les méthodes de modification d’État. La tâche est **confirmée** après l’appel de Complete () et tous les fichiers téléchargés terminés sont disponibles. La tâche est **annulée** une fois que vous avez appelé Cancel () et que tous les fichiers téléchargés sont supprimés. 


## <a name="life-cycle-of-a-bits-job"></a>Cycle de vie d’une tâche BITS

Le cycle de vie d’un travail BITS commence lorsque vous créez un travail. Un travail est un conteneur qui contient un ou plusieurs fichiers à transférer. Un travail possède également des propriétés qui spécifient comment BITS transfère les fichiers et interagit avec votre application. Par exemple, vous pouvez spécifier la priorité du travail, s’il s’agit d’un travail de chargement ou de téléchargement, et pour quels événements vous souhaitez recevoir des notifications.

Après avoir créé le travail, ajoutez un ou plusieurs fichiers (les travaux de chargement ne peuvent contenir qu’un seul fichier) au travail et modifiez les valeurs de propriété en fonction de votre application. Lorsque vous ajoutez un fichier au travail, spécifiez à la fois le nom local (client) et le nom distant (serveur) du fichier. Le nom du fichier distant doit utiliser le protocole HTTP, HTTPs ou SMB. Les fichiers d’un travail sont traités séquentiellement (premier dans, premier sorti).

Le service BITS interrompt automatiquement les travaux lorsqu’ils sont créés. Vous devez reprendre la tâche pour l’activer dans la file d’attente de transfert. Vous pouvez suspendre ou reprendre un travail à tout moment. La reprise du travail déplace le travail de l’état suspendu à l’État en file d’attente. Le travail reste dans l’état de mise en file d’attente jusqu’à ce que le planificateur détermine qu’il est le tour du travail de transférer des fichiers. Tous les travaux de premier plan s’exécutent simultanément avec un travail en arrière-plan. BITS traite les fichiers dans les travaux de premier plan en série.

Lorsqu’il s’agit d’une tâche de transfert de fichiers, le travail passe à l’État connexion pendant que BITS se connecte au serveur distant (spécifié dans le nom du fichier distant). Si le service BITS est en mesure de se connecter au serveur distant, le travail passe à l’État transfert où il reste jusqu’à ce que sa tranche de temps se termine, que le transfert soit terminé, qu’une erreur se produise ou que l’application interrompe le travail.

Le travail se déplace entre les États de mise en file d’attente, de connexion et de transfert jusqu’à ce que le service BITS transfère tous les fichiers du travail. À ce stade, le travail passe à l’état transféré. BITS utilise la planification par tourniquet (Round Robin) pour planifier les tâches qui sont au même niveau de priorité. Chaque travail reçoit une tranche de temps pour traiter ses fichiers. Si la tâche ne se termine pas pendant sa tranche de temps, le travail revient à l’État en file d’attente et la tâche suivante dans la file d’attente est activée. Cela évite que des travaux de grande taille bloquent des tâches plus petites. Les travaux sont traités en grande partie selon le principe du premier entré, premier sorti (FIFO). Toutefois, le service BITS ne peut pas garantir le traitement FIFO en raison de la planification par tourniquet (Round Robin), des erreurs de travail et des redémarrages du service.

Les fichiers transférés ne sont pas disponibles pour le client tant que l’application n’a pas appelé la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) pour transférer la propriété des fichiers de bits à l’utilisateur. Les travaux de chargement sont également définis sur l’état transféré lorsque le fichier est reçu avec succès par le serveur. Les travaux de chargement-réponse sont définis sur l’état transféré une fois que le fichier a été envoyé au serveur et que la réponse de l’application serveur est transférée avec succès au client.

Si une erreur se produit, le travail passe à l’état d’erreur irrécupérable ou temporaire. Les erreurs irrécupérables sont des erreurs que BITS ne peut pas récupérer à partir de ou qui nécessitent une intervention pour résoudre le problème. Si l’application est en mesure de corriger l’erreur, l’application reprend la tâche et le service BITS déplace la tâche à l’État en file d’attente. Les erreurs temporaires sont des erreurs qui peuvent se résoudre eux-mêmes. BITS réessaie les travaux en état d’erreur temporaire jusqu’à ce que le transfert soit réussi ou que le délai d’attente du travail soit dépassé. Le travail expire quand aucune progression n’est effectuée au cours d’une période spécifiée par l’application. Si le travail expire, le service BITS déplace le travail vers l’état d’erreur irrécupérable.

Pour plus d’informations sur les États de travail, consultez [**\_ \_ État du travail BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state).
