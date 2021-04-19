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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534589"
---
# <a name="dot11_cipher_algorithm-enumeration"></a><span data-ttu-id="15cce-103">\_Énumération de l’algorithme de chiffrement DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="15cce-103">DOT11\_CIPHER\_ALGORITHM enumeration</span></span>

<span data-ttu-id="15cce-104">Le type énuméré de l' **\_ \_ algorithme de chiffrement DOT11** définit un algorithme de chiffrement pour le chiffrement et le déchiffrement des données.</span><span class="sxs-lookup"><span data-stu-id="15cce-104">The **DOT11\_CIPHER\_ALGORITHM** enumerated type defines a cipher algorithm for data encryption and decryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="15cce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15cce-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="15cce-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="15cce-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="15cce-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**\_Chiffrement DOT11 \_ algorithme \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="15cce-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11\_CIPHER\_ALGO\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="15cce-108">Spécifie qu’aucun algorithme de chiffrement n’est activé ou pris en charge.</span><span class="sxs-lookup"><span data-stu-id="15cce-108">Specifies that no cipher algorithm is enabled or supported.</span></span>

</dd> <dt>

<span data-ttu-id="15cce-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**\_Algorithme de chiffrement DOT11 \_ \_ WEP40**</span><span class="sxs-lookup"><span data-stu-id="15cce-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11\_CIPHER\_ALGO\_WEP40**</span></span>
</dt> <dd>

<span data-ttu-id="15cce-110">Spécifie un algorithme WEP (Wired Equivalent Privacy), qui est l’algorithme RC4 spécifié dans la norme 802.11-1999.</span><span class="sxs-lookup"><span data-stu-id="15cce-110">Specifies a Wired Equivalent Privacy (WEP) algorithm, which is the RC4-based algorithm that is specified in the 802.11-1999 standard.</span></span> <span data-ttu-id="15cce-111">Cet énumérateur spécifie l’algorithme de chiffrement WEP avec une clé de chiffrement 40 bits.</span><span class="sxs-lookup"><span data-stu-id="15cce-111">This enumerator specifies the WEP cipher algorithm with a 40-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="15cce-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**\_Chiffrement DOT11 \_ algorithme \_ TKIP**</span><span class="sxs-lookup"><span data-stu-id="15cce-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11\_CIPHER\_ALGO\_TKIP**</span></span>
</dt> <dd>

<span data-ttu-id="15cce-113">Spécifie un algorithme TKIP (Temporal Key Integrity Protocol), qui est la suite de chiffrement RC4 basée sur les algorithmes définis dans la spécification WPA et la norme IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="15cce-113">Specifies a Temporal Key Integrity Protocol (TKIP) algorithm, which is the RC4-based cipher suite that is based on the algorithms that are defined in the WPA specification and IEEE 802.11i-2004 standard.</span></span> <span data-ttu-id="15cce-114">Ce chiffrement utilise également l’algorithme MIC (message integrity code) Michael pour la protection de la falsification.</span><span class="sxs-lookup"><span data-stu-id="15cce-114">This cipher also uses the Michael Message Integrity Code (MIC) algorithm for forgery protection.</span></span>

</dd> <dt>

<span data-ttu-id="15cce-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**\_Chiffrement DOT11 \_ algorithme \_ CCMP**</span><span class="sxs-lookup"><span data-stu-id="15cce-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11\_CIPHER\_ALGO\_CCMP**</span></span>
</dt> <dd>

<span data-ttu-id="15cce-116">Spécifie un algorithme AES-CCMP, tel que spécifié dans les normes IEEE 802.11 i-2004 et RFC 3610.</span><span class="sxs-lookup"><span data-stu-id="15cce-116">Specifies an AES-CCMP algorithm, as specified in the IEEE 802.11i-2004 standard and RFC 3610.</span></span> <span data-ttu-id="15cce-117">Advanced Encryption Standard (AES) est l’algorithme de chiffrement défini dans la publication FIPS 197.</span><span class="sxs-lookup"><span data-stu-id="15cce-117">Advanced Encryption Standard (AES) is the encryption algorithm defined in FIPS PUB 197.</span></span>

</dd> <dt>

<span data-ttu-id="15cce-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**\_Algorithme de chiffrement DOT11 \_ \_ WEP104**</span><span class="sxs-lookup"><span data-stu-id="15cce-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11\_CIPHER\_ALGO\_WEP104**</span></span>
</dt> <dd>

<span data-ttu-id="15cce-119">Spécifie un algorithme de chiffrement WEP avec une clé de chiffrement 104 bits.</span><span class="sxs-lookup"><span data-stu-id="15cce-119">Specifies a WEP cipher algorithm with a 104-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="15cce-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**\_Groupe d' \_ \_ utilisation WPA \_ \_ de chiffrement DOT11 algorithme**</span><span class="sxs-lookup"><span data-stu-id="15cce-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11\_CIPHER\_ALGO\_WPA\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="15cce-121">Spécifie une suite de chiffrement de clé de groupe Wi-Fi WPA (Protected Access).</span><span class="sxs-lookup"><span data-stu-id="15cce-121">Specifies a Wi-Fi Protected Access (WPA) Use Group Key cipher suite.</span></span> <span data-ttu-id="15cce-122">Pour plus d’informations sur l’utilisation de la suite de chiffrement de clé de groupe, reportez-vous à la clause 7.3.2.25.1 de la norme IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="15cce-122">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="15cce-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**\_Algorithme de chiffrement DOT11- \_ \_ \_ groupe d’utilisation RSN \_**</span><span class="sxs-lookup"><span data-stu-id="15cce-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11\_CIPHER\_ALGO\_RSN\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="15cce-124">Spécifie un réseau de sécurité fiable (RSN) utiliser la suite de chiffrement de clé de groupe.</span><span class="sxs-lookup"><span data-stu-id="15cce-124">Specifies a Robust Security Network (RSN) Use Group Key cipher suite.</span></span> <span data-ttu-id="15cce-125">Pour plus d’informations sur l’utilisation de la suite de chiffrement de clé de groupe, reportez-vous à la clause 7.3.2.25.1 de la norme IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="15cce-125">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="15cce-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**\_Chiffrement \_ algorithme WEP du CHIFFREment DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="15cce-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11\_CIPHER\_ALGO\_WEP**</span></span>
</dt> <dd>

<span data-ttu-id="15cce-127">Spécifie un algorithme de chiffrement WEP avec une clé de chiffrement de n’importe quelle longueur.</span><span class="sxs-lookup"><span data-stu-id="15cce-127">Specifies a WEP cipher algorithm with a cipher key of any length.</span></span>

</dd> <dt>

<span data-ttu-id="15cce-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**\_Démarrage du \_ fabricant de algorithme de CHIFFREment DOT11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="15cce-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11\_CIPHER\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="15cce-129">Spécifie le début de la plage utilisée pour définir des algorithmes de chiffrement propriétaires développés par un fabricant de matériel indépendant.</span><span class="sxs-lookup"><span data-stu-id="15cce-129">Specifies the start of the range that is used to define proprietary cipher algorithms that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="15cce-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**\_Fin de \_ algorithme \_ IHV du chiffrement DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="15cce-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11\_CIPHER\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="15cce-131">Spécifie la fin de la plage utilisée pour définir des algorithmes de chiffrement propriétaires développés par un IHV.</span><span class="sxs-lookup"><span data-stu-id="15cce-131">Specifies the end of the range that is used to define proprietary cipher algorithms that are developed by an IHV.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15cce-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15cce-132">Requirements</span></span>



| <span data-ttu-id="15cce-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15cce-133">Requirement</span></span> | <span data-ttu-id="15cce-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="15cce-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15cce-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15cce-135">Minimum supported client</span></span><br/> | <span data-ttu-id="15cce-136">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15cce-136">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="15cce-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15cce-137">Minimum supported server</span></span><br/> | <span data-ttu-id="15cce-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15cce-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="15cce-139">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="15cce-139">Redistributable</span></span><br/>          | <span data-ttu-id="15cce-140">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="15cce-140">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="15cce-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="15cce-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="15cce-142"><dt>Wlantypes. h (inclure Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15cce-142"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15cce-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15cce-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15cce-144">**\_Paire de \_ chiffrement d’authentification DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="15cce-144">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="15cce-145">**\_réseau WLAN disponible \_**</span><span class="sxs-lookup"><span data-stu-id="15cce-145">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="15cce-146">**\_attributs de sécurité WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="15cce-146">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




