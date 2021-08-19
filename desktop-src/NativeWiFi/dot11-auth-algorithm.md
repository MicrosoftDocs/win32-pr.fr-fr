---
description: Définit un algorithme d’authentification de réseau local sans fil.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: Énumération DOT11_AUTH_ALGORITHM (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 774b2218a451f4cbaa85e6b77559c0d5761b0b132ebdf9d3f11c15ea6658e7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798469"
---
# <a name="dot11_auth_algorithm-enumeration"></a>\_Énumération de l’algorithme d’authentification DOT11 \_

Le type énuméré de l' **\_ \_ algorithme d’authentification DOT11** définit un algorithme d’authentification de réseau local sans fil.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _DOT11_AUTH_ALGORITHM { 
  DOT11_AUTH_ALGO_80211_OPEN        = 1,
  DOT11_AUTH_ALGO_80211_SHARED_KEY  = 2,
  DOT11_AUTH_ALGO_WPA               = 3,
  DOT11_AUTH_ALGO_WPA_PSK           = 4,
  DOT11_AUTH_ALGO_WPA_NONE          = 5,
  DOT11_AUTH_ALGO_RSNA              = 6,
  DOT11_AUTH_ALGO_RSNA_PSK          = 7,
  DOT11_AUTH_ALGO_IHV_START         = 0x80000000,
  DOT11_AUTH_ALGO_IHV_END           = 0xffffffff
} DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**\_Algorithme d’authentification DOT11 \_ \_ 80211 \_ Open**
</dt> <dd>

Spécifie un algorithme d’authentification système IEEE 802,11 Open System.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**\_ \_ \_ \_ Clé partagée algorithme \_ de l’authentification DOT11 80211**
</dt> <dd>

Spécifie un algorithme d’authentification par clé partagée 802,11 qui requiert l’utilisation d’une clé WEP (Wired Equivalent Privacy) prépartagée pour l’authentification 802,11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**\_ \_ Algorithme WPA d’authentification DOT11 \_**
</dt> <dd>

Spécifie un algorithme d’accès protégé Wi-Fi (WPA). L’authentification du port IEEE 802.1 X est effectuée par le demandeur, l’authentificateur et le serveur d’authentification. Les clés de chiffrement sont dérivées dynamiquement par le processus d’authentification.

Cet algorithme est valide uniquement pour les types BSS de l' \_ infrastructure de type BSS dot11 \_ \_ .

Lorsque l’algorithme WPA est activé, la station 802,11 associe uniquement à un point d’accès dont les réponses de balise ou de sonde contiennent la suite d’authentification de type 1 (802.1 X) au sein de l’élément d’information WPA (IE).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**\_ \_ Algorithme \_ WPA PSK d' \_ authentification DOT11**
</dt> <dd>

Spécifie un algorithme WPA qui utilise des clés prépartagées (PSK). L’authentification du port IEEE 802.1 X est effectuée par le demandeur et l’authentificateur. Les clés de chiffrement sont dérivées dynamiquement par le biais d’une clé prépartagée qui est utilisée à la fois par le demandeur et l’authentificateur.

Cet algorithme est valide uniquement pour les types BSS de l' **\_ \_ \_ infrastructure de type BSS dot11**.

Lorsque l’algorithme WPA PSK est activé, la station 802,11 associe uniquement à un point d’accès dont les réponses de balise ou de sonde contiennent la suite d’authentification de type 2 (clé prépartagée) dans le WPA IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**\_Autorisation DOT11 \_ algorithme \_ WPA \_ None**
</dt> <dd>

Cette valeur n’est pas prise en charge.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**\_Algorithme d’authentification DOT11 \_ \_ RSNA**
</dt> <dd>

Spécifie un algorithme d’association de réseau de sécurité fiable (RSNA) 802.11 i. WPA2 est un algorithme de ce type. L’authentification du port IEEE 802.1 X est effectuée par le demandeur, l’authentificateur et le serveur d’authentification. Les clés de chiffrement sont dérivées dynamiquement par le processus d’authentification.

Cet algorithme est valide uniquement pour les types BSS de l' **\_ \_ \_ infrastructure de type BSS dot11**.

Lorsque l’algorithme RSNA est activé, la station 802,11 associe uniquement à un point d’accès dont les réponses de balise ou de sonde contiennent la suite d’authentification de type 1 (802.1 X) dans le RSN d’IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**\_Algorithme d’authentification DOT11 \_ \_ RSNA \_ PSK**
</dt> <dd>

Spécifie un algorithme 802.11 i RSNA qui utilise PSK. L’authentification du port IEEE 802.1 X est effectuée par le demandeur et l’authentificateur. Les clés de chiffrement sont dérivées dynamiquement par le biais d’une clé prépartagée qui est utilisée à la fois par le demandeur et l’authentificateur.

Cet algorithme est valide uniquement pour les types BSS de l' **\_ \_ \_ infrastructure de type BSS dot11**.

Lorsque l’algorithme PSK RSNA est activé, la station 802,11 associe uniquement à un point d’accès dont les réponses de balise ou de sonde contiennent la suite d’authentification de type 2 (clé prépartagée) dans le RSN d’IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**\_Démarrage du fabricant d’authentification DOT11 \_ algorithme \_ \_**
</dt> <dd>

Indique le début de la plage qui spécifie les algorithmes d’authentification propriétaires développés par un IHV.

L’énumérateur de **\_ démarrage de fabricant d’authentification \_ algorithme \_ \_ DOT11** est valide uniquement lorsque le pilote de miniport fonctionne en mode de station extensible (ExtSTA).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**Fin de l' \_ authentification DOT11 \_ algorithme \_ IHV \_**
</dt> <dd>

Indique la fin de la plage qui spécifie les algorithmes d’authentification propriétaires développés par un IHV.

L’énumérateur de **\_ fin du fabricant d’authentification \_ algorithme \_ \_ DOT11** est valide uniquement lorsque le pilote de miniport fonctionne en mode ExtSTA.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                        |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Wlantypes. h (inclure Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paire de \_ chiffrement d’authentification DOT11 \_**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**\_réseau WLAN disponible \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**\_attributs de sécurité WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




