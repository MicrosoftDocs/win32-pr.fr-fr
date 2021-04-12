---
description: Spécifie la méthode d’authentification à utiliser pour se connecter au réseau local sans fil.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: Élément Authentication (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201833"
---
# <a name="authentication-authencryption-element"></a><span data-ttu-id="ef5b1-103">Élément Authentication (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="ef5b1-103">authentication (authEncryption) Element</span></span>

<span data-ttu-id="ef5b1-104">L’élément Authentication (authEncryption) spécifie la méthode d’authentification à utiliser pour se connecter au réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-104">The authentication (authEncryption) element specifies the authentication method to be used to connect to the wireless LAN.</span></span>

``` syntax
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
```

<span data-ttu-id="ef5b1-105">L’élément est défini par l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ef5b1-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef5b1-106">Notes</span><span class="sxs-lookup"><span data-stu-id="ef5b1-106">Remarks</span></span>

<span data-ttu-id="ef5b1-107">Le tableau suivant décrit les valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-107">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="ef5b1-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef5b1-108">Value</span></span>   | <span data-ttu-id="ef5b1-109">Description</span><span class="sxs-lookup"><span data-stu-id="ef5b1-109">Description</span></span>                            |
|---------|----------------------------------------|
| <span data-ttu-id="ef5b1-110">ouvert</span><span class="sxs-lookup"><span data-stu-id="ef5b1-110">open</span></span>    | <span data-ttu-id="ef5b1-111">Ouvrez l’authentification 802,11.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-111">Open 802.11 authentication.</span></span>            |
| <span data-ttu-id="ef5b1-112">partagés</span><span class="sxs-lookup"><span data-stu-id="ef5b1-112">shared</span></span>  | <span data-ttu-id="ef5b1-113">Authentification 802,11 partagée.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-113">Shared 802.11 authentication.</span></span>          |
| <span data-ttu-id="ef5b1-114">WPA</span><span class="sxs-lookup"><span data-stu-id="ef5b1-114">WPA</span></span>     | <span data-ttu-id="ef5b1-115">WPA-Enterprise l’authentification 802,11.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-115">WPA-Enterprise 802.11 authentication.</span></span>  |
| <span data-ttu-id="ef5b1-116">WPAPSK</span><span class="sxs-lookup"><span data-stu-id="ef5b1-116">WPAPSK</span></span>  | <span data-ttu-id="ef5b1-117">WPA-Personal l’authentification 802,11.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-117">WPA-Personal 802.11 authentication.</span></span>    |
| <span data-ttu-id="ef5b1-118">WPA2</span><span class="sxs-lookup"><span data-stu-id="ef5b1-118">WPA2</span></span>    | <span data-ttu-id="ef5b1-119">WPA2-Enterprise l’authentification 802,11.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-119">WPA2-Enterprise 802.11 authentication.</span></span> |
| <span data-ttu-id="ef5b1-120">WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="ef5b1-120">WPA2PSK</span></span> | <span data-ttu-id="ef5b1-121">WPA2-Personal l’authentification 802,11.</span><span class="sxs-lookup"><span data-stu-id="ef5b1-121">WPA2-Personal 802.11 authentication.</span></span>   |



 

<span data-ttu-id="ef5b1-122">Pour plus d’informations sur les méthodes d’authentification 802,11, consultez les spécifications [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)et [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="ef5b1-122">For more information about 802.11 authentication methods, see the [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1X](https://ieeexplore.ieee.org/document/1438730), and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="ef5b1-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="ef5b1-123">Examples</span></span>

<span data-ttu-id="ef5b1-124">Pour afficher des exemples de profils qui utilisent l’élément **Authentication** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ef5b1-124">To view sample profiles that use the **authentication** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef5b1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef5b1-125">Requirements</span></span>



| <span data-ttu-id="ef5b1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef5b1-126">Requirement</span></span> | <span data-ttu-id="ef5b1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef5b1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ef5b1-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef5b1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ef5b1-129">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef5b1-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ef5b1-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef5b1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ef5b1-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef5b1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ef5b1-132">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="ef5b1-132">Redistributable</span></span><br/>          | <span data-ttu-id="ef5b1-133">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="ef5b1-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ef5b1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef5b1-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef5b1-135">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="ef5b1-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ef5b1-136">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="ef5b1-136">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="ef5b1-137">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="ef5b1-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ef5b1-138">**authEncryption (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="ef5b1-138">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




