---
description: Les interfaces CRM sont requises pour assurer la prise en charge des travailleurs CRM et des compensateurs CRM développés à l’aide de Visual Basic et Visual C++.
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Interfaces CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749005"
---
# <a name="com-crm-interfaces"></a>Interfaces CRM COM+

Les interfaces CRM sont requises pour assurer la prise en charge des travailleurs CRM et des compensateurs CRM développés à l’aide de Visual Basic et Visual C++.

Vous pouvez utiliser le Gestionnaire des ressources CRM (Compensating Compensating) pour intégrer rapidement et facilement des ressources d’application à des transactions Microsoft Distributed Transaction Coordinator (DTC).

Il est plus facile pour les composants écrits avec Visual Basic de créer un enregistrement de journal sous la forme d’une collection de variantes. En outre, les composants Visual Basic sont des threads cloisonnés, ce qui signifie qu’il doit être possible de marshaler les interfaces du cloisonnement multithread à un cloisonnement à thread unique. Les composants CRM développés avec Visual C++ pouvaient également utiliser le modèle de thread cloisonné, bien qu’il soit recommandé d’utiliser à la place le modèle de thread à la fois.

Les interfaces décrites dans le tableau suivant fournissent des informations de référence détaillées pour les développeurs de données CRM COM+.



| Interfaces CRM                                             | Description                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | Cette interface fournit des enregistrements de journal non structurés dans Visual C++.                                                           |
| [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | Cette interface fournit des enregistrements de journal structurés au compensateur CRM lors de l’utilisation de Visual Basic.                            |
| [**ICrmFormatLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | Cette interface convertit les enregistrements de journal au format affichable afin qu’ils puissent être présentés à l’aide d’un outil d’analyse générique. |
| [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | Cette interface est utilisée par le processus de travail CRM et le compensateur CRM pour écrire des enregistrements dans le journal et les rendre durables.           |
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | Cette interface capture un instantané de l’état actuel d’un CRM et contient un Clerk CRM spécifique.                          |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | Cette interface obtient des informations sur l’état des Clerk.                                                             |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | Cette interface analyse les enregistrements de journal individuels gérés par un Clerk CRM spécifique pour une transaction donnée.            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



