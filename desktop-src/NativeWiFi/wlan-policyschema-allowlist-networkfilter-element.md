---
description: Spécifie la liste des réseaux locaux sans fil auxquels un ordinateur doit être autorisé à se connecter.
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: Élément allowList (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5488f962a1ba526b34ca2d10144a150d7c1417d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515396"
---
# <a name="allowlist-networkfilter-element"></a><span data-ttu-id="2cce8-103">Élément allowList (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="2cce8-103">allowList (networkFilter) Element</span></span>

<span data-ttu-id="2cce8-104">L’élément allowList (networkFilter) spécifie la liste des réseaux locaux sans fil auxquels un ordinateur doit être autorisé à se connecter.</span><span class="sxs-lookup"><span data-stu-id="2cce8-104">The allowList (networkFilter) element specifies the list of wireless LAN networks to which any machine must be allowed to connect.</span></span>

``` syntax
<xs:element name="allowList">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="network"
                type="networkItemType"
                maxOccurs="unbounded"
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

<span data-ttu-id="2cce8-105">L’élément **allowList** est défini par l’élément [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2cce8-105">The **allowList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2cce8-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2cce8-106">Child elements</span></span>



| <span data-ttu-id="2cce8-107">Élément</span><span class="sxs-lookup"><span data-stu-id="2cce8-107">Element</span></span>                                                        | <span data-ttu-id="2cce8-108">Type</span><span class="sxs-lookup"><span data-stu-id="2cce8-108">Type</span></span>                                                                     | <span data-ttu-id="2cce8-109">Description</span><span class="sxs-lookup"><span data-stu-id="2cce8-109">Description</span></span>                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="2cce8-110">**réseaux**</span><span class="sxs-lookup"><span data-stu-id="2cce8-110">**network**</span></span>](wlan-policyschema-network-allowlist-element.md) | [<span data-ttu-id="2cce8-111">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="2cce8-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="2cce8-112">Réseau auquel la machine peut se connecter.</span><span class="sxs-lookup"><span data-stu-id="2cce8-112">The network to which the machine can connect.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2cce8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cce8-113">Requirements</span></span>



| <span data-ttu-id="2cce8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cce8-114">Requirement</span></span> | <span data-ttu-id="2cce8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cce8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2cce8-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cce8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2cce8-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cce8-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2cce8-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cce8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2cce8-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cce8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cce8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cce8-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="2cce8-121">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="2cce8-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2cce8-122">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="2cce8-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="2cce8-123">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="2cce8-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2cce8-124">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="2cce8-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




