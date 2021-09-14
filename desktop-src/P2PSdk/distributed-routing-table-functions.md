---
description: L’API DRT (Distributed Routing Table) utilise les fonctions suivantes.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Fonctions de table de routage distribuée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013939"
---
# <a name="distributed-routing-table-functions"></a>Fonctions de table de routage distribuée

L’API DRT (Distributed Routing Table) utilise les fonctions suivantes.

## <a name="lifetime-management-functions"></a>Fonctions de gestion de la durée de vie



| Fonction                                           | Description                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen)                         | Crée une instance DRT locale à l’aide de critères spécifiés par la structure de [**\_ paramètres DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .  |
| [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose)                       | Ferme et supprime l’instance locale de DRT.                                                              |
| [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | Récupère les données d’événement associées à un événement signalé.                                                         |
| [**DrtGetEventDataSize**](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | Retourne la taille de la structure de [**\_ \_ données d’événement DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data) associée à un événement signalé. |



 

## <a name="module-management-functions"></a>Fonctions de gestion des modules



| Fonction                                                                           | Description                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtCreatePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | Crée un programme de résolution de démarrage basé sur le protocole PNRP.                                                                              |
| [**DrtDeletePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | Supprime un programme de résolution de démarrage basé sur le protocole PNRP.                                                                              |
| [**DrtCreateDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | Crée un fournisseur de démarrage qui contacte un hôte bien connu par son nom.                                                             |
| [**DrtDeleteDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | Supprime un fournisseur de démarrage qui contacte un hôte bien connu par son nom.                                                             |
| [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | Crée un transport basé sur le protocole UDP IPv6.                                                                                   |
| [**DrtDeleteIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | Supprime un transport basé sur le protocole UDP IPv6.                                                                                   |
| [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | Crée un fournisseur de sécurité de clé dérivée pour DRT.                                                                                  |
| [**DrtCreateDerivedKey**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | Crée une clé qui peut être utilisée par [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) lorsque DRT utilise un fournisseur de sécurité de clé dérivé. |
| [**DrtDeleteDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | Supprime un fournisseur de sécurité de clé dérivé pour DRT.                                                                                  |
| [**DrtCreateNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | Crée un fournisseur de sécurité null. Ce fournisseur de sécurité ne nécessite pas que les nœuds authentifient les clés.                                 |
| [**DrtDeleteNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | Supprime un fournisseur de sécurité null.                                                                                                     |



 

## <a name="registration-functions"></a>Fonctions d’inscription



| Fonction                                     | Description                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | Inscrit une clé dans DRT.                                    |
| [**DrtUpdateKey**](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | Met à jour les données d’application associées à une clé inscrite. |
| [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | Annule l’inscription d’une clé de l’DRT.                                |



 

## <a name="search-functions"></a>Fonctions de recherche



| Fonction                                                 | Description                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | Recherche une clé à l’aide de critères spécifiés dans la structure d' [**\_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .                                                                                                      |
| [**DrtContinueSearch**](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | Poursuit un \_ chemin de retour de recherche DRT \_ \_ Rechercher une clé dans le DRT. Cette fonction est utilisée uniquement lorsque l’indicateur **fIterative** est défini sur **true** dans la structure [**d' \_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) associée. |
| [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | Récupère le ou les résultats de la recherche.                                                                                                                                                                                         |
| [**DrtGetSearchResultSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | Retourne la taille du résultat de la recherche disponible suivant.                                                                                                                                                                   |
| [**DrtGetSearchPath**](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | Retourne la liste des nœuds contactés pendant l’opération de recherche.                                                                                                                                                          |
| [**DrtGetSearchPathSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | Retourne la taille du chemin de recherche, qui représente le nombre de nœuds utilisés dans l’opération de recherche.                                                                                                             |
| [**DrtEndSearch**](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | Annule la recherche d’une clé dans un objet DRT et, par conséquent, le retour des résultats via [**le \_ \_ résultat de la recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) est arrêté. Cette API peut être appelée à tout moment après l’émission d’une recherche.              |



 

## <a name="instance-name-functions"></a>Fonctions de nom d’instance



| Fonction                                                 | Description                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**DrtGetInstanceName**](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | Obtient le nom associé à une instance DRT.                    |
| [**DrtGetInstanceNameSize**](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | Retourne la taille du nom de l’instance de la table de routage distribuée. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumérations de tables de routage distribuées](distributed-routing-table-enumerations.md)
</dt> <dt>

[Structures de table de routage distribué](distributed-routing-table-structures.md)
</dt> <dt>

[Référence de API Table de routage distribué](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



