---
description: Définit un algorithme de chiffrement pour le chiffrement et le déchiffrement des données.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: Énumération DOT11_CIPHER_ALGORITHM (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fcbd61476458b5ed906ee57af6ab22b35f0378d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011611"
---
# <a name="dot11_cipher_algorithm-enumeration"></a>\_Énumération de l’algorithme de chiffrement DOT11 \_

Le type énuméré de l' **\_ \_ algorithme de chiffrement DOT11** définit un algorithme de chiffrement pour le chiffrement et le déchiffrement des données.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**\_Chiffrement DOT11 \_ algorithme \_ aucun**
</dt> <dd>

Spécifie qu’aucun algorithme de chiffrement n’est activé ou pris en charge.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**\_Algorithme de chiffrement DOT11 \_ \_ WEP40**
</dt> <dd>

Spécifie un algorithme WEP (Wired Equivalent Privacy), qui est l’algorithme RC4 spécifié dans la norme 802.11-1999. Cet énumérateur spécifie l’algorithme de chiffrement WEP avec une clé de chiffrement 40 bits.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**\_Chiffrement DOT11 \_ algorithme \_ TKIP**
</dt> <dd>

Spécifie un algorithme TKIP (Temporal Key Integrity Protocol), qui est la suite de chiffrement RC4 basée sur les algorithmes définis dans la spécification WPA et la norme IEEE 802.11 i-2004. Ce chiffrement utilise également l’algorithme MIC (message integrity code) Michael pour la protection de la falsification.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**\_Chiffrement DOT11 \_ algorithme \_ CCMP**
</dt> <dd>

Spécifie un algorithme AES-CCMP, tel que spécifié dans les normes IEEE 802.11 i-2004 et RFC 3610. Advanced Encryption Standard (AES) est l’algorithme de chiffrement défini dans la publication FIPS 197.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**\_Algorithme de chiffrement DOT11 \_ \_ WEP104**
</dt> <dd>

Spécifie un algorithme de chiffrement WEP avec une clé de chiffrement 104 bits.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**\_Groupe d' \_ \_ utilisation WPA \_ \_ de chiffrement DOT11 algorithme**
</dt> <dd>

Spécifie une suite de chiffrement de clé de groupe Wi-Fi WPA (Protected Access). Pour plus d’informations sur l’utilisation de la suite de chiffrement de clé de groupe, reportez-vous à la clause 7.3.2.25.1 de la norme IEEE 802.11 i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**\_Algorithme de chiffrement DOT11- \_ \_ \_ groupe d’utilisation RSN \_**
</dt> <dd>

Spécifie un réseau de sécurité fiable (RSN) utiliser la suite de chiffrement de clé de groupe. Pour plus d’informations sur l’utilisation de la suite de chiffrement de clé de groupe, reportez-vous à la clause 7.3.2.25.1 de la norme IEEE 802.11 i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**\_Chiffrement \_ algorithme WEP du CHIFFREment DOT11 \_**
</dt> <dd>

Spécifie un algorithme de chiffrement WEP avec une clé de chiffrement de n’importe quelle longueur.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**\_Démarrage du \_ fabricant de algorithme de CHIFFREment DOT11 \_ \_**
</dt> <dd>

Spécifie le début de la plage utilisée pour définir des algorithmes de chiffrement propriétaires développés par un fabricant de matériel indépendant.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**\_Fin de \_ algorithme \_ IHV du chiffrement DOT11 \_**
</dt> <dd>

Spécifie la fin de la plage utilisée pour définir des algorithmes de chiffrement propriétaires développés par un IHV.

</dd> </dl>

## <a name="requirements"></a>Spécifications



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

 

 




