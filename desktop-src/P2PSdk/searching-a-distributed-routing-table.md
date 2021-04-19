---
description: Pour qu’une application puisse effectuer une recherche dans la table de routage distribué (DRT), une requête de recherche doit être créée.
ms.assetid: b3403a64-128c-461e-9384-8e62c03322e1
title: Recherche dans une table de routage distribuée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9977ca395393cef09198182fb8790738d2b00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529334"
---
# <a name="searching-a-distributed-routing-table"></a>Recherche dans une table de routage distribuée

Pour qu’une application puisse effectuer une recherche dans la table de routage distribué (DRT), une requête de recherche doit être créée. La valeur de clé souhaitée est spécifiée par l’application lorsque la fonction [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) est appelée. Le comportement de la recherche est déterminé par les informations spécifiées par l’application dans la structure d' [**\_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .

En règle générale, un événement d’application est signalé lorsque la recherche Découvre les résultats et un autre à la fin de la recherche. Toutefois, si **fIterative** est défini dans [**\_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info), un événement d’application peut être signalé lorsque le contact est établi avec chaque nœud en cours de route.

Une fois qu’un événement est signalé, l’application appelle ensuite la fonction [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) pour obtenir les résultats. Si le code retourné est **S \_ OK**, les résultats sont signalés dans la structure de [**\_ \_ résultat de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) retournée par l’API. Les résultats retournés sont dans la plage de valeurs spécifiée dans [**\_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info). Si la recherche ne trouve aucune correspondance, seule la valeur **DRT \_ E n' \_ est \_ pas** retournée à la fin des retours de résultats.

Les informations suivantes détaillent comment les membres contenus dans les [**\_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) permettent à une application de dicter spécifiquement le comportement de recherche de l’infrastructure DRT :

## <a name="fallowcurrentinstancematch"></a>fAllowCurrentInstanceMatch

Par défaut, les résultats de la recherche DRT incluent uniquement les correspondances trouvées en dehors du nœud local. La définition de **fAllowCurrentInstanceMatch** spécifie que les résultats de la recherche incluent également les correspondances trouvées dans l’instance DRT locale.

## <a name="cmaxendpoints"></a>cMaxEndpoints

La quantité et la plage des résultats retournés par la recherche sont spécifiées par l’application avec les valeurs **cMaxEndpoints** (Quantity) et **pMinimumKey** et **pMaximumKey** (Range), et référencées par les [**\_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info).

Lorsque **cMaxEndpoints = 1**, l’infrastructure DRT recherche une clé, en retournant une correspondance dans la plage spécifiée par les valeurs **pMinimumKey** et **pMaximumKey** dans les [**\_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info). Cette correspondance peut être une correspondance exacte ou la correspondance la plus proche dans la plage. Si aucune correspondance n’est trouvée, le **DRT \_ E \_ n' \_** est pas retourné.

Si **cMaxEndpoints > 1**, l’infrastructure DRT retourne des correspondances dans la plage jusqu’à la valeur de **cMaxEndpoints**. Les correspondances retournées peuvent contenir une correspondance exacte ou les résultats de correspondance les plus proches dans la plage. En outre, si **pMinimumKey** et **pMaximumKey** sont définis sur la même valeur, une recherche est effectuée uniquement pour cette valeur, en renvoyant le **DRT \_ E \_ \_** uniquement s’il est introuvable.

## <a name="fanymatchinrange"></a>fAnyMatchInRange

Le membre **fAnyMatchInRange** indique si la recherche s’arrêtera une fois la première correspondance trouvée dans la plage spécifiée, ou si la recherche se poursuivra pour la correspondance la plus proche de la clé spécifiée dans l’API [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) . Lorsque **fAnyMatchInRange** est défini, la recherche est effectuée avec **cMaxEndpoints = 1** , quelle que soit la valeur spécifiée de **cMaxEndpoints** dans les [**\_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info).

## <a name="fiterative"></a>fIterative

Le membre **fIterative** spécifie si chaque nœud contacté par l’infrastructure DRT pendant la recherche aura les données de clé/point de terminaison qui lui sont associées, accessibles à l’application via le résultat de la [**\_ recherche \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result). En affectant à **fIterative** la valeur **true**, la valeur de **cMaxEndpoints = 1** est forcée. Lorsque **fIterative** a la valeur **true** dans une requête de recherche pour l’objet DRT, l’application est rappelée après le contact avec chaque nœud ou « tronçon ». Chaque résultat de tronçon contient une clé indiquant le nœud que le DRT recherchera ensuite. Un résultat de tronçon est retourné via [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) sous la forme d’un résultat **\_ \_ intermédiaire de correspondance DRT** .

## <a name="pminimumkey-and-pmaximumkey"></a>pMinimumKey et pMaximumKey

Les membres **pMinimumKey** et **pMaximumKey** peuvent être utilisés pour rechercher des clés comprises dans une plage. Si le membre **fAnyMatchInRange** a la valeur **false**, l’objet DRT retourne la ou les clés les plus proches à la cible de recherche (spécifiée à l’aide de l’argument de la clé de page passée dans la fonction [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) ) comprise dans la plage. Notez que l' *argument de* grand-groupe transmis à **DrtStartSearch** doit être compris dans la plage définie par **pMinimumKey** et **pMaximumKey**. Pour rechercher une clé précise, attribuez la même valeur à **pMinimumKey**, **pMaximumKey** *et au* jeu de clés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription et annulation de l’inscription des clés](registering-and-deregistering-keys.md)
</dt> <dt>

[À propos des tables de routage distribuées](about-distributed-routing-tables.md)
</dt> <dt>

[Référence de API Table de routage distribué](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



