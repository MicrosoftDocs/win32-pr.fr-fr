---
description: Contient différents paramètres de module spécifique au support (MSM).
ms.assetid: 31f98af8-a577-4f6a-9a0a-b182b5a89cc3
title: Élément MSM (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: b2e1ffdc5ad27524d3d2fc5b37b3a060a90c7575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520676"
---
# <a name="msm-wlanprofile-element"></a><span data-ttu-id="8fe4f-103">Élément MSM (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="8fe4f-103">MSM (WLANProfile) Element</span></span>

<span data-ttu-id="8fe4f-104">L’élément MSM (WLANProfile) contient différents paramètres de module spécifique au support (MSM).</span><span class="sxs-lookup"><span data-stu-id="8fe4f-104">The MSM (WLANProfile) element contains various media-specific module (MSM) settings.</span></span>

``` syntax
<xs:element name="MSM"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="phyType"
                            minOccurs="0"
                            maxOccurs="4"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="a"
                                     />
                                    <xs:enumeration
                                        value="b"
                                     />
                                    <xs:enumeration
                                        value="g"
                                     />
                                    <xs:enumeration
                                        value="n"
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

<span data-ttu-id="8fe4f-105">L’élément est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8fe4f-105">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8fe4f-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8fe4f-106">Child elements</span></span>



| <span data-ttu-id="8fe4f-107">Élément</span><span class="sxs-lookup"><span data-stu-id="8fe4f-107">Element</span></span>                                                                            | <span data-ttu-id="8fe4f-108">Type</span><span class="sxs-lookup"><span data-stu-id="8fe4f-108">Type</span></span>                                                              | <span data-ttu-id="8fe4f-109">Description</span><span class="sxs-lookup"><span data-stu-id="8fe4f-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fe4f-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="8fe4f-111">Spécifie l’authentification et la paire de chiffrement à utiliser pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="8fe4f-112">**identification**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="8fe4f-113">Spécifie l’authentification et la paire de chiffrement à utiliser pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="8fe4f-114">**connectivité**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-114">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="8fe4f-115">Contient différents paramètres de connectivité.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-115">Contains various connectivity settings.</span></span> <span data-ttu-id="8fe4f-116">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-116">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="8fe4f-117">**chiffre**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-117">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="8fe4f-118">Définit le chiffrement des données à utiliser pour se connecter au réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-118">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="8fe4f-119">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-119">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="8fe4f-120">Spécifie l’index de clé qui doit être utilisé pour chiffrer le trafic sans fil.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-120">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="8fe4f-121">Cette valeur est utilisée uniquement lorsque KeyType est défini sur networkKey.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-121">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="8fe4f-122">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-122">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="8fe4f-123">string</span><span class="sxs-lookup"><span data-stu-id="8fe4f-123">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="8fe4f-124">Contient la clé réseau ou la phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-124">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="8fe4f-125">**keyType**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-125">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="8fe4f-126">Type de clé.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-126">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="8fe4f-127">**phyType**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-127">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="8fe4f-128">Spécifie la norme de réseau local sans fil 802,11 utilisée sur le réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-128">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="8fe4f-129">La valeur « n » est uniquement prise en charge sur Windows Vista avec SP1 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-129">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="8fe4f-130">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="8fe4f-131">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-131">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="8fe4f-132">Indique si la mise en cache PMK sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-132">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="8fe4f-133">Cet élément est valide uniquement pour les réseaux définis par WPA2.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-133">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="8fe4f-134">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-134">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="8fe4f-135">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-135">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="8fe4f-136">Spécifie le nombre d’entrées dans le cache OMK sur le client.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-136">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="8fe4f-137">Cet élément est valide uniquement pour les réseaux définis WPA2 avec le mode PMKCache défini sur activé.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-137">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="8fe4f-138">Si le mode PMKCache est activé et que cet élément est absent, la taille du cache est par défaut de 128 entrées.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-138">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="8fe4f-139">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-139">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="8fe4f-140">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-140">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="8fe4f-141">Indique la durée, en minutes, pendant laquelle un cache PMK est conservé.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-141">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="8fe4f-142">Cet élément est valide uniquement pour les réseaux définis WPA2 avec le mode PMKCache défini sur activé.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-142">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="8fe4f-143">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-143">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="8fe4f-144">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-144">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="8fe4f-145">Détermine si la pré-authentification est utilisée par le client.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-145">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="8fe4f-146">La pré-authentification permet l’itinérance sécurisée sécurisée par WPA2.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-146">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="8fe4f-147">Cet élément est valide uniquement pour les réseaux définis WPA2 avec le mode PMKCache défini sur activé.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-147">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="8fe4f-148">Si le mode PMKCache est activé et que cet élément est absent, la valeur par défaut est Disabled.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-148">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="8fe4f-149">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-149">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="8fe4f-150">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-150">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="8fe4f-151">Indique le nombre de tentatives lors de la préauthentification à des points d’accès voisins.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-151">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="8fe4f-152">Cet élément est valide uniquement pour les réseaux définis WPA2 avec le mode PMKCache défini sur activé.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-152">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="8fe4f-153">Si le mode PMKCache est activé et que cet élément est absent, le nombre de tentatives est défini par défaut sur 3.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-153">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="8fe4f-154">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-154">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="8fe4f-155">**Protect**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-155">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="8fe4f-156">boolean</span><span class="sxs-lookup"><span data-stu-id="8fe4f-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="8fe4f-157">Indique si la clé est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-157">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="8fe4f-158">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément doit avoir la valeur FALSe.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-158">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="8fe4f-159">**caution**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-159">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="8fe4f-160">Contient différents paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-160">Contains various security settings.</span></span> <span data-ttu-id="8fe4f-161">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-161">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="8fe4f-162">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-162">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="8fe4f-163">Contient les informations sur la clé partagée.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-163">Contains the shared key information.</span></span> <span data-ttu-id="8fe4f-164">Cet élément est requis uniquement si des clés WEP ou PSK sont requises pour la paire authentification et chiffrement.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-164">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="8fe4f-165">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-165">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="8fe4f-166">boolean</span><span class="sxs-lookup"><span data-stu-id="8fe4f-166">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="8fe4f-167">Indique si 802.1 X est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-167">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="8fe4f-168">Cet indicateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="8fe4f-168">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="8fe4f-169">Notes</span><span class="sxs-lookup"><span data-stu-id="8fe4f-169">Remarks</span></span>

<span data-ttu-id="8fe4f-170">L’élément [**FipsMode**](wlan-profileschema-fipsmode-authencryption-element.md) peut être inséré en tant qu’enfant de l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8fe4f-170">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="8fe4f-171">L’élément [**Onex**](onexschema-onex-element.md) peut être inséré en tant qu’enfant de l’élément de [**sécurité (MSM)**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8fe4f-171">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="8fe4f-172">Exemples</span><span class="sxs-lookup"><span data-stu-id="8fe4f-172">Examples</span></span>

<span data-ttu-id="8fe4f-173">Pour afficher des exemples de profils qui utilisent l’élément **MSM** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8fe4f-173">To view sample profiles that use the **MSM** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe4f-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fe4f-174">Requirements</span></span>



| <span data-ttu-id="8fe4f-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fe4f-175">Requirement</span></span> | <span data-ttu-id="8fe4f-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fe4f-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8fe4f-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe4f-177">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe4f-178">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fe4f-178">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8fe4f-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe4f-179">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe4f-180">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fe4f-180">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="8fe4f-181">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8fe4f-181">Redistributable</span></span><br/>          | <span data-ttu-id="8fe4f-182">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="8fe4f-182">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8fe4f-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fe4f-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe4f-184">Exemples de profils sans fil</span><span class="sxs-lookup"><span data-stu-id="8fe4f-184">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="8fe4f-185">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-185">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8fe4f-186">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-186">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="8fe4f-187">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-187">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8fe4f-188">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="8fe4f-188">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
