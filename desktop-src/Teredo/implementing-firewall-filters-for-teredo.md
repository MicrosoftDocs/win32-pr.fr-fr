---
title: Implémentation de filtres de pare-feu pour Teredo
description: Windows permet aux applications de définir une option de socket qui permet aux applications d’indiquer une intention explicite de recevoir le trafic Teredo envoyé au pare-feu hôte via la plateforme de filtrage Windows.
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f24d4351f10a3b37f2bf63c952e81883d97b781
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013399"
---
# <a name="implementing-firewall-filters-for-teredo"></a>Implémentation de filtres de pare-feu pour Teredo

Windows permet aux applications de définir une option de socket qui permet aux applications d’indiquer une intention explicite de recevoir le trafic Teredo envoyé au pare-feu hôte via la plateforme de filtrage Windows. dans Windows, une option de socket permettant de définir un niveau de protection est utilisée pour permettre à une application de définir le type de trafic qu’elle souhaite recevoir. Plus spécifiquement, dans les scénarios impliquant le trafic Teredo, l’option de socket de [ \_ \_ niveau de protection IPv6](/windows/desktop/WinSock/ipv6-protection-level) est spécifiée. Il est recommandé que les implémentations de pare-feu d’hôte maintiennent les filtres suivants pour autoriser de manière sélective le trafic Teredo pour une application, tout en bloquant le trafic par défaut pour toute application sans exemption.

## <a name="default-block-filter-for-edge-traversed-traffic"></a>Filtre de blocage par défaut pour le trafic traversé Edge

un pare-feu d’hôte doit toujours conserver un filtre de bloc par défaut dans la \_ \_ couche de filtrage d’authentification ALE RECV \_ ACCEPT \_ V6 pour le trafic correspondant au **type d’Interface spécifié Tunnel** et Tunnel conditions Teredo de **type** . En cas d’implémentation, ce filtre indique la présence d’un pare-feu hôte prenant en charge la traversée latérale dans le système. Ce filtre est considéré comme un contrat d’API entre le pare-feu de l’hôte et Windows. Par défaut, ce filtre bloque le trafic traversé Edge vers n’importe quelle application.

``` syntax
   filter.layerKey  = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_BLOCK;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;
   filter.weight.uint64 = 0;
   filter.flags = 0;
   filter.numFilterConditions = 2; // Or 3 depending on including the loopback condition
   filter.filterCondition = filterConditions;
   filter.displayData.name  = L"Teredo Edge Traversal Default Block";
   filter.displayData.description = L"Teredo Edge Traversal Default Block Filter.";

   // Match Interface type tunnel
   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   // Match tunnel type Teredo
   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   // Having this condition is OPTIONAL, including this will automatically exempt 
   // loopback traffic to receive Teredo.
   filterConditions[2].fieldKey = FWPM_CONDITION_FLAGS;
   filterConditions[2].matchType = FWP_MATCH_FLAGS_NONE_SET;
   filterConditions[2].conditionValue.type = FWP_UINT32;
   filterConditions[2].conditionValue.uint32 = FWP_CONDITION_FLAG_IS_LOOPBACK;
```

> [!Note]  
> Les classes « remise », « arrivée » et « tronçon suivant » des conditions d’interface sont utilisées pour contrôler un modèle d’hôte faible et le transfert de paquets entre les interfaces. L’exemple ci-dessus utilise la classe « Delivery ». Consultez les [conditions de filtrage disponibles à chaque couche de filtrage](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) dans la documentation du kit de développement logiciel (SDK) WFP, car votre conception de sécurité doit prendre en considération chaque cas.

 

## <a name="allow-filter-for-exempt-applications"></a>Autoriser le filtre pour les applications exemptes

Si une application est exempte de la réception du trafic Teredo sur un socket d’écoute, un filtre d’autorisation doit être implémenté dans la \_ \_ couche de \_ filtrage V6 d’authentification ALE Accept \_ V6 sur le pare-feu hôte. Il est important de noter que, en fonction de la façon dont l’exemption est configurée par l’utilisateur ou l’application, le pare-feu hôte peut inclure une option de Socket.

``` syntax
   filter.layerKey   = FWPM_LAYER_ALE_AUTH_RCV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_PERMIT;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64= 1; // Use a weight higher than the default block
   filter.flags = 0;
   filter.numFilterConditions = 3; // Or 4 depending on the socket option based condition
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal Allow Application A";
   filter.displayData.description = L"Teredo Edge Traversal Allow Application A Filter.";

   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[2].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[2].matchType = FWP_MATCH_EQUAL;
   filterConditions[2].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[2].conditionValue.byteBlob = &byteBlob;
   filterConditions[2].conditionValue.byteBlob->data = (uint8 *) wszApplicationA;
   filterConditions[2].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[3].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[3].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[3].conditionValue.type = FWP_UINT32;
   filterConditions[3].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

## <a name="dormancy-callout-filter"></a>Filtre de légende latence

le service Teredo dans Windows implémente un modèle latence. À un moment donné, si aucune application n’écoute sur un socket UDP ou TCP pour lequel la traversée latérale est activée, le service passe à un état dormant. Pour que le mécanisme latence fonctionne, le pare-feu hôte doit conserver un filtre de légende pour chaque application exempte spécifiée dans la \_ \_ \_ couche de filtrage V6 d’écoute de l’authentification ALE pour TCP et la \_ \_ couche de filtrage V6 d’affectation de ressources ALE \_ pour les applications basées sur UDP. L’exemple suivant illustre une légende latence pour une application **TCP** .

``` syntax
   filter.layerKey = FWPM_LAYER_ALE_AUTH_LISTEN_V6;
   // Use FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.action.type = FWP_ACTION_CALLOUT_TERMINATING;
   filter.action.calloutKey = FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6;
   // Use FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64 = 1;
   filter.flags = 0;
   filter.numFilterConditions = 1; // 2 if including the socket option based condition 
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal dormancy callout for app A";
   filter.displayData.description = L"Teredo Edge Traversal dormancy callout filter for A.";

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[0].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[0].conditionValue.byteBlob = &byteBlob;
   filterConditions[0].conditionValue.byteBlob->data = (uint8 *)wszApplicationA;
   filterConditions[0].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[1].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[1].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

 

 