---
title: Tri des résultats de la recherche avec IDirectorySearch
description: Par défaut, les résultats d’une recherche sont retournés dans aucun ordre garanti. La \_ préférence SEARCHPREF \_ \_ de tri des publicités indique au serveur de trier le jeu de résultats sur une valeur d’attribut spécifiée avant qu’il ne soit retourné au client.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Tri des résultats de la recherche avec IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, tri des résultats de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730237"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a>Tri des résultats de la recherche avec IDirectorySearch

Par défaut, les résultats d’une recherche sont retournés dans aucun ordre garanti. La **préférence \_ SEARCHPREF \_ \_ de tri des publicités** indique au serveur de trier le jeu de résultats sur une valeur d’attribut spécifiée avant qu’il ne soit retourné au client.

Il est recommandé d’utiliser des attributs indexés pour le tri. Dans le cas contraire, le serveur doit récupérer le jeu de résultats complet et le trier avant d’envoyer les résultats au client. Cela s’applique également aux recherches paginées. Sachez que les performances d’une recherche triée sont augmentées si le filtre comprend un attribut indexé et que cet attribut est spécifié comme clé de tri. dans ce cas, Active Directory peut satisfaire le tri lors du traitement du filtre. Par exemple, une requête de tri efficace pour un ensemble d’utilisateurs peut avoir un filtre inclus (SN>Smith) et une clé de tri SN.

Le tri côté serveur à l’aide de l’option **\_ \_ \_ de tri SEARCHPREF ADS sur** la recherche permet de réduire les performances du serveur. Si vous effectuez de nombreuses recherches, envisagez de trier les résultats manuellement du côté client afin de réduire la charge de travail sur le serveur.

Par défaut, le tri des résultats est désactivé. Pour activer le tri des résultats, définissez un **\_ SEARCHPREF ADS \_ \_ sur** l’option de recherche avec un **ADSTYPE \_ Prov \_ spécifique** qui pointe vers une structure de type de clé ( [**\_ SortKey**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) ) ads dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . La **structure \_ SortKey ADS** est utilisée pour spécifier l’attribut à utiliser pour le tri et l’ordre de tri.

L’exemple de code suivant montre comment activer le tri des résultats.


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



Active Directory ne prend pas en charge le tri sur les attributs construits, il n’est donc pas possible de spécifier un attribut construit pour le tri. L’attribut [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) ne peut pas non plus être utilisé pour le tri. Active Directory ne permet pas non plus d’effectuer un tri sur plusieurs attributs, l’option SEARCHPREF de l’option Trier sur les publicités ne peut donc contenir qu’une [**seule structure \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) **\_ \_ \_ de type de clé** .

 

 