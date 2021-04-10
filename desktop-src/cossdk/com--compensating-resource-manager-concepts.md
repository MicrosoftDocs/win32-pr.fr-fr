---
description: Vous pouvez utiliser le Gestionnaire des ressources CRM (Compensating Compensating) pour intégrer facilement et rapidement des ressources d’application à des transactions Microsoft Distributed Transaction Coordinator (DTC).
ms.assetid: 8d1d034f-8a09-40ae-842a-5251135bd3c8
title: Concepts de Gestionnaire des ressources de compensation COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14206a54ffcb4f7e06ddf7362736a722393b0791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950607"
---
# <a name="com-compensating-resource-manager-concepts"></a>Concepts de Gestionnaire des ressources de compensation COM+

Vous pouvez utiliser le Gestionnaire des ressources CRM (Compensating Compensating) pour intégrer facilement et rapidement des ressources d’application à des transactions Microsoft Distributed Transaction Coordinator (DTC). Les ressources de votre application peuvent voter sur le résultat d’une transaction et peuvent recevoir la notification finale de ses résultats. Un journal durable est généré afin que les ressources de votre application puissent écrire des enregistrements qui survivent aux échecs et que le CRM récupère ce fichier journal au redémarrage de l’application.

Un CRM comprend les deux composants suivants :

-   CRM Worker. Ce composant effectue le travail principal du CRM spécifique et implémente une interface spécifique à la tâche qu’il doit effectuer. L’infrastructure CRM fournit une interface au processus de travail CRM par le biais duquel le processus de travail CRM peut écrire des enregistrements dans un fichier journal durable sur le disque. Le processus de travail CRM doit écrire des enregistrements dans le journal et les rendre durables avant d’effectuer son travail afin que, si un incident se produise, la récupération puisse se produire correctement. Le processus de travail CRM requiert toujours une transaction.
-   Compensateur CRM. Ce composant est créé par l’infrastructure CRM à l’issue de la transaction. Il implémente une interface définie par laquelle l’infrastructure CRM peut transmettre les notifications d’achèvement des transactions et les enregistrements de journal précédemment écrits par le processus de travail CRM.

Un CRM COM+ fournit une atomicité avec les notifications transactionnelles et la durabilité avec le journal CRM, mais ne permet pas l’isolation des ressources. Dans un environnement multithread, il incombe au développeur CRM de s’assurer que l’accès aux ressources, que ce soit par plusieurs Workers CRM ou applications externes, est sérialisé dans une transaction.

Une fois que la transaction a dépassé la phase de préparation, le compensateur CRM et le CRM Workers peuvent s’exécuter simultanément. Il est possible que le composant de travail CRM d’une nouvelle transaction devienne actif alors que le compensateur CRM d’une transaction précédente traite toujours la transaction précédente.

Pendant les défaillances avant la récupération de l’application CRM Server, une transaction interrompue doit être considérée comme active et non terminée. Il ne devrait pas être possible pour les processus externes d’accéder aux ressources qui étaient modifiées par cette transaction avant la récupération du processus du serveur CRM.

Le CRM définit trois types d’interface pour les fonctions CRM de base :

-   [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) est implémenté sur le Clerk CRM et est utilisé par le processus de travail CRM pour écrire des enregistrements de journal dans le journal. Il peut également être utilisé par le compensateur CRM.
-   [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) et [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) sont implémentés sur le compensateur CRM. Ces interfaces sont utilisées pour fournir des notifications de résultat de transaction et leurs enregistrements de journal associés au compensateur CRM. Normalement, le compensateur CRM n’implémenterait qu’une seule de ces interfaces, selon qu’il a requis des enregistrements de journal non structurés ou structurés. Les *enregistrements de journal structurés* sont ceux qui sont générés sous la forme d’une collection de variantes et qui sont généralement utilisés par Microsoft Visual Basic. Les *enregistrements de journal non structurés* sont simplement une mémoire tampon d’octets et sont généralement utilisés par Microsoft Visual C++. Un compensateur CRM peut implémenter les deux interfaces Compensator ; Toutefois, une seule à la fois est utilisée pour remettre les enregistrements de journal.
-   Les interfaces d’analyse CRM de COM+ sont utilisées pour analyser les données de gestion des données au sein d’une application serveur particulière. Pour plus d’informations sur les interfaces de surveillance, consultez [interfaces de surveillance CRM com+](com--crm-monitoring-interfaces.md).

Les rubriques suivantes de cette section fournissent plus de détails sur le service CRM COM+ :

-   [Considérations sur la sécurité de COM+ CRM](com--crm-security-considerations.md)
-   [Processus de fonctionnement COM+ CRM](com--crm-operating-process.md)
-   [Démarrage et récupération COM+ CRM](com--crm-startup-and-recovery.md)
-   [Utilisation du CRM COM+ dans un environnement de cluster](using-the-com--crm-in-a-cluster-environment.md)
-   [Gestion des erreurs dans le CRM COM+](error-handling-in-the-com--crm.md)
-   [Paramètres du Registre CRM CRM](com--crm-registry-settings.md)
-   [Résolution des problèmes liés à COM+ CRM](troubleshooting-the-com--crm.md)
-   [Suggestions de conception pour le développement d’un CRM COM+](design-suggestions-for-developing-a-com--crm.md)
-   [Interfaces d’analyse CRM COM+](com--crm-monitoring-interfaces.md)
-   [Interfaces CRM COM+](com--crm-interfaces.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-tasks.md)
</dt> </dl>

 

 



