---
description: en raison des différences architecturales sous-jacentes dans le système d’exploitation, Windows xp avec service pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec service pack 2 (SP2) ne prennent en charge qu’un sous-ensemble des éléments décrits dans le \_ schéma de profil WLAN et la documentation de référence du schéma OneX.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilité avec le profil sans fil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36db0ecea6f85341d904603c99308ec10e79cee20d7567160cd3beee3b13c35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684569"
---
# <a name="wireless-profile-compatibility"></a>Compatibilité avec le profil sans fil

en raison des différences architecturales sous-jacentes dans le système d’exploitation, Windows xp avec service pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec service pack 2 (SP2) ne prennent en charge qu’un sous-ensemble des éléments décrits dans le [ \_ schéma de profil WLAN](wlan-profileschema-schema.md) et la documentation de référence du [schéma OneX](onexschema-schema.md) .

tous les profils conformes à Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 peuvent également être utilisés sur Windows Vista et Windows Server 2008.

## <a name="wlan_profile-support"></a>\_Prise en charge du profil WLAN

les éléments de profil WLAN suivants ne \_ sont pas pris en charge dans Windows xp avec SP3 ou l’API LAN sans fil pour Windows XP avec SP2 :

-   connectivité (IHV)
-   IHV (WLANProfile)
-   OUI (OUIHeader)
-   phyType (connectivité)
-   PMKCacheMode (sécurité)
-   PMKCacheSize (sécurité)
-   PMKCacheTTL (sécurité)
-   preAuthMode (sécurité)
-   preAuthThrottle (sécurité)
-   sécurité (IHV)
-   type (OUIHeader)
-   useMSOneX (IHV)

le tableau suivant présente les \_ éléments de profil WLAN avec des valeurs conle pour Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :



| Élément                                                                               | Contrainte                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**nom (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)             | L’élément Name est ignoré lorsque le profil est enregistré dans le magasin de profils. Le nom du profil est dérivé automatiquement du SSID du réseau. Pour les profils réseau d’infrastructure, le nom du profil correspond à l’identificateur SSID du réseau. Pour les profils réseau ad hoc, le nom du profil correspond à l’identificateur SSID du réseau ad hoc suivi de `-adhoc` . |
| [**protégé (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)       | Doit avoir la valeur FALSe.                                                                                                                                                                                                                                                                                                                                      |
| [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md) | Limité à un seul élément [**SSID enfant (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) .                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a>Prise en charge OneX

seul l’élément [**EAPConfig**](onexschema-eapconfig-onex-element.md) est pris en charge sur Windows xp avec SP3 et l’API LAN sans fil pour Windows XP avec SP2. Les autres éléments OneX, s’ils sont présents dans un profil, seront ignorés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’API WiFi Native](about-the-native-wifi-api.md)
</dt> <dt>

[prise en charge de l’API Wifi Native sur Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



