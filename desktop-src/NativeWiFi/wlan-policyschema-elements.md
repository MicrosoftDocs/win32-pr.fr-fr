---
description: Un profil de stratégie de réseau local sans fil Wi-Fi (WLAN) natif se compose des éléments de schéma suivants.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: Éléments de schéma WLAN_policy
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92bfca66e1eff2c8c180968c83b5dbb565d1d4aa27ace1ba89d1c70634d6e7b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619544"
---
# <a name="wlan_policy-schema-elements"></a>\_Éléments du schéma de stratégie WLAN

Un profil de stratégie de réseau local sans fil Wi-Fi (WLAN) natif se compose des éléments de schéma suivants. Tous les éléments nommés se trouvent dans l’espace de noms `https://www.microsoft.com/networking/WLAN/policy/v1` .

La liste suivante présente les éléments définis dans l’ordre dans lequel les éléments apparaissent dans un profil. L’ordre des éléments est appliqué. Tous les éléments ne se trouvent pas dans chaque profil, car certains éléments sont facultatifs.

Cette liste n’affiche pas tous les éléments possibles qui peuvent apparaître dans un profil, car des éléments peuvent être ajoutés dans **XS : n’importe quel** point d’insertion.

-   [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
    -   [**nom (WLANPolicy)**](wlan-policyschema-name-wlanpolicy-element.md)
    -   [**Description (WLANPolicy)**](wlan-policyschema-description-wlanpolicy-element.md)
    -   [**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [**enableAutoConfig (globalFlags)**](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [**showDeniedNetwork (globalFlags)**](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [**allowEveryoneToCreateAllUserProfiles (globalFlags)**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [**allowList (networkFilter)**](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [**réseau (allowList)**](wlan-policyschema-network-allowlist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**Blocage (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [**réseau (de blocage)**](wlan-policyschema-network-blocklist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**denyAllIBSS (networkFilter)**](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [**denyAllESS (networkFilter)**](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [**profileList (WLANPolicy)**](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



