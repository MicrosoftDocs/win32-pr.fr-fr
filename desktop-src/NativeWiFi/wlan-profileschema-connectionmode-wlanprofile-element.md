---
description: Indique si la connexion à un réseau local sans fil doit être automatique ou lancée par l’utilisateur.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: Élément connectionMode (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753756"
---
# <a name="connectionmode-wlanprofile-element"></a><span data-ttu-id="6ae60-103">Élément connectionMode (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="6ae60-103">connectionMode (WLANProfile) Element</span></span>

<span data-ttu-id="6ae60-104">L’élément connectionMode (WLANProfile) indique si la connexion à un réseau local sans fil doit être automatique ou lancée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6ae60-104">The connectionMode (WLANProfile) element indicates whether connection to a wireless LAN should be automatic or initiated by user.</span></span>

<span data-ttu-id="6ae60-105">Si [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) est défini sur ESS, cette valeur peut être automatique ou manuelle.</span><span class="sxs-lookup"><span data-stu-id="6ae60-105">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either auto or manual.</span></span> <span data-ttu-id="6ae60-106">La valeur par défaut est auto si cet élément est absent.</span><span class="sxs-lookup"><span data-stu-id="6ae60-106">The default value is auto if this element is absent.</span></span>

<span data-ttu-id="6ae60-107">Si [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) est défini sur IBSS, cette valeur doit être manuelle.</span><span class="sxs-lookup"><span data-stu-id="6ae60-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be manual.</span></span>

``` syntax
<xs:element name="connectionMode">
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
```

<span data-ttu-id="6ae60-108">L’élément **connectionMode** est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6ae60-108">The **connectionMode** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ae60-109">Notes</span><span class="sxs-lookup"><span data-stu-id="6ae60-109">Remarks</span></span>

<span data-ttu-id="6ae60-110">Le tableau suivant décrit les valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="6ae60-110">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="6ae60-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ae60-111">Value</span></span>  | <span data-ttu-id="6ae60-112">Description</span><span class="sxs-lookup"><span data-stu-id="6ae60-112">Description</span></span>                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae60-113">auto</span><span class="sxs-lookup"><span data-stu-id="6ae60-113">auto</span></span>   | <span data-ttu-id="6ae60-114">La connexion au réseau sans fil doit être lancée automatiquement chaque fois que le réseau est à portée.</span><span class="sxs-lookup"><span data-stu-id="6ae60-114">The connection to the wireless network should be initiated automatically whenever the network is in range.</span></span> |
| <span data-ttu-id="6ae60-115">manual</span><span class="sxs-lookup"><span data-stu-id="6ae60-115">manual</span></span> | <span data-ttu-id="6ae60-116">La connexion au réseau sans fil est uniquement initialisée par sur la demande explicite d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6ae60-116">The connection to the wireless network is only initated upon the explicit request of a user.</span></span>               |



 

## <a name="examples"></a><span data-ttu-id="6ae60-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="6ae60-117">Examples</span></span>

<span data-ttu-id="6ae60-118">Pour afficher des exemples de profils qui utilisent l’élément **connectionMode** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="6ae60-118">To view sample profiles that use the **connectionMode** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae60-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ae60-119">Requirements</span></span>



| <span data-ttu-id="6ae60-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ae60-120">Requirement</span></span> | <span data-ttu-id="6ae60-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ae60-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6ae60-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ae60-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae60-123">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ae60-123">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6ae60-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ae60-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae60-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ae60-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6ae60-126">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6ae60-126">Redistributable</span></span><br/>          | <span data-ttu-id="6ae60-127">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="6ae60-127">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6ae60-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ae60-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="6ae60-129">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="6ae60-129">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6ae60-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="6ae60-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="6ae60-131">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="6ae60-131">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6ae60-132">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="6ae60-132">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




