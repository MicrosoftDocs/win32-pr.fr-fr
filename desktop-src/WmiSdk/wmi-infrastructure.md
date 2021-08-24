---
description: Dans l’infrastructure WMI, le service WMI (WinMgmt) est le composant du système d’exploitation qui agit en tant que médiateur entre les applications de gestion et les fournisseurs de données WMI. Le référentiel WMI est une zone de stockage pour les données statiques relatives à WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Infrastructure WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bc4492c7d26f422705863609a2e0ec19af5eb930e0aa80f4fd8bb8c26bea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757329"
---
# <a name="wmi-infrastructure"></a>Infrastructure WMI

Dans l’infrastructure WMI, le service WMI (WinMgmt) est le composant du système d’exploitation qui agit en tant que médiateur entre les applications de gestion et les [*fournisseurs*](gloss-p.md)de données WMI. Le [*référentiel WMI*](gloss-w.md) est une zone de stockage pour les données statiques relatives à WMI.

Le service WMI est implémenté en tant que processus de service au sein d’un processus hôte de service partagé (SVCHOST). Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

Le service WMI démarre lorsque la première application ou le script de gestion effectue un appel pour se connecter à un espace de noms WMI. Selon la configuration, le service WMI peut s’arrêter ou passer à un profil de mémoire insuffisante lorsqu’il n’est pas appelé par une application de gestion.

Le service WMI interagit avec les applications de gestion par le biais de l’interface COM. Lorsqu’une application effectue une requête via l’interface, WMI détermine si la requête concerne des données statiques ou dynamiques. Si la requête implique des données statiques, telles que le nom d’un objet géré, WMI récupère les données du référentiel. Si la requête implique des données dynamiques, telles que la quantité de mémoire qu’un objet managé utilise actuellement, WMI transmet la demande à un fournisseur.

Les fournisseurs inscrivent leur emplacement auprès du service WMI, qui permet à WMI d’acheminer les demandes de données. Un fournisseur enregistre également la prise en charge de certaines opérations, telles que la récupération de données, la modification, la suppression, l’énumération ou le traitement des requêtes. Le service WMI utilise les informations d’inscription du fournisseur pour faire correspondre les demandes d’application avec le fournisseur approprié. WMI utilise également les informations d’inscription pour charger et décharger les fournisseurs, si nécessaire. Lorsqu’un fournisseur termine le traitement d’une demande, le fournisseur renvoie le résultat au service WMI. WMI transmet ensuite le résultat à l’application par le biais de l’interface COM. Pour plus d’informations, consultez [fourniture de données à WMI](providing-data-to-wmi.md).

WMI utilise [le suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW) pour enregistrer l’activité du service WMI.

Étant donné que l’infrastructure gère tout le trafic entre les fournisseurs et les applications de gestion, l’infrastructure fournit les fonctionnalités suivantes :

-   Prise en charge des notifications d’événements

    Pour plus d’informations, consultez [surveillance des événements](monitoring-events.md).

-   Prise en charge du langage de requête

    Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).

-   Support sécurité

    Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).

-   Écriture de scripts pour l’accès aux données des compteurs de performances

    Pour plus d’informations, consultez [analyse des données de performances](monitoring-performance-data.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Architecture WMI](wmi-architecture.md)
</dt> </dl>

 

 
