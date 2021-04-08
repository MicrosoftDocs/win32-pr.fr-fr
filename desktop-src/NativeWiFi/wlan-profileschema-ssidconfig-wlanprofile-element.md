---
description: Contient un ou plusieurs SSID pour les réseaux locaux sans fil.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Élément SSIDConfig (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865738"
---
# <a name="ssidconfig-wlanprofile-element"></a><span data-ttu-id="36aa3-103">Élément SSIDConfig (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="36aa3-103">SSIDConfig (WLANProfile) Element</span></span>

<span data-ttu-id="36aa3-104">L’élément SSIDConfig (WLANProfile) contient un ou plusieurs SSID pour les réseaux locaux sans fil.</span><span class="sxs-lookup"><span data-stu-id="36aa3-104">The SSIDConfig (WLANProfile) element contains one or more SSIDs for wireless LANs.</span></span>

``` syntax
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
```

<span data-ttu-id="36aa3-105">L’élément **SSIDConfig** est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="36aa3-105">The **SSIDConfig** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="36aa3-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="36aa3-106">Child elements</span></span>



| <span data-ttu-id="36aa3-107">Élément</span><span class="sxs-lookup"><span data-stu-id="36aa3-107">Element</span></span>                                                                    | <span data-ttu-id="36aa3-108">Type</span><span class="sxs-lookup"><span data-stu-id="36aa3-108">Type</span></span>                                                              | <span data-ttu-id="36aa3-109">Description</span><span class="sxs-lookup"><span data-stu-id="36aa3-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36aa3-110">**hex**</span><span class="sxs-lookup"><span data-stu-id="36aa3-110">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | <span data-ttu-id="36aa3-111">Contient le SSID d’un réseau local sans fil au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="36aa3-111">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="36aa3-112">**nomme**</span><span class="sxs-lookup"><span data-stu-id="36aa3-112">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                       |                                                                   | <span data-ttu-id="36aa3-113">Contient le nom (sensible à la casse) du SSID d’un réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="36aa3-113">Contains the (case-sensitive) name of the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="36aa3-114">**ne pas diffuser**</span><span class="sxs-lookup"><span data-stu-id="36aa3-114">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [<span data-ttu-id="36aa3-115">boolean</span><span class="sxs-lookup"><span data-stu-id="36aa3-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="36aa3-116">Indique si le réseau diffuse son SSID.</span><span class="sxs-lookup"><span data-stu-id="36aa3-116">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="36aa3-117">Si [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) est défini sur ESS, cette valeur peut être **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="36aa3-117">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either **TRUE** or **FALSE**.</span></span> <span data-ttu-id="36aa3-118">La valeur par défaut est **true** si cet élément est absent.</span><span class="sxs-lookup"><span data-stu-id="36aa3-118">The default value is **TRUE** if this element is absent.</span></span><br/> <span data-ttu-id="36aa3-119">Si [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) est défini sur IBSS, cette valeur doit être **false**.</span><span class="sxs-lookup"><span data-stu-id="36aa3-119">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be **FALSE**.</span></span><br/> <span data-ttu-id="36aa3-120">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="36aa3-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="36aa3-121">**SSID**</span><span class="sxs-lookup"><span data-stu-id="36aa3-121">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | <span data-ttu-id="36aa3-122">Contient un SSID pour un réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="36aa3-122">Contains an SSID for a wireless LAN.</span></span><br/> <span data-ttu-id="36aa3-123">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Au plus un élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) peut apparaître dans un profil.</span><span class="sxs-lookup"><span data-stu-id="36aa3-123">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a><span data-ttu-id="36aa3-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="36aa3-124">Examples</span></span>

<span data-ttu-id="36aa3-125">Pour afficher des exemples de profils qui utilisent l’élément **SSIDConfig** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="36aa3-125">To view sample profiles that use the **SSIDConfig** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36aa3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36aa3-126">Requirements</span></span>



| <span data-ttu-id="36aa3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36aa3-127">Requirement</span></span> | <span data-ttu-id="36aa3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="36aa3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="36aa3-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36aa3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="36aa3-130">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36aa3-130">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="36aa3-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36aa3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="36aa3-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36aa3-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="36aa3-133">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="36aa3-133">Redistributable</span></span><br/>          | <span data-ttu-id="36aa3-134">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="36aa3-134">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="36aa3-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36aa3-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="36aa3-136">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="36aa3-136">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="36aa3-137">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="36aa3-137">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="36aa3-138">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="36aa3-138">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="36aa3-139">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="36aa3-139">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
