---
description: Contient un profil de réseau local sans fil.
ms.assetid: bc97cb49-3891-4a4a-aab4-895cd9ce6908
title: Élément WLANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 227d912128bf3f656fca7aecbaf0fe0640659465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868634"
---
# <a name="wlanprofile-element"></a><span data-ttu-id="66878-103">Élément WLANProfile</span><span class="sxs-lookup"><span data-stu-id="66878-103">WLANProfile Element</span></span>

<span data-ttu-id="66878-104">L’élément **WLANProfile** contient un profil de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="66878-104">The **WLANProfile** element contains a wireless LAN profile.</span></span> <span data-ttu-id="66878-105">Cet élément est l’élément racine unique pour un profil sans fil.</span><span class="sxs-lookup"><span data-stu-id="66878-105">This element is the unique root element for a wireless profile.</span></span>

<span data-ttu-id="66878-106">L’espace de noms cible de l’élément WLANProfile est `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="66878-106">The target namespace for the WLANProfile element is `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

``` syntax
<xs:element name="WLANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="SSIDConfig"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="SSID"
                            maxOccurs="256"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="hex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="name"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
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
                        <xs:element name="nonBroadcast"
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
            <xs:element name="connectionType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="IBSS"
                         />
                        <xs:enumeration
                            value="ESS"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="connectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="manual"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="autoSwitch"
                type="boolean"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
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
            <xs:element name="IHV"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUIHeader">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OUI">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="type">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="1"
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
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
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
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="useMSOneX"
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

## <a name="child-elements"></a><span data-ttu-id="66878-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="66878-107">Child elements</span></span>



| <span data-ttu-id="66878-108">Élément</span><span class="sxs-lookup"><span data-stu-id="66878-108">Element</span></span>                                                                            | <span data-ttu-id="66878-109">Type</span><span class="sxs-lookup"><span data-stu-id="66878-109">Type</span></span>                                                              | <span data-ttu-id="66878-110">Description</span><span class="sxs-lookup"><span data-stu-id="66878-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66878-111">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="66878-111">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="66878-112">Spécifie l’authentification et la paire de chiffrement à utiliser pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="66878-112">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="66878-113">**identification**</span><span class="sxs-lookup"><span data-stu-id="66878-113">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="66878-114">Spécifie la méthode d’authentification à utiliser pour se connecter au réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="66878-114">Specifies the authentication method to be used to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="66878-115">**Commutation autocommutateur**</span><span class="sxs-lookup"><span data-stu-id="66878-115">**autoSwitch**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [<span data-ttu-id="66878-116">boolean</span><span class="sxs-lookup"><span data-stu-id="66878-116">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="66878-117">Détermine le comportement d’itinérance d’un réseau connecté automatiquement lorsqu’un réseau plus préféré est à portée.</span><span class="sxs-lookup"><span data-stu-id="66878-117">Determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="66878-118">Cet élément est facultatif et n’a aucun effet sur un réseau connecté manuellement.</span><span class="sxs-lookup"><span data-stu-id="66878-118">This element is optional and has no effect on a manually connected network.</span></span><br/> <span data-ttu-id="66878-119">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="66878-120">**connectionMode**</span><span class="sxs-lookup"><span data-stu-id="66878-120">**connectionMode**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="66878-121">Indique si la connexion au réseau local sans fil doit être automatique (« automatique ») ou initiée (« manuelle ») par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66878-121">Indicates whether connection to the wireless LAN should be automatic ("auto") or initiated ("manual") by user.</span></span> <span data-ttu-id="66878-122">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="66878-122">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="66878-123">**connectionType**</span><span class="sxs-lookup"><span data-stu-id="66878-123">**connectionType**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="66878-124">Indique si le réseau est une infrastructure (« ESS ») ou ad-hoc (« IBSS »).</span><span class="sxs-lookup"><span data-stu-id="66878-124">Indicates whether the network is infrastructure ("ESS") or ad-hoc ("IBSS").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="66878-125">**connectivité**</span><span class="sxs-lookup"><span data-stu-id="66878-125">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="66878-126">Contient différents paramètres de connectivité.</span><span class="sxs-lookup"><span data-stu-id="66878-126">Contains various connectivity settings.</span></span> <span data-ttu-id="66878-127">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="66878-127">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="66878-128">**connectivité**</span><span class="sxs-lookup"><span data-stu-id="66878-128">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | <span data-ttu-id="66878-129">Contient des paramètres de connectivité liés aux IHV.</span><span class="sxs-lookup"><span data-stu-id="66878-129">Contains IHV-related connectivity settings.</span></span><br/> <span data-ttu-id="66878-130">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="66878-131">**chiffre**</span><span class="sxs-lookup"><span data-stu-id="66878-131">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="66878-132">Définit le chiffrement des données à utiliser pour se connecter au réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="66878-132">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="66878-133">**hex**</span><span class="sxs-lookup"><span data-stu-id="66878-133">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | <span data-ttu-id="66878-134">Contient le SSID d’un réseau local sans fil au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="66878-134">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="66878-135">**FABRICANTS**</span><span class="sxs-lookup"><span data-stu-id="66878-135">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="66878-136">Contient les paramètres facultatifs du fournisseur de matériel indépendant (IHV).</span><span class="sxs-lookup"><span data-stu-id="66878-136">Contains optional independent hardware vendor (IHV) settings.</span></span><br/> <span data-ttu-id="66878-137">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-137">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="66878-138">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="66878-138">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="66878-139">Spécifie l’index de clé à utiliser pour chiffrer le trafic sans fil.</span><span class="sxs-lookup"><span data-stu-id="66878-139">Specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="66878-140">Cette valeur est utilisée uniquement lorsque [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) est défini sur « networkKey ».</span><span class="sxs-lookup"><span data-stu-id="66878-140">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="66878-141">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="66878-141">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="66878-142">string</span><span class="sxs-lookup"><span data-stu-id="66878-142">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="66878-143">Contient la clé réseau ou la phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="66878-143">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="66878-144">**keyType**</span><span class="sxs-lookup"><span data-stu-id="66878-144">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="66878-145">Type de clé.</span><span class="sxs-lookup"><span data-stu-id="66878-145">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="66878-146">**MSM**</span><span class="sxs-lookup"><span data-stu-id="66878-146">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="66878-147">Contient différents paramètres MSM.</span><span class="sxs-lookup"><span data-stu-id="66878-147">Contains various MSM settings.</span></span> <span data-ttu-id="66878-148">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="66878-148">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="66878-149">**nomme**</span><span class="sxs-lookup"><span data-stu-id="66878-149">**name**</span></span>](wlan-profileschema-name-wlanprofile-element.md)                        | [<span data-ttu-id="66878-150">**nameType**</span><span class="sxs-lookup"><span data-stu-id="66878-150">**nameType**</span></span>](wlan-profileschema-nametype-simpletype.md)        | <span data-ttu-id="66878-151">Nom du profil de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="66878-151">Name of the WLAN profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="66878-152">**nomme**</span><span class="sxs-lookup"><span data-stu-id="66878-152">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                               |                                                                   | <span data-ttu-id="66878-153">Contient le SSID d’un réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="66878-153">Contains the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="66878-154">**ne pas diffuser**</span><span class="sxs-lookup"><span data-stu-id="66878-154">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [<span data-ttu-id="66878-155">boolean</span><span class="sxs-lookup"><span data-stu-id="66878-155">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="66878-156">Indique si le réseau diffuse son SSID.</span><span class="sxs-lookup"><span data-stu-id="66878-156">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="66878-157">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-157">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="66878-158">**OUI**</span><span class="sxs-lookup"><span data-stu-id="66878-158">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | <span data-ttu-id="66878-159">Contient une hexBinary de 3 octets qui identifie le IHV.</span><span class="sxs-lookup"><span data-stu-id="66878-159">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/> <span data-ttu-id="66878-160">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-160">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="66878-161">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="66878-161">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | <span data-ttu-id="66878-162">Identifie le IHV.</span><span class="sxs-lookup"><span data-stu-id="66878-162">Identifies the IHV.</span></span><br/> <span data-ttu-id="66878-163">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-163">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="66878-164">**phyType**</span><span class="sxs-lookup"><span data-stu-id="66878-164">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="66878-165">Spécifie la norme de réseau local sans fil 802,11 utilisée sur le réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="66878-165">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="66878-166">La valeur « n » est uniquement prise en charge sur Windows Vista avec SP1 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="66878-166">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="66878-167">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-167">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="66878-168">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="66878-168">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="66878-169">Indique si la mise en cache PMK sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="66878-169">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="66878-170">Cet élément est valide uniquement pour les réseaux définis par WPA2.</span><span class="sxs-lookup"><span data-stu-id="66878-170">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="66878-171">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-171">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="66878-172">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="66878-172">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="66878-173">Spécifie le nombre d’entrées dans le cache PMK sur le client.</span><span class="sxs-lookup"><span data-stu-id="66878-173">Specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="66878-174">Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ».</span><span class="sxs-lookup"><span data-stu-id="66878-174">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="66878-175">Si **PMKCacheMode** est activé et que cet élément est absent, la taille du cache est par défaut de 128 entrées.</span><span class="sxs-lookup"><span data-stu-id="66878-175">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="66878-176">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-176">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="66878-177">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="66878-177">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="66878-178">Indique la durée, en minutes, pendant laquelle un cache PMK est conservé.</span><span class="sxs-lookup"><span data-stu-id="66878-178">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="66878-179">Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ».</span><span class="sxs-lookup"><span data-stu-id="66878-179">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span><br/> <span data-ttu-id="66878-180">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-180">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="66878-181">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="66878-181">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="66878-182">Détermine si la pré-authentification est utilisée par le client.</span><span class="sxs-lookup"><span data-stu-id="66878-182">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="66878-183">La pré-authentification permet l’itinérance sécurisée sécurisée par WPA2.</span><span class="sxs-lookup"><span data-stu-id="66878-183">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="66878-184">Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ».</span><span class="sxs-lookup"><span data-stu-id="66878-184">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="66878-185">Si **PMKCacheMode** est activé et que cet élément est absent, la valeur par défaut est Disabled.</span><span class="sxs-lookup"><span data-stu-id="66878-185">If **PMKCacheMode** is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="66878-186">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-186">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="66878-187">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="66878-187">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="66878-188">Indique le nombre de tentatives lors de la préauthentification à des points d’accès voisins.</span><span class="sxs-lookup"><span data-stu-id="66878-188">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="66878-189">Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ».</span><span class="sxs-lookup"><span data-stu-id="66878-189">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="66878-190">Si **PMKCacheMode** est activé et que cet élément est absent, le nombre de tentatives est défini par défaut sur 3.</span><span class="sxs-lookup"><span data-stu-id="66878-190">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="66878-191">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-191">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="66878-192">**Protect**</span><span class="sxs-lookup"><span data-stu-id="66878-192">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="66878-193">boolean</span><span class="sxs-lookup"><span data-stu-id="66878-193">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="66878-194">Indique si la clé est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="66878-194">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="66878-195">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="66878-195">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="66878-196">**caution**</span><span class="sxs-lookup"><span data-stu-id="66878-196">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="66878-197">Contient différents paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="66878-197">Contains various security settings.</span></span> <span data-ttu-id="66878-198">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="66878-198">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="66878-199">**caution**</span><span class="sxs-lookup"><span data-stu-id="66878-199">**security**</span></span>](wlan-profileschema-security-ihv-element.md)                        |                                                                   | <span data-ttu-id="66878-200">Contient des paramètres de sécurité spécifiques au IHV.</span><span class="sxs-lookup"><span data-stu-id="66878-200">Contains IHV-specific security settings.</span></span> <span data-ttu-id="66878-201">Les paramètres de sécurité Microsoft et les paramètres de sécurité IHV s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="66878-201">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="66878-202">Si les deux jeux de paramètres de sécurité sont présents dans le même profil, le profil n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="66878-202">If both sets of security settings are present in the same profile, the profile is invalid.</span></span><br/> <span data-ttu-id="66878-203">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-203">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="66878-204">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="66878-204">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="66878-205">Contient les informations sur la clé partagée.</span><span class="sxs-lookup"><span data-stu-id="66878-205">Contains the shared key information.</span></span> <span data-ttu-id="66878-206">Cet élément est requis uniquement si des clés WEP ou PSK sont requises pour la paire authentification et chiffrement.</span><span class="sxs-lookup"><span data-stu-id="66878-206">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="66878-207">**SSID**</span><span class="sxs-lookup"><span data-stu-id="66878-207">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | <span data-ttu-id="66878-208">Spécifie le SSID d’un réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="66878-208">Specifies the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="66878-209">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="66878-209">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | <span data-ttu-id="66878-210">Contient un ou plusieurs SSID avec d’autres paramètres communs.</span><span class="sxs-lookup"><span data-stu-id="66878-210">Contains one or more SSIDs along with other common settings.</span></span> <br/> <span data-ttu-id="66878-211">Un profil peut avoir plusieurs éléments [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) et chaque élément [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) peut avoir plusieurs éléments [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="66878-211">A profile can have multiple [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) elements and each [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element can have multiple [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) elements.</span></span> <span data-ttu-id="66878-212">Toutefois, Windows ne prend jamais en compte le premier élément [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) dans un élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="66878-212">However, Windows only ever considers the first [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element in a [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span><br/> <span data-ttu-id="66878-213">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Au plus un élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) peut apparaître dans un profil.</span><span class="sxs-lookup"><span data-stu-id="66878-213">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/> |
| [<span data-ttu-id="66878-214">**entrer**</span><span class="sxs-lookup"><span data-stu-id="66878-214">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | <span data-ttu-id="66878-215">Contient une valeur **hexBinary** de 1 octet qui est utilisée pour différencier les cartes réseau par le même IHV.</span><span class="sxs-lookup"><span data-stu-id="66878-215">Contains a 1 byte **hexBinary** that is used to differentiate NICs by the same IHV.</span></span><br/> <span data-ttu-id="66878-216">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="66878-216">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="66878-217">**useMSOneX**</span><span class="sxs-lookup"><span data-stu-id="66878-217">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)                      | [<span data-ttu-id="66878-218">boolean</span><span class="sxs-lookup"><span data-stu-id="66878-218">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="66878-219">Spécifie l’origine des paramètres de sécurité 802.1 X utilisés par un composant de sécurité IHV.</span><span class="sxs-lookup"><span data-stu-id="66878-219">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="66878-220">Quand [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) a la valeur true, les composants de sécurité IHV utilisent les paramètres 802.1 x définis par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="66878-220">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="66878-221">Quand **useMSOneX** a la valeur false, les composants de sécurité IHV utilisent les paramètres 802.1 x fournis par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="66878-221">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="66878-222">Par défaut, **useMSOneX** a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="66878-222">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="66878-223">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="66878-223">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="66878-224">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="66878-224">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="66878-225">boolean</span><span class="sxs-lookup"><span data-stu-id="66878-225">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="66878-226">Indique si 802.1 X est utilisé.</span><span class="sxs-lookup"><span data-stu-id="66878-226">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="66878-227">Cet indicateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="66878-227">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="66878-228">Notes</span><span class="sxs-lookup"><span data-stu-id="66878-228">Remarks</span></span>

<span data-ttu-id="66878-229">La plupart des éléments enfants de l’élément WLANProfile se trouvent dans l' `https://www.microsoft.com/networking/WLAN/profile/v1` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="66878-229">Most child elements of the WLANProfile element are in the `https://www.microsoft.com/networking/WLAN/profile/v1` namespace.</span></span> <span data-ttu-id="66878-230">Il existe deux exceptions : l’élément [**FipsMode**](wlan-profileschema-fipsmode-authencryption-element.md) est dans l' `https://www.microsoft.com/networking/WLAN/profile/v2` espace de noms et l’élément [**Onex**](onexschema-onex-element.md) est dans l’espace de `https://www.microsoft.com/networking/OneX/v1` noms.</span><span class="sxs-lookup"><span data-stu-id="66878-230">There are two exceptions: the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace and the [**OneX**](onexschema-onex-element.md) element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="66878-231">L’élément [**FipsMode**](wlan-profileschema-fipsmode-authencryption-element.md) peut être inséré en tant qu’enfant de l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="66878-231">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="66878-232">L’élément [**Onex**](onexschema-onex-element.md) peut être inséré en tant qu’enfant de l’élément de [**sécurité (MSM)**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="66878-232">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

<span data-ttu-id="66878-233">Pour afficher la liste des éléments enfants dans une structure de type arborescence, consultez [ \_ éléments de schéma de profil WLAN](wlan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="66878-233">To view the list of child elements in a tree-like structure, see [WLAN\_profile Schema Elements](wlan-profileschema-elements.md).</span></span>

## <a name="examples"></a><span data-ttu-id="66878-234">Exemples</span><span class="sxs-lookup"><span data-stu-id="66878-234">Examples</span></span>

<span data-ttu-id="66878-235">Pour afficher des exemples de profils, consultez la page exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="66878-235">To view sample profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66878-236">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66878-236">Requirements</span></span>



| <span data-ttu-id="66878-237">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66878-237">Requirement</span></span> | <span data-ttu-id="66878-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="66878-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="66878-239">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66878-239">Minimum supported client</span></span><br/> | <span data-ttu-id="66878-240">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66878-240">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="66878-241">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66878-241">Minimum supported server</span></span><br/> | <span data-ttu-id="66878-242">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66878-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="66878-243">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="66878-243">Redistributable</span></span><br/>          | <span data-ttu-id="66878-244">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="66878-244">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="66878-245">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66878-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66878-246">Exemples de profils sans fil</span><span class="sxs-lookup"><span data-stu-id="66878-246">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
