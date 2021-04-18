---
description: Contient différents paramètres de sécurité.
ms.assetid: 1d912fb1-8fb4-4761-8991-5a50ffb0399e
title: Élément sécurité (MSM) (LAN_policy) (WLAN)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f6ea42a83d39c328db88e992555e5d593cc778b6
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106529033"
---
# <a name="security-msm-element-lan_policy-for-wlan"></a><span data-ttu-id="a8fa6-103">Élément Security (MSM) (LAN_policy) pour WLAN</span><span class="sxs-lookup"><span data-stu-id="a8fa6-103">Security (MSM) Element (LAN_policy) for WLAN</span></span>

<span data-ttu-id="a8fa6-104">L’élément Security (MSM) contient différents paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-104">The security (MSM) element contains various security settings.</span></span>

``` syntax
<xs:element name="security"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authEncryption">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="authentication">
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="open"
                                     />
                                    <xs:enumeration
                                        value="shared"
                                     />
                                    <xs:enumeration
                                        value="WPA"
                                     />
                                    <xs:enumeration
                                        value="WPAPSK"
                                     />
                                    <xs:enumeration
                                        value="WPA2"
                                     />
                                    <xs:enumeration
                                        value="WPA2PSK"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="encryption">
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="none"
                                     />
                                    <xs:enumeration
                                        value="WEP"
                                     />
                                    <xs:enumeration
                                        value="TKIP"
                                     />
                                    <xs:enumeration
                                        value="AES"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="useOneX"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="sharedKey"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="keyType">
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="networkKey"
                                     />
                                    <xs:enumeration
                                        value="passPhrase"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="protected"
                            type="boolean"
                         />
                        <xs:element name="keyMaterial"
                            type="string"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="keyIndex"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:minInclusive
                            value="0"
                         />
                        <xs:maxInclusive
                            value="3"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="PMKCacheMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="disabled"
                         />
                        <xs:enumeration
                            value="enabled"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="PMKCacheTTL"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:minInclusive
                            value="5"
                         />
                        <xs:maxInclusive
                            value="1400"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="PMKCacheSize"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:minInclusive
                            value="1"
                         />
                        <xs:maxInclusive
                            value="255"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="preAuthMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="disabled"
                         />
                        <xs:enumeration
                            value="enabled"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="preAuthThrottle"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:minInclusive
                            value="1"
                         />
                        <xs:maxInclusive
                            value="16"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="a8fa6-105">L’élément est défini par l’élément [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fa6-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a8fa6-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a8fa6-106">Child elements</span></span>



| <span data-ttu-id="a8fa6-107">Élément</span><span class="sxs-lookup"><span data-stu-id="a8fa6-107">Element</span></span>                                                                            | <span data-ttu-id="a8fa6-108">Type</span><span class="sxs-lookup"><span data-stu-id="a8fa6-108">Type</span></span>                                                              | <span data-ttu-id="a8fa6-109">Description</span><span class="sxs-lookup"><span data-stu-id="a8fa6-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8fa6-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="a8fa6-111">Spécifie l’authentification et la paire de chiffrement à utiliser pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="a8fa6-112">**identification**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="a8fa6-113">Spécifie l’authentification et la paire de chiffrement à utiliser pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="a8fa6-114">**chiffre**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-114">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="a8fa6-115">Définit le chiffrement des données à utiliser pour se connecter au réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-115">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="a8fa6-116">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-116">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="a8fa6-117">Spécifie l’index de clé qui doit être utilisé pour chiffrer le trafic sans fil.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-117">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="a8fa6-118">Cette valeur est utilisée uniquement lorsque KeyType est défini sur networkKey.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-118">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a8fa6-119">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-119">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="a8fa6-120">string</span><span class="sxs-lookup"><span data-stu-id="a8fa6-120">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="a8fa6-121">Contient la clé réseau ou la phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-121">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a8fa6-122">**keyType**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-122">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="a8fa6-123">Type de clé.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-123">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="a8fa6-124">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-124">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="a8fa6-125">Indique si la mise en cache PMK sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-125">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="a8fa6-126">Cet élément est valide uniquement pour les réseaux définis par WPA2.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-126">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="a8fa6-127">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-127">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="a8fa6-128">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-128">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="a8fa6-129">Spécifie le nombre d’entrées dans le cache OMK sur le client.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-129">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="a8fa6-130">Cet élément est valide uniquement pour les réseaux définis WPA2 avec le mode PMKCache défini sur activé.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-130">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="a8fa6-131">Si le mode PMKCache est activé et que cet élément est absent, la taille du cache est par défaut de 128 entrées.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-131">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="a8fa6-132">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-132">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="a8fa6-133">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-133">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="a8fa6-134">Indique la durée, en minutes, pendant laquelle un cache PMK est conservé.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-134">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="a8fa6-135">Cet élément est valide uniquement pour les réseaux définis WPA2 avec le mode PMKCache défini sur activé.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-135">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="a8fa6-136">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-136">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="a8fa6-137">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-137">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="a8fa6-138">Détermine si la pré-authentification est utilisée par le client.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-138">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="a8fa6-139">La pré-authentification permet l’itinérance sécurisée sécurisée par WPA2.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-139">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="a8fa6-140">Cet élément est valide uniquement pour les réseaux définis WPA2 avec le mode PMKCache défini sur activé.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-140">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="a8fa6-141">Si le mode PMKCache est activé et que cet élément est absent, la valeur par défaut est Disabled.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-141">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="a8fa6-142">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-142">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="a8fa6-143">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-143">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="a8fa6-144">Indique le nombre de tentatives lors de la préauthentification à des points d’accès voisins.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-144">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="a8fa6-145">Cet élément est valide uniquement pour les réseaux définis WPA2 avec le mode PMKCache défini sur activé.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-145">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="a8fa6-146">Si le mode PMKCache est activé et que cet élément est absent, le nombre de tentatives est défini par défaut sur 3.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-146">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="a8fa6-147">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-147">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="a8fa6-148">**Protect**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-148">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="a8fa6-149">boolean</span><span class="sxs-lookup"><span data-stu-id="a8fa6-149">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="a8fa6-150">Indique si la clé est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-150">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="a8fa6-151">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-151">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="a8fa6-152">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-152">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="a8fa6-153">Contient les informations sur la clé partagée.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-153">Contains the shared key information.</span></span> <span data-ttu-id="a8fa6-154">Cet élément est requis uniquement si des clés WEP ou PSK sont requises pour la paire authentification et chiffrement.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-154">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="a8fa6-155">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-155">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="a8fa6-156">boolean</span><span class="sxs-lookup"><span data-stu-id="a8fa6-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="a8fa6-157">Indique si 802.1 X est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-157">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="a8fa6-158">Cet indicateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a8fa6-158">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="a8fa6-159">Notes</span><span class="sxs-lookup"><span data-stu-id="a8fa6-159">Remarks</span></span>

<span data-ttu-id="a8fa6-160">L’élément [**FipsMode**](wlan-profileschema-fipsmode-authencryption-element.md) peut être inséré en tant qu’enfant de l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fa6-160">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="a8fa6-161">L’élément [**Onex**](onexschema-onex-element.md) peut être inséré en tant qu’enfant de l’élément de **sécurité (MSM)** .</span><span class="sxs-lookup"><span data-stu-id="a8fa6-161">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the **security (MSM)** element.</span></span>

## <a name="examples"></a><span data-ttu-id="a8fa6-162">Exemples</span><span class="sxs-lookup"><span data-stu-id="a8fa6-162">Examples</span></span>

<span data-ttu-id="a8fa6-163">Pour afficher des exemples de profils qui utilisent l’élément de **sécurité** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a8fa6-163">To view sample profiles that use the **security** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8fa6-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8fa6-164">Requirements</span></span>



| <span data-ttu-id="a8fa6-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8fa6-165">Requirement</span></span> | <span data-ttu-id="a8fa6-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8fa6-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a8fa6-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8fa6-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a8fa6-168">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8fa6-168">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a8fa6-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8fa6-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a8fa6-170">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8fa6-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a8fa6-171">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a8fa6-171">Redistributable</span></span><br/>          | <span data-ttu-id="a8fa6-172">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="a8fa6-172">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a8fa6-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8fa6-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8fa6-174">Exemples de profils sans fil</span><span class="sxs-lookup"><span data-stu-id="a8fa6-174">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="a8fa6-175">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-175">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a8fa6-176">**MSM**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-176">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="a8fa6-177">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-177">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a8fa6-178">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="a8fa6-178">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
