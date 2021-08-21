---
description: Le \_ schéma de profil WLAN définit les éléments suivants.
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: Éléments de schéma WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ceac5f857e7b9bef51f4c8f527afe90f46f506f445eaf4fe1ef50670a090a7aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984449"
---
# <a name="wlan_profile-schema-elements"></a>\_Éléments de schéma de profil WLAN

Le \_ schéma de profil WLAN définit les éléments suivants. La plupart des éléments se trouvent dans l’espace de noms `https://www.microsoft.com/networking/WLAN/profile/v1` , à l’exception de [**FipsMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), qui se trouve dans l’espace de noms `https://www.microsoft.com/networking/WLAN/profile/v2` .

La liste suivante présente les éléments définis dans l’ordre dans lequel les éléments apparaissent dans un profil. L’ordre des éléments est appliqué. Tous les éléments ne se trouvent pas dans chaque profil, car certains éléments sont facultatifs.

Cette liste n’affiche pas tous les éléments possibles qui peuvent apparaître dans un profil sans fil, car des éléments peuvent être ajoutés dans **XS : n’importe quel** point d’insertion.

-   [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
    -   [**nom (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)
    -   [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [**hex (SSID)**](wlan-profileschema-hex-ssid-element.md)
            -   [**nom (SSID)**](wlan-profileschema-name-ssid-element.md)
        -   [**dédiffusion (SSIDConfig)**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [**Hotspot2 (WLANProfile)**](wlan-profileschema-hotspot2-element.md)
        -   [**Nom_domaine (Hotspot2)**](wlan-profileschema-hotspot2-domainname-element.md)
        -   [**NAIRealm (Hotspot2)**](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [**Network3GPP (Hotspot2)**](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [**RoamingConsortium (Hotspot2)**](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [**connectionType (WLANProfile)**](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [**connectionMode (WLANProfile)**](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [**AutoSwitch (WLANProfile)**](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
        -   [**connectivité (MSM)**](wlan-profileschema-connectivity-msm-element.md)
            -   [**phyType (connectivité)**](wlan-profileschema-phytype-connectivity-element.md)
        -   [**sécurité (MSM)**](wlan-profileschema-security-msm-element.md)
            -   [**authEncryption (sécurité)**](wlan-profileschema-authencryption-security-element.md)
                -   [**authentification (authEncryption)**](wlan-profileschema-authentication-authencryption-element.md)
                -   [**chiffrement (authEncryption)**](wlan-profileschema-encryption-authencryption-element.md)
                -   [**useOneX (authEncryption)**](wlan-profileschema-useonex-authencryption-element.md)
                -   [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [**sharedKey (sécurité)**](wlan-profileschema-sharedkey-security-element.md)
                -   [**KeyType (sharedKey)**](wlan-profileschema-keytype-sharedkey-element.md)
                -   [**protégé (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)
                -   [**Matériel de sharedKey**](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [**KeyIndex (sécurité)**](wlan-profileschema-keyindex-security-element.md)
            -   [**PMKCacheMode (sécurité)**](wlan-profileschema-pmkcachemode-security-element.md)
            -   [**PMKCacheTTL (sécurité)**](wlan-profileschema-pmkcachettl-security-element.md)
            -   [**PMKCacheSize (sécurité)**](wlan-profileschema-pmkcachesize-security-element.md)
            -   [**preAuthMode (sécurité)**](wlan-profileschema-preauthmode-security-element.md)
            -   [**preAuthThrottle (sécurité)**](wlan-profileschema-preauththrottle-security-element.md)
    -   [**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [**OUIHeader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
            -   [**OUI (OUIHeader)**](wlan-profileschema-oui-ouiheader-element.md)
            -   [**type (OUIHeader)**](wlan-profileschema-type-ouiheader-element.md)
        -   [**connectivité (IHV)**](wlan-profileschema-connectivity-ihv-element.md)
        -   [**sécurité (IHV)**](wlan-profileschema-security-ihv-element.md)
        -   [**useMSOneX (IHV)**](wlan-profileschema-usemsonex-ihv-element.md)

 

 



