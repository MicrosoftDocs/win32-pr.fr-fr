---
title: À propos de la gestion de routeur avec MIB
description: Les API MIB (Management Information base) pour la gestion de routeur permettent d’interroger et de définir les valeurs des variables MIB exportées par l’un des gestionnaires de routeur ou l’un des protocoles de routage utilisés par le service gestionnaires de routeur.
ms.assetid: d0fafd82-e7cb-4524-a499-d14830f02b21
keywords:
- Routage, base d’informations de gestion
- Routage, base d’informations de gestion, Description
- Service RRAS de base d’informations de gestion
- MIB
- MIB, voir base d’informations de gestion
- Service RRAS de base d’informations de gestion
- Informations de gestion service RRAS, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a867d903e0fb79f9360dc5f1cb485040ed4489b328365bc2daa063a35fbe27d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792194"
---
# <a name="about-router-management-with-mib"></a>À propos de la gestion de routeur avec MIB

Les API MIB (Management Information base) pour la gestion de routeur permettent d’interroger et de définir les valeurs des variables MIB exportées par l’un des gestionnaires de routeur ou l’un des protocoles de routage utilisés par le service gestionnaires de routeur. À l’aide de cette API, le routeur prend en charge le protocole SNMP (simple Network Management Protocol).

Dans l’infrastructure SNMP, chacun des objets gérables dans le routeur est représenté par une variable qui a un identificateur d’objet (OID) unique. Correspondant à chaque OID est une valeur qui représente l’état actuel de l’objet. La collection d’OID et de valeurs est appelée MIB (Management Information base). Les appels MprAdminMib permettent à un développeur de spécifier un objet par son OID et de demander ou d’écrire (« définir ») la valeur de l’objet.

Pour interroger et définir des variables MIB, le module qui services les appels doit définir un ensemble de structures de données. Ces structures de données incluent des structures à utiliser comme identificateurs et structures d’objets qui contiennent les valeurs des variables MIB en cours d’accès. Ces structures de données sont opaques à tous, sauf l’appelant de la fonction MIB et le module traitant l’appel.

Le module traitant l’appel MIB est un gestionnaire de routeur ou un des protocoles de routage. L’appelant doit spécifier un gestionnaire de routeur même si l’appel est géré par l’un des protocoles de routage. Dans ce cas, l’appelant doit spécifier le gestionnaire de routeur qui correspond à la famille de protocoles pour ce protocole de routage. Par exemple, si le protocole de routage OSPF (Open Shortest Path First) utilisait l’appel MIB, l’appelant devra spécifier le gestionnaire de routeur IP, puisque le protocole OSPF appartient à la famille de protocoles IP. Dans chacune des fonctions MIB, le paramètre *dwTransportId* spécifie un gestionnaire de routeur et le paramètre *RoutingPid* spécifie le protocole de routage. Le gestionnaire de routeur possède également un *RoutingPid* unique, car certaines des variables MIB peuvent être gérées par le gestionnaire de routeur lui-même.

Les fonctions MprAdminMib peuvent être appelées sur un ordinateur autre que celui qui est administré. Les fonctions MprAdminMIB qui interrogent ou écrivent des valeurs prennent comme paramètre un handle vers l’ordinateur à administrer. Utilisez la fonction [**MprAdminMIBServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverconnect) pour établir la connexion à l’ordinateur distant et obtenir ce descripteur. Après avoir appelé les fonctions MprAdminMIB nécessaires pour accomplir une tâche administrative particulière, appelez la fonction [**MprAdminMIBServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverdisconnect) pour mettre fin à la connexion à l’ordinateur distant.

Les fonctions [**MprAdminMIBEntryCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrycreate) et [**MprAdminMIBEntrySet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryset) prennent comme paramètres un OID et une mémoire tampon qui contient la nouvelle valeur de l’objet.

Les fonctions [**MprAdminMIBEntryGet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget), [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) et [**MPRADMINMIBENTRYGETNEXT**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) prennent comme paramètres un OID et l’adresse d’une variable pointeur. En cas de retour correct, la variable pointeur pointe vers une mémoire tampon qui contient la valeur de l’objet. L’appelant doit libérer la mémoire pour ce tampon en appelant la fonction [**MprAdminMIBBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibbufferfree) .

Les fonctions [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) et [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) permettent à un développeur d’effectuer un *parcours SNMP*. Étant donné que les OID sont triés, chaque OID et, par conséquent, chaque objet gérable possède un OID *suivant* . Un parcours SNMP fait référence à la traversée d’une partie de la MIB en lisant ou en écrivant une séquence d’OID.

Tous les appels MprAdminMib passent par le gestionnaire d’interface dynamique (DIM). Selon l’OID, DIM passe l’appel à l’un des gestionnaires de routeur. (IP et IPX prennent en charge SNMP). Là encore, en fonction de l’OID, le gestionnaire de routeur peut traiter l’appel lui-même ou passer l’appel à l’un de ses clients. Tous les clients de routeur sont requis pour implémenter et exporter les fonctions suivantes qui correspondent aux fonctions MprAdminMIB nommées de la même façon :

-   [**MibCreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)
-   [**MibDelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)
-   [**MibSet**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)
-   [**MibGet**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)
-   [**MibGetFirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)
-   [**MibGetNext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)
-   [**MibGetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)
-   [**MibSetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

 

 




