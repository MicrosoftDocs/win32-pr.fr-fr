---
description: L’infrastructure CRM fournit un ensemble d’interfaces qui peuvent être utilisées pour analyser les CRM au sein d’une application serveur particulière.
ms.assetid: b8f40c91-001b-4003-b377-57a918988100
title: Interfaces d’analyse CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c893040c46810c980c647cbacdc808200e8d5f5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403551"
---
# <a name="com-crm-monitoring-interfaces"></a>Interfaces d’analyse CRM COM+

L’infrastructure CRM fournit un ensemble d’interfaces qui peuvent être utilisées pour analyser les CRM au sein d’une application serveur particulière. Pour accéder aux interfaces de surveillance, un composant qui s’exécute dans l’application serveur doit d’abord créer un Clerk CRM spécialisé appelé « Clerk Recovery Clerk ».

Dans le cas d’une utilisation normale de CRM, les transactions sont supposées être éphémères et, par conséquent, les Workers CRM et les compensateurs CRM existent pendant une courte période, en général seulement quelques secondes. Par conséquent, les interfaces de surveillance sont conçues pour fournir un instantané de l’état des CRM en cours d’exécution à un moment donné. Si l’un des CRM rencontre des problèmes, les interfaces de surveillance peuvent être utilisées pour se trouver à zéro dans sur le CRM gênant, pour inspecter ses enregistrements de journal et pour abandonner sa transaction si nécessaire.

Voici les trois interfaces d’analyse CRM et les descriptions de leur fonctionnement.



| Interface                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)<br/>                     | À l’aide de [**ICrmMonitor :: GetClerks**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-getclerks), un instantané peut être obtenu de l’ensemble actuel des Clerk CRM actifs au sein de l’application serveur. À partir de ce, un objet de collection de Clerk CRM particulier digne d’intérêt peut être localisé et interrogé, y compris l’état actuel de sa transaction et les enregistrements de journal écrits par le CRM.<br/> Lorsque l’outil de surveillance a déterminé quel Clerk est digne d’intérêt, il appelle [**ICrmMonitor :: HoldClerk**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-holdclerk) pour recevoir une interface [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) sur ce Clerk particulier. À ce stade, l’outil de surveillance détient une référence à ce Clerk et, si la transaction se termine, le régisseur est conservé en mémoire et n’est pas libéré tant que l’outil de surveillance n’est pas terminé.<br/>                                                                                                                                                                                                    |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)<br/>         | À l’aide de cette interface, l’objet de collection Clerk peut être parcouru pour obtenir des informations sur l’état de la collection Clerk au moment où elle a été obtenue. Ces informations incluent le nombre d’employés, le ProgID du compensateur CRM utilisé par le Clerk, la description fournie au moment de l’inscription du compensateur CRM (à l’aide de [**ICrmLogControl :: RegisterCompensator**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator)), l’ID d’unité de travail de la transaction et l’ID d’activité. Les employés individuels sont également identifiés de manière unique par un « CLSID d’instance du Clerk », qui n’est pas un CLSID COM au sens habituel du terme, mais simplement un GUID unique qui identifie ce Clerk en particulier pour sa durée de vie.<br/>                                                                                                                                                                                                                                                                                                |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)<br/> | Cette interface peut être utilisée pour interroger l’état actuel de la transaction, pour connaître le nombre d’enregistrements de journal écrits par le Clerk CRM et pour obtenir les données d’enregistrement de journal réelles. Les enregistrements de journal sont fournis à partir de l’interface [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) dans le même format que celui dans lequel ils ont été écrits à l’origine (à l’aide de [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)). En outre, les **ICrmMonitorLogRecords** peuvent éventuellement être implémentés pour convertir les enregistrements de journal au format affichable, de sorte qu’ils puissent être présentés à l’aide d’un outil d’analyse générique.<br/> Étant donné que [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) est implémenté directement sur le Clerk CRM, vous pouvez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) (également implémenté sur le Clerk CRM). Il peut ensuite être utilisé pour abandonner directement la transaction si nécessaire ([**ICrmLogControl :: ForceTransactionToAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcetransactiontoabort)).<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

