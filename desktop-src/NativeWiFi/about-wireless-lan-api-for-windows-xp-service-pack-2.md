---
description: un sous-ensemble de la fonctionnalité de l’API Wifi Native est pris en charge sur Windows xp avec service pack 2 (SP2) et Windows xp avec service pack 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: prise en charge de l’API Wifi Native sur Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021138"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>prise en charge de l’API Wifi Native sur Windows XP

un sous-ensemble de la fonctionnalité de l’API Wifi Native est pris en charge sur Windows xp avec service pack 2 (SP2) et Windows xp avec service pack 3 (SP3). cette fonctionnalité est incluse dans Windows XP avec SP3 par défaut. dans Windows XP avec SP2, cette fonctionnalité peut être ajoutée en appliquant un correctif, connu sous le nom d’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2). pour plus d’informations ou pour télécharger le correctif logiciel, consultez la rubrique « les développeurs ne peuvent pas créer de programmes clients sans fil qui gèrent des profils sans fil et des connexions sur le service de Configuration sans fil sans fil dans Microsoft Windows XP service Pack 2 (SP2) » dans la Base de connaissances d’aide et de Support à l’adresse [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .

en raison des différences architecturales sous-jacentes dans Windows XP, l’API Wifi Native sur présente certaines limites. Voici une liste de limitations :

-   Au plus un SSID peut être associé à un profil.
-   Les réseaux d’infrastructure apparaissent toujours avant les réseaux ad hoc dans la liste des profils.
-   Les noms de profil sont dérivés du SSID et ne peuvent pas être définis par l’utilisateur sur une chaîne arbitraire.
-   Les types PHY ne sont pas pris en charge.
-   La mise en cache de la clé PMK (Pairwise Master Key) n’est pas prise en charge.
-   Les fonctions d’extensibilité du fournisseur de matériel indépendant (IHV) ne sont pas prises en charge.
-   Les autorisations de profil ne sont pas prises en charge.
-   Seule la \_ connexion ACM de notification WLAN \_ \_ \_ est terminée et \_ les \_ notifications d’accès hors connexion ACM de notification WLAN \_ sont disponibles.
-   Les paramètres globaux de configuration 802.1 X et EAPOL ne sont pas pris en charge.

les fonctions suivantes sont prises en charge par Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :

-   [**\_rappel de notification WLAN \_**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [**WlanAllocateMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [**WlanFreeMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [**WlanGetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [**WlanOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [**WlanSetProfileEapXmlUserData**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [**WlanSetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [**WlanSetProfilePosition**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[À propos de la WiFi Native](about-native-wifi.md)
</dt> </dl>

 

 
