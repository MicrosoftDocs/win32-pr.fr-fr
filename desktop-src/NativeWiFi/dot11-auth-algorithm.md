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
ms.openlocfilehash: 1b14886c62448194b79eab2e0302ce5608ad282d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519990"
---
# <a name="dot11_auth_algorithm-enumeration"></a><span data-ttu-id="42274-103">\_Énumération de l’algorithme d’authentification DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="42274-103">DOT11\_AUTH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="42274-104">Le type énuméré de l' **\_ \_ algorithme d’authentification DOT11** définit un algorithme d’authentification de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="42274-104">The **DOT11\_AUTH\_ALGORITHM** enumerated type defines a wireless LAN authentication algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="42274-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42274-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="42274-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="42274-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="42274-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**\_Algorithme d’authentification DOT11 \_ \_ 80211 \_ Open**</span><span class="sxs-lookup"><span data-stu-id="42274-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11\_AUTH\_ALGO\_80211\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="42274-108">Spécifie un algorithme d’authentification système IEEE 802,11 Open System.</span><span class="sxs-lookup"><span data-stu-id="42274-108">Specifies an IEEE 802.11 Open System authentication algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="42274-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**\_ \_ \_ \_ Clé partagée algorithme \_ de l’authentification DOT11 80211**</span><span class="sxs-lookup"><span data-stu-id="42274-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11\_AUTH\_ALGO\_80211\_SHARED\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="42274-110">Spécifie un algorithme d’authentification par clé partagée 802,11 qui requiert l’utilisation d’une clé WEP (Wired Equivalent Privacy) prépartagée pour l’authentification 802,11.</span><span class="sxs-lookup"><span data-stu-id="42274-110">Specifies an 802.11 Shared Key authentication algorithm that requires the use of a pre-shared Wired Equivalent Privacy (WEP) key for the 802.11 authentication.</span></span>

</dd> <dt>

<span data-ttu-id="42274-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**\_ \_ Algorithme WPA d’authentification DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="42274-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11\_AUTH\_ALGO\_WPA**</span></span>
</dt> <dd>

<span data-ttu-id="42274-112">Spécifie un algorithme d’accès protégé Wi-Fi (WPA).</span><span class="sxs-lookup"><span data-stu-id="42274-112">Specifies a Wi-Fi Protected Access (WPA) algorithm.</span></span> <span data-ttu-id="42274-113">L’authentification du port IEEE 802.1 X est effectuée par le demandeur, l’authentificateur et le serveur d’authentification.</span><span class="sxs-lookup"><span data-stu-id="42274-113">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="42274-114">Les clés de chiffrement sont dérivées dynamiquement par le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="42274-114">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="42274-115">Cet algorithme est valide uniquement pour les types BSS de l' \_ infrastructure de type BSS dot11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="42274-115">This algorithm is valid only for BSS types of dot11\_BSS\_type\_infrastructure.</span></span>

<span data-ttu-id="42274-116">Lorsque l’algorithme WPA est activé, la station 802,11 associe uniquement à un point d’accès dont les réponses de balise ou de sonde contiennent la suite d’authentification de type 1 (802.1 X) au sein de l’élément d’information WPA (IE).</span><span class="sxs-lookup"><span data-stu-id="42274-116">When the WPA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the WPA information element (IE).</span></span>

</dd> <dt>

<span data-ttu-id="42274-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**\_ \_ Algorithme \_ WPA PSK d' \_ authentification DOT11**</span><span class="sxs-lookup"><span data-stu-id="42274-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11\_AUTH\_ALGO\_WPA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="42274-118">Spécifie un algorithme WPA qui utilise des clés prépartagées (PSK).</span><span class="sxs-lookup"><span data-stu-id="42274-118">Specifies a WPA algorithm that uses preshared keys (PSK).</span></span> <span data-ttu-id="42274-119">L’authentification du port IEEE 802.1 X est effectuée par le demandeur et l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="42274-119">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="42274-120">Les clés de chiffrement sont dérivées dynamiquement par le biais d’une clé prépartagée qui est utilisée à la fois par le demandeur et l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="42274-120">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="42274-121">Cet algorithme est valide uniquement pour les types BSS de l' **\_ \_ \_ infrastructure de type BSS dot11**.</span><span class="sxs-lookup"><span data-stu-id="42274-121">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="42274-122">Lorsque l’algorithme WPA PSK est activé, la station 802,11 associe uniquement à un point d’accès dont les réponses de balise ou de sonde contiennent la suite d’authentification de type 2 (clé prépartagée) dans le WPA IE.</span><span class="sxs-lookup"><span data-stu-id="42274-122">When the WPA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2 (preshared key) within the WPA IE.</span></span>

</dd> <dt>

<span data-ttu-id="42274-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**\_Autorisation DOT11 \_ algorithme \_ WPA \_ None**</span><span class="sxs-lookup"><span data-stu-id="42274-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11\_AUTH\_ALGO\_WPA\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="42274-124">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="42274-124">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="42274-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**\_Algorithme d’authentification DOT11 \_ \_ RSNA**</span><span class="sxs-lookup"><span data-stu-id="42274-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11\_AUTH\_ALGO\_RSNA**</span></span>
</dt> <dd>

<span data-ttu-id="42274-126">Spécifie un algorithme d’association de réseau de sécurité fiable (RSNA) 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="42274-126">Specifies an 802.11i Robust Security Network Association (RSNA) algorithm.</span></span> <span data-ttu-id="42274-127">WPA2 est un algorithme de ce type.</span><span class="sxs-lookup"><span data-stu-id="42274-127">WPA2 is one such algorithm.</span></span> <span data-ttu-id="42274-128">L’authentification du port IEEE 802.1 X est effectuée par le demandeur, l’authentificateur et le serveur d’authentification.</span><span class="sxs-lookup"><span data-stu-id="42274-128">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="42274-129">Les clés de chiffrement sont dérivées dynamiquement par le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="42274-129">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="42274-130">Cet algorithme est valide uniquement pour les types BSS de l' **\_ \_ \_ infrastructure de type BSS dot11**.</span><span class="sxs-lookup"><span data-stu-id="42274-130">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="42274-131">Lorsque l’algorithme RSNA est activé, la station 802,11 associe uniquement à un point d’accès dont les réponses de balise ou de sonde contiennent la suite d’authentification de type 1 (802.1 X) dans le RSN d’IE.</span><span class="sxs-lookup"><span data-stu-id="42274-131">When the RSNA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="42274-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**\_Algorithme d’authentification DOT11 \_ \_ RSNA \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="42274-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11\_AUTH\_ALGO\_RSNA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="42274-133">Spécifie un algorithme 802.11 i RSNA qui utilise PSK.</span><span class="sxs-lookup"><span data-stu-id="42274-133">Specifies an 802.11i RSNA algorithm that uses PSK.</span></span> <span data-ttu-id="42274-134">L’authentification du port IEEE 802.1 X est effectuée par le demandeur et l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="42274-134">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="42274-135">Les clés de chiffrement sont dérivées dynamiquement par le biais d’une clé prépartagée qui est utilisée à la fois par le demandeur et l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="42274-135">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="42274-136">Cet algorithme est valide uniquement pour les types BSS de l' **\_ \_ \_ infrastructure de type BSS dot11**.</span><span class="sxs-lookup"><span data-stu-id="42274-136">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="42274-137">Lorsque l’algorithme PSK RSNA est activé, la station 802,11 associe uniquement à un point d’accès dont les réponses de balise ou de sonde contiennent la suite d’authentification de type 2 (clé prépartagée) dans le RSN d’IE.</span><span class="sxs-lookup"><span data-stu-id="42274-137">When the RSNA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2(preshared key) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="42274-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**\_Démarrage du fabricant d’authentification DOT11 \_ algorithme \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42274-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11\_AUTH\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="42274-139">Indique le début de la plage qui spécifie les algorithmes d’authentification propriétaires développés par un IHV.</span><span class="sxs-lookup"><span data-stu-id="42274-139">Indicates the start of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="42274-140">L’énumérateur de **\_ démarrage de fabricant d’authentification \_ algorithme \_ \_ DOT11** est valide uniquement lorsque le pilote de miniport fonctionne en mode de station extensible (ExtSTA).</span><span class="sxs-lookup"><span data-stu-id="42274-140">The **DOT11\_AUTH\_ALGO\_IHV\_START** enumerator is valid only when the miniport driver is operating in Extensible Station (ExtSTA) mode.</span></span>

</dd> <dt>

<span data-ttu-id="42274-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**Fin de l' \_ authentification DOT11 \_ algorithme \_ IHV \_**</span><span class="sxs-lookup"><span data-stu-id="42274-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11\_AUTH\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="42274-142">Indique la fin de la plage qui spécifie les algorithmes d’authentification propriétaires développés par un IHV.</span><span class="sxs-lookup"><span data-stu-id="42274-142">Indicates the end of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="42274-143">L’énumérateur de **\_ fin du fabricant d’authentification \_ algorithme \_ \_ DOT11** est valide uniquement lorsque le pilote de miniport fonctionne en mode ExtSTA.</span><span class="sxs-lookup"><span data-stu-id="42274-143">The **DOT11\_AUTH\_ALGO\_IHV\_END** enumerator is valid only when the miniport driver is operating in ExtSTA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42274-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42274-144">Requirements</span></span>



| <span data-ttu-id="42274-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42274-145">Requirement</span></span> | <span data-ttu-id="42274-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="42274-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42274-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42274-147">Minimum supported client</span></span><br/> | <span data-ttu-id="42274-148">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42274-148">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="42274-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42274-149">Minimum supported server</span></span><br/> | <span data-ttu-id="42274-150">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42274-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="42274-151">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="42274-151">Redistributable</span></span><br/>          | <span data-ttu-id="42274-152">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="42274-152">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="42274-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="42274-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="42274-154"><dt>Wlantypes. h (inclure Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42274-154"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42274-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42274-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42274-156">**\_Paire de \_ chiffrement d’authentification DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="42274-156">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="42274-157">**\_réseau WLAN disponible \_**</span><span class="sxs-lookup"><span data-stu-id="42274-157">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="42274-158">**\_attributs de sécurité WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="42274-158">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




