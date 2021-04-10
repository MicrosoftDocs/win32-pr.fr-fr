---
title: Repérage de références avec IDirectorySearch
description: Une référence est le mécanisme utilisé par un serveur d’annuaire pour diriger un client vers un autre serveur lorsqu’il ne contient pas suffisamment de données sur l’objet demandé par une requête.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Repérage des références avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, repérage des références
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941363"
---
# <a name="referral-chasing-with-idirectorysearch"></a><span data-ttu-id="61f96-105">Repérage de références avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="61f96-105">Referral Chasing with IDirectorySearch</span></span>

<span data-ttu-id="61f96-106">Une référence est le mécanisme utilisé par un serveur d’annuaire pour diriger un client vers un autre serveur lorsqu’il ne contient pas suffisamment de données sur l’objet demandé par une requête.</span><span class="sxs-lookup"><span data-stu-id="61f96-106">A referral is the mechanism that a directory server uses to direct a client to another server when it does not contain sufficient data about the object requested by a query.</span></span>

<span data-ttu-id="61f96-107">Dans une recherche de sous-arborescence ou de niveau unique, les références sont retournées pour les conteneurs de domaine, de schéma ou de configuration connus, immédiatement subordonnés. autrement dit, les domaines enfants qui sont des descendants directs.</span><span class="sxs-lookup"><span data-stu-id="61f96-107">In a one-level or subtree search, referrals are returned for known, immediately subordinate domain, schema, or configuration containers only; that is, child domains that are direct descendants.</span></span> <span data-ttu-id="61f96-108">Pour plus d’informations, consultez [étendue de recherche](/windows/desktop/AD/search-scope).</span><span class="sxs-lookup"><span data-stu-id="61f96-108">For more information, see [Search Scope](/windows/desktop/AD/search-scope).</span></span>

<span data-ttu-id="61f96-109">Dans un répertoire, toutes les données ne sont pas disponibles sur un serveur unique, mais elles sont distribuées sur plusieurs serveurs différents sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="61f96-109">In a directory, not all data is available on a single server, rather, it is distributed over several different servers across the network.</span></span> <span data-ttu-id="61f96-110">Si les serveurs partagent les données que d’autres serveurs peuvent fournir, ils peuvent fournir des références à un client lorsqu’une requête demandée ne peut pas être résolue sur le serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="61f96-110">If the servers share the data that other servers can provide, they can provide referrals to a client when a requested query cannot be resolved on the originating server.</span></span> <span data-ttu-id="61f96-111">Par exemple, lorsqu’un client demande au serveur A d’interroger un objet utilisateur (U), un peut suggérer que le client continue la recherche sur le serveur B si U ne réside pas sur un, mais qu’il est identifié sur B. Le client a la possibilité de poursuivre la référence.</span><span class="sxs-lookup"><span data-stu-id="61f96-111">For example, when a client asks Server A to query a user object (U), then A can suggest that the client continue the search on Server B if U does not reside on A, but is identified to be on B. The client has the choice to pursue the referral or not.</span></span> <span data-ttu-id="61f96-112">Les références permettent au client de devoir posséder une connaissance préalable de la capacité de chaque serveur, mais le client doit spécifier le type de références qu’un serveur doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="61f96-112">Referrals free the client from having to possess previous knowledge of the capability of each server, but the client must specify the type of referrals a server should perform.</span></span>

<span data-ttu-id="61f96-113">Pour activer ou désactiver le repérage de références, définissez une option de recherche de **\_ \_ \_ références Chase SEARCHPREF** pour les publicités avec une valeur **\_ entière ADSTYPE** qui contient l’une des [**\_ \_ références \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) de la recherche de recherches de publicités énumérer les valeurs d’énumération dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="61f96-113">To enable or disable referral chasing, set an **ADS\_SEARCHPREF\_CHASE\_REFERRALS** search option with an **ADSTYPE\_INTEGER** value that contains one of the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) enumeration values in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="61f96-114">L’exemple de code suivant montre comment activer les références de Chase.</span><span class="sxs-lookup"><span data-stu-id="61f96-114">The following code example shows how to enable chase referrals.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



<span data-ttu-id="61f96-115">Pour plus d’informations sur les références dans Active Directory, consultez [références](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="61f96-115">For more information about referrals in Active Directory, see [Referrals](/windows/desktop/AD/referrals).</span></span>

 

 