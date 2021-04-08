---
description: Contient un SSID pour un réseau local sans fil.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: Élément SSID (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866030"
---
# <a name="ssid-ssidconfig-element"></a><span data-ttu-id="6f33a-103">Élément SSID (SSIDConfig)</span><span class="sxs-lookup"><span data-stu-id="6f33a-103">SSID (SSIDConfig) Element</span></span>

<span data-ttu-id="6f33a-104">L’élément SSID (SSIDConfig) contient un SSID pour un réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="6f33a-104">The SSID (SSIDConfig) element contains an SSID for a wireless LAN.</span></span>

<span data-ttu-id="6f33a-105">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Au plus un élément **SSID** peut apparaître dans un profil.</span><span class="sxs-lookup"><span data-stu-id="6f33a-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one **SSID** element can appear in a profile.</span></span>

``` syntax
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
```

<span data-ttu-id="6f33a-106">L’élément **SSID** est défini par l’élément [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6f33a-106">The **SSID** element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6f33a-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6f33a-107">Child elements</span></span>



| <span data-ttu-id="6f33a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="6f33a-108">Element</span></span>                                              | <span data-ttu-id="6f33a-109">Type</span><span class="sxs-lookup"><span data-stu-id="6f33a-109">Type</span></span> | <span data-ttu-id="6f33a-110">Description</span><span class="sxs-lookup"><span data-stu-id="6f33a-110">Description</span></span>                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [<span data-ttu-id="6f33a-111">**hex**</span><span class="sxs-lookup"><span data-stu-id="6f33a-111">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)   |      | <span data-ttu-id="6f33a-112">Contient le SSID d’un réseau local sans fil au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="6f33a-112">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/> |
| [<span data-ttu-id="6f33a-113">**nomme**</span><span class="sxs-lookup"><span data-stu-id="6f33a-113">**name**</span></span>](wlan-profileschema-name-ssid-element.md) |      | <span data-ttu-id="6f33a-114">Contient le SSID d’un réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="6f33a-114">Contains the SSID for a wireless LAN.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="6f33a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6f33a-115">Remarks</span></span>

<span data-ttu-id="6f33a-116">Bien que les éléments [**Hex**](wlan-profileschema-hex-ssid-element.md) et [**Name**](wlan-profileschema-name-ssid-element.md) soient facultatifs, au moins un élément **Hex** ou [**Name**](wlan-profileschema-name-ssid-element.md) doit apparaître en tant qu’enfant de l’élément **SSID** .</span><span class="sxs-lookup"><span data-stu-id="6f33a-116">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the **SSID** element.</span></span>

<span data-ttu-id="6f33a-117">Lorsque les informations de profil sont converties en SSID, l’élément [**Hex**](wlan-profileschema-hex-ssid-element.md) est converti en SSID (le cas échéant) et l’élément [**Name**](wlan-profileschema-name-ssid-element.md) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6f33a-117">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored.</span></span> <span data-ttu-id="6f33a-118">Si l’élément **Hex** n’est pas présent, l’élément [**Name**](wlan-profileschema-name-ssid-element.md) est converti en SSID à l’aide d’une conversion Unicode en ASCII.</span><span class="sxs-lookup"><span data-stu-id="6f33a-118">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="6f33a-119">Lorsqu’un SSID est stocké dans un profil, l’élément [**Hex**](wlan-profileschema-hex-ssid-element.md) est toujours généré.</span><span class="sxs-lookup"><span data-stu-id="6f33a-119">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="6f33a-120">L’élément [**Name**](wlan-profileschema-name-ssid-element.md) est généré uniquement si la conversion ASCII en Unicode du SSID et de la génération de profil XML réussit.</span><span class="sxs-lookup"><span data-stu-id="6f33a-120">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="6f33a-121">Certaines informations du SSID d’origine peuvent être perdues lorsqu’elles sont converties en un [**nom**](wlan-profileschema-name-ssid-element.md).</span><span class="sxs-lookup"><span data-stu-id="6f33a-121">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6f33a-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="6f33a-122">Examples</span></span>

<span data-ttu-id="6f33a-123">Pour afficher des exemples de profils qui utilisent l’élément **SSID** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="6f33a-123">To view sample profiles that use the **SSID** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f33a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f33a-124">Requirements</span></span>



| <span data-ttu-id="6f33a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f33a-125">Requirement</span></span> | <span data-ttu-id="6f33a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f33a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6f33a-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f33a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6f33a-128">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f33a-128">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6f33a-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f33a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6f33a-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f33a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6f33a-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6f33a-131">Redistributable</span></span><br/>          | <span data-ttu-id="6f33a-132">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="6f33a-132">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6f33a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f33a-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f33a-134">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="6f33a-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6f33a-135">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="6f33a-135">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="6f33a-136">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="6f33a-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6f33a-137">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="6f33a-137">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




