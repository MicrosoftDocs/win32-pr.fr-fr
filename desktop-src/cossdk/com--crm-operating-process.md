---
description: Processus de fonctionnement COM+ CRM
ms.assetid: be50912e-b9fd-4ef7-b81a-e37617a96955
title: Processus de fonctionnement COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39dba3dedcbdefebe0f62144547ebb6985fa51f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861637"
---
# <a name="com-crm-operating-process"></a>Processus de fonctionnement COM+ CRM

En mode de fonctionnement normal, un composant d’application exécuté dans un processus d’application serveur utilise un CRM COM+ en créant un travail CRM. Le processus de travail CRM implémente une interface COM spécifique à la tâche qu’il est conçu pour effectuer. Le composant d’application doit s’exécuter sous une transaction afin que le processus de travail CRM hérite de la transaction du composant d’application. Les Workers CRM requièrent toujours une transaction.

Pour accéder au CRM COM+, le Worker CRM obtient d’abord l’interface [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) , ce qui permet au processus de travail CRM d’écrire des enregistrements dans le journal durable. Le processus de travail CRM obtient cette interface en créant un composant Clerk CRM.

Ensuite, le CRM Worker doit indiquer au Clerk CRM le nom du compensateur CRM qu’il souhaite utiliser. Pour ce faire, il appelle la méthode [**ICrmLogControl :: RegisterCompensator**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) . Une fois cette méthode appelée, le compensateur CRM est créé par l’infrastructure CRM lorsque la transaction est terminée.

Une fois que le service CRM a inscrit son compensateur CRM, il peut écrire des enregistrements dans le journal CRM à l’aide de [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol). Le processus de travail CRM doit écrire à l' *avance*; autrement dit, il doit écrire un enregistrement dans le journal décrivant une action avant d’effectuer l’action, au cas où un incident se produira immédiatement après l’achèvement de l’action. Sans ces enregistrements de journal avec écriture anticipée, il n’existe aucun moyen de corriger l’action.

En outre, l’écriture anticipée signifie que le compensateur CRM, qui est le composant qui reçoit les enregistrements de journal en cours de récupération, doit gérer le cas où les enregistrements de journal ont été écrits, mais que l’action n’a pas été effectuée en fait. Les actions effectuées par le compensateur CRM doivent être *idempotent*; autrement dit, elles doivent pouvoir être exécutées plusieurs fois, mais doivent entraîner le même résultat. Par exemple, la définition d’un solde de compte à la valeur $100 est une action idempotent ; l’ajout de $100 au solde du compte n’est pas.

L’interface [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) fournit les deux méthodes suivantes pour écrire des enregistrements de journal :

-   [**WriteLogRecordVariants**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants) est utilisé pour écrire un enregistrement de journal structuré qui est créé sous la forme d’une collection de variantes. Il est principalement destiné à une utilisation lors du développement de CRM dans Microsoft Visual Basic.
-   [**WriteLogRecord**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecord) est utilisé pour l’écriture d’un enregistrement de journal non structuré en tant qu’objet blob d’octets. Il est principalement destiné à une utilisation lors du développement de CRM dans Microsoft Visual C++. Étant donné que les structures d’enregistrement en C sont souvent composées d’un ensemble d’en-têtes et de champs qui peuvent être disséminés en mémoire, la méthode **WriteLogRecord** implémente une fonctionnalité de regroupement qui réduit la copie des données.

> [!Note]  
> Vous ne devez pas les types de pointeur utilisateur dans les structures de données d’un enregistrement de journal. Les pointeurs ne sont plus valides durant la phase de récupération, car le compensateur CRM s’exécute dans un processus différent de celui du travail CRM qui a écrit l’enregistrement du journal. L’inclusion de types pointeur dans un enregistrement de journal peut entraîner un blocage ou une altération de l’application pendant la récupération.

 

Ces deux méthodes d’écriture écrivent un enregistrement de journal sur le disque, mais ne garantissent pas la durabilité de l’enregistrement. Tout en autorisant l’accumulation des écritures différées avant de forcer le disque à améliorer les performances, vous pouvez utiliser la méthode [**ICrmLogControl :: ForceLog**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcelog) à la place pour garantir que toutes les écritures effectuées par le CRM sont durables sur le disque, ce qui est important pour la récupération en cas d’échec.

Lorsque le processus de travail CRM est terminé avec ses actions et a terminé l’écriture et le forçage des enregistrements dans le journal, il doit libérer [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol). Une fois la transaction terminée (en général, en raison du composant d’application qui appelle [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ou [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)), l’infrastructure CRM crée le composant CRM compensator, qui implémente l’interface [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) ou l’interface [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) . Ces interfaces sont utilisées pour transmettre les enregistrements non structurés (Visual C++) ou structurés (Visual Basic) au compensateur CRM avec les notifications de résultat de la transaction.

Le compensateur CRM est tout d’abord notifié de la phase de préparation de l’exécution de la transaction et peut voter oui ou non pour la demande de préparation. Si le compensateur CRM vote non, il ne reçoit pas de notifications d’abandon supplémentaires. S’il vote oui pour la demande de préparation, il reçoit les notifications de validation ou d’abandon. En cas d’abandon d’un client, aucune notification de préparation n’est reçue, les notifications d’abandon sont uniquement abandonnées. Le compensateur CRM doit être prêt à gérer tous ces cas, et il doit également gérer le cas où aucun enregistrement de journal n’a été écrit avec succès par le Worker CRM. Le compensateur CRM ne doit pas supposer que la même instance CRM Compensator recevra à la fois les notifications de phase 1 (préparation) et de phase 2 (validation ou abandon), car elles pourraient être interrompues par la récupération.

En règle générale, un Compensator CRM utilise la notification d’abandon pour inverser l’action effectuée par le processus de travail CRM. Le processus de travail CRM peut conserver un état disponible au cas où il aurait besoin d’inverser son action. Cet État peut être entièrement contenu dans les enregistrements de journal. dans le cas contraire, le compensateur CRM doit nettoyer cet État si la transaction est validée. C’est la raison pour laquelle le compensateur CRM reçoit la notification de validation. Le compensateur CRM ne s’exécute pas sous une transaction DTC.

Le compensateur CRM peut enregistrer de nouveaux enregistrements si nécessaire à l’aide de [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol), qu’il reçoit lorsqu’il est créé. Le processus de travail CRM et le compensateur CRM peuvent également oublier le dernier enregistrement de journal qu’ils ont écrit, ce qui peut être nécessaire pour éviter une récupération inutile.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Démarrage et récupération COM+ CRM](com--crm-startup-and-recovery.md)
</dt> </dl>

 

 



