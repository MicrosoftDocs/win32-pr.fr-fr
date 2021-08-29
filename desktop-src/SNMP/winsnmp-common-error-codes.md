---
title: Codes d’erreur courants WinSNMP
description: La fonction SnmpGetLastError peut retourner un code d’erreur général après l’échec d’une fonction WinSNMP. Le tableau suivant répertorie les codes d’erreur les plus courants de l’WinSNMP.
ms.assetid: c286750f-a542-4f61-a22c-d77debd45775
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37550478b37cdc75c2dea427e54b4d9d3d52dcc838273a09cf904cd4479baa4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142952"
---
# <a name="winsnmp-common-error-codes"></a>Codes d’erreur courants WinSNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

La fonction [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) peut retourner un code d’erreur général après l’échec d’une fonction winsnmp. Le tableau suivant répertorie les codes d’erreur les plus courants de l’WinSNMP.



| Code d'erreur                | Signification                                                                                                                                                                                                        | Action recommandée                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ non \_ initialisé | La fonction [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) n’a pas été exécutée correctement depuis le début de l’exécution du programme, ou depuis la réussite d’un appel à la fonction [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) . | L’application doit appeler [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) avant d’appeler toute autre fonction API WinSNMP lorsque [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) échoue. La fonction [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) retourne des informations d’erreur étendues sur l’échec de [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup).                                                          |
| \_erreur d’allocation SNMPAPI \_     | L’application a spécifié un pointeur non valide, ou une erreur s’est produite lors de l’allocation de mémoire. L’implémentation Microsoft WinSNMP n’a pas pu obtenir suffisamment de ressources pour exécuter la demande.                | L’application doit fournir des pointeurs de mémoire valides pour tous les paramètres de sortie. Il doit libérer des ressources, réduire les besoins en ressources, ou faciliter un arrêt approprié. Un arrêt approprié comprend plusieurs appels à la fonction [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) , un pour chaque session WinSNMP ouverte. Il comprend également un appel à la fonction [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) . |
| SNMPAPI \_ NOOP             | La fonction ne s’est pas terminée correctement, car tous les paramètres de sortie ont la **valeur null**.                                                                                                                         | L’application doit spécifier au moins un paramètre de sortie qui n’a pas la **valeur null** lors de l’appel d’une fonction qui retourne des informations à l’application.                                                                                                                                                                                                                                  |
| SNMPAPI \_ autre \_ erreur     | Une erreur inconnue ou non définie s’est produite.                                                                                                                                                                        | L’application doit généralement répondre avec un arrêt approprié. Un arrêt approprié comprend plusieurs appels à la fonction [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) , un pour chaque session WinSNMP ouverte. Il comprend également un appel à la fonction [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) .                                                                                                           |



 

Les erreurs WinSNMP qui transmettent des informations spécifiques au contexte sont indiquées dans la page de référence de chaque fonction.

 

 