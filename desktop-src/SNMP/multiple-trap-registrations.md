---
title: Enregistrements d’interruptions multiples
description: Plusieurs options sont disponibles lorsqu’une application WinSNMP inscrit une session WinSNMP pour les interruptions ou les notifications.
ms.assetid: 76a4095f-ab5c-4f7a-9b60-a383a632fd65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2149e4ac1e9880601ae64718cd78991718d54a6228488a03e593376d9a7937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009326"
---
# <a name="multiple-trap-registrations"></a>Enregistrements d’interruptions multiples

Plusieurs options sont disponibles lorsqu’une application WinSNMP inscrit une session WinSNMP pour les interruptions ou les notifications. Pour cette raison, une application peut appeler la fonction [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) plusieurs fois, en définissant un filtre personnalisé pour la réception des interruptions et des notifications. Par exemple, vous pouvez vous inscrire pour un type d’interruption ou de notification, ou pour toutes les interruptions et notifications, selon la valeur du paramètre de *notification* . En outre, l’application peut spécifier des valeurs dans d’autres paramètres de la fonction **SnmpRegister** pour définir plus précisément les interruptions et les notifications qui doivent atteindre une application. Pour plus d’informations, consultez [gestion des interruptions et des notifications](managing-traps-and-notifications.md).

Voici les instances dans lesquelles plusieurs appels à **SnmpRegister** sont redondants. Dans ces instances, **SnmpRegister** retourne SNMPAPI \_ Success si la fonction se termine correctement, mais l’inscription redondante est inefficace.

1.  Appel à la fonction [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) qui demande la remise filtrée des interruptions et des notifications à la session, après un appel précédent à **SnmpRegister** demandant la remise de toutes les interruptions et notifications (remise non filtrée). Cet appel est redondant, car la session reçoit déjà toutes les interruptions et notifications, y compris le type unique défini par le filtre.
2.  Appel dupliqué à **SnmpRegister**, ou dans lequel la liste de paramètres est identique à la liste de paramètres dans un appel précédent à **SnmpRegister** pour la session.
3.  Appel à la fonction [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) qui demande la remise filtrée d’interruptions et de notifications basées sur un identificateur d’objet (OID) dont le préfixe est un OID spécifié dans un appel précédent à **SnmpRegister**. Par exemple, vous pouvez spécifier « 1.3.6.1.4.1.311 » dans le paramètre de *notification* pour recevoir des notifications provenant d’une entité de l’agent Microsoft SNMP. Si vous renommez **SnmpRegister** et spécifiez « 1.3.6.1.4.1.311.1 », le deuxième appel est redondant, car la session reçoit déjà toutes les interruptions et notifications qui contiennent le préfixe OID « 1.3.6.1.4.1.311 ».

Pour annuler l’inscription de la session, vous devez faire correspondre chaque appel d’inscription unique à la fonction [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) . Appelez **SnmpRegister** pour annuler l’inscription de la session et assurez-vous que les cinq premiers paramètres de **SnmpRegister** sont identiques à ceux de l’appel d’inscription initial. La seule différence entre l’appel initial et l’annulation de l’inscription est que, lors de l’inscription, vous devez spécifier la valeur SNMPAPI \_ dans le paramètre *Status* , et lorsque vous appelez la fonction pour annuler l’inscription, vous devez spécifier SNMPAPI \_ off. Vous n’avez pas besoin de faire correspondre les appels d’inscription redondants à la fonction **SnmpRegister** . Vous devez uniquement faire correspondre le premier appel d’inscription unique.

Pour modifier des critères de filtrage, il peut être nécessaire pour une application d’annuler son inscription et de désactiver la remise de certaines interruptions ou notifications. L’application peut ensuite créer un nouveau filtre en appelant [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), en transmettant les valeurs appropriées.

 

 




