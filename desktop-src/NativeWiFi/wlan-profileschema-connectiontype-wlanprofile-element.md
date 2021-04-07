---
description: Indique le mode de fonctionnement du réseau.
ms.assetid: b71de38a-6373-4d96-90dd-a3ad4a7de074
title: Élément connectionType (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1e7b456260c656ebb3d64b6a3732fe97ca3ca488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863349"
---
# <a name="connectiontype-wlanprofile-element"></a><span data-ttu-id="3673b-103">Élément connectionType (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="3673b-103">connectionType (WLANProfile) Element</span></span>

<span data-ttu-id="3673b-104">L’élément connectionType (WLANProfile) indique le mode de fonctionnement du réseau.</span><span class="sxs-lookup"><span data-stu-id="3673b-104">The connectionType (WLANProfile) element indicates the operating mode of the network.</span></span>

<span data-ttu-id="3673b-105">La valeur **ESS** indique un réseau d’infrastructure, tandis que **IBSS** indique un réseau ad hoc.</span><span class="sxs-lookup"><span data-stu-id="3673b-105">A value of **ESS** indicates an infrastructure network, while **IBSS** indicates an ad-hoc network.</span></span>

``` syntax
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
```

<span data-ttu-id="3673b-106">L’élément **ConnectionType** est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3673b-106">The **connectionType** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="3673b-107">Exemples</span><span class="sxs-lookup"><span data-stu-id="3673b-107">Examples</span></span>

<span data-ttu-id="3673b-108">Pour afficher des exemples de profils qui utilisent l’élément **ConnectionType** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="3673b-108">To view sample profiles that use the **connectionType** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3673b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3673b-109">Requirements</span></span>



| <span data-ttu-id="3673b-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3673b-110">Requirement</span></span> | <span data-ttu-id="3673b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="3673b-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="3673b-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3673b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3673b-113">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3673b-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3673b-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3673b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3673b-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3673b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="3673b-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3673b-116">Redistributable</span></span><br/>          | <span data-ttu-id="3673b-117">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="3673b-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3673b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3673b-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="3673b-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="3673b-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3673b-120">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="3673b-120">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="3673b-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="3673b-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3673b-122">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="3673b-122">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




