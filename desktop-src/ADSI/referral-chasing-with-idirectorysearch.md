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
# <a name="referral-chasing-with-idirectorysearch"></a>Repérage de références avec IDirectorySearch

Une référence est le mécanisme utilisé par un serveur d’annuaire pour diriger un client vers un autre serveur lorsqu’il ne contient pas suffisamment de données sur l’objet demandé par une requête.

Dans une recherche de sous-arborescence ou de niveau unique, les références sont retournées pour les conteneurs de domaine, de schéma ou de configuration connus, immédiatement subordonnés. autrement dit, les domaines enfants qui sont des descendants directs. Pour plus d’informations, consultez [étendue de recherche](/windows/desktop/AD/search-scope).

Dans un répertoire, toutes les données ne sont pas disponibles sur un serveur unique, mais elles sont distribuées sur plusieurs serveurs différents sur le réseau. Si les serveurs partagent les données que d’autres serveurs peuvent fournir, ils peuvent fournir des références à un client lorsqu’une requête demandée ne peut pas être résolue sur le serveur d’origine. Par exemple, lorsqu’un client demande au serveur A d’interroger un objet utilisateur (U), un peut suggérer que le client continue la recherche sur le serveur B si U ne réside pas sur un, mais qu’il est identifié sur B. Le client a la possibilité de poursuivre la référence. Les références permettent au client de devoir posséder une connaissance préalable de la capacité de chaque serveur, mais le client doit spécifier le type de références qu’un serveur doit effectuer.

Pour activer ou désactiver le repérage de références, définissez une option de recherche de **\_ \_ \_ références Chase SEARCHPREF** pour les publicités avec une valeur **\_ entière ADSTYPE** qui contient l’une des [**\_ \_ références \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) de la recherche de recherches de publicités énumérer les valeurs d’énumération dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

L’exemple de code suivant montre comment activer les références de Chase.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



Pour plus d’informations sur les références dans Active Directory, consultez [références](/windows/desktop/AD/referrals).

 

 