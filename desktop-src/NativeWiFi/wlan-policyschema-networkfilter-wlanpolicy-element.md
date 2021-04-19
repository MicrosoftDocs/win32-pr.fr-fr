---
description: Définit la liste des réseaux autorisés et refusés pour les ordinateurs.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Élément networkFilter (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528310"
---
# <a name="networkfilter-wlanpolicy-element"></a><span data-ttu-id="c0d57-103">Élément networkFilter (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="c0d57-103">networkFilter (WLANPolicy) Element</span></span>

<span data-ttu-id="c0d57-104">L’élément networkFilter (WLANPolicy) définit la liste des réseaux autorisés et refusés pour les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="c0d57-104">The networkFilter (WLANPolicy) element defines the list of allowed and denied networks for machines.</span></span>

``` syntax
<xs:element name="networkFilter">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="allowList"
                minOccurs="0"
            >
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
            <xs:element name="blockList"
                minOccurs="0"
            >
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
            <xs:element name="denyAllIBSS"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="denyAllESS"
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

<span data-ttu-id="c0d57-105">L’élément **networkFilter** est défini par l’élément [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c0d57-105">The **networkFilter** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c0d57-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c0d57-106">Child elements</span></span>



| <span data-ttu-id="c0d57-107">Élément</span><span class="sxs-lookup"><span data-stu-id="c0d57-107">Element</span></span>                                                                    | <span data-ttu-id="c0d57-108">Type</span><span class="sxs-lookup"><span data-stu-id="c0d57-108">Type</span></span>                                                                     | <span data-ttu-id="c0d57-109">Description</span><span class="sxs-lookup"><span data-stu-id="c0d57-109">Description</span></span>                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0d57-110">**allowList**</span><span class="sxs-lookup"><span data-stu-id="c0d57-110">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="c0d57-111">Liste des réseaux locaux sans fil auxquels un ordinateur doit être autorisé à se connecter.</span><span class="sxs-lookup"><span data-stu-id="c0d57-111">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/> |
| [<span data-ttu-id="c0d57-112">**Noires**</span><span class="sxs-lookup"><span data-stu-id="c0d57-112">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="c0d57-113">Liste des réseaux locaux sans fil auxquels un ordinateur ne doit pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="c0d57-113">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>              |
| [<span data-ttu-id="c0d57-114">**denyAllESS**</span><span class="sxs-lookup"><span data-stu-id="c0d57-114">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)   | <span data-ttu-id="c0d57-115">boolean</span><span class="sxs-lookup"><span data-stu-id="c0d57-115">boolean</span></span>                                                                  | <span data-ttu-id="c0d57-116">Spécifie si l’accès à tous les réseaux d’infrastructure est bloqué.</span><span class="sxs-lookup"><span data-stu-id="c0d57-116">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                     |
| [<span data-ttu-id="c0d57-117">**denyAllIBSS**</span><span class="sxs-lookup"><span data-stu-id="c0d57-117">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md) | <span data-ttu-id="c0d57-118">boolean</span><span class="sxs-lookup"><span data-stu-id="c0d57-118">boolean</span></span>                                                                  | <span data-ttu-id="c0d57-119">Spécifie si l’accès à tous les réseaux ad hoc est bloqué.</span><span class="sxs-lookup"><span data-stu-id="c0d57-119">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                             |
| [<span data-ttu-id="c0d57-120">**réseaux**</span><span class="sxs-lookup"><span data-stu-id="c0d57-120">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)             | [<span data-ttu-id="c0d57-121">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="c0d57-121">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="c0d57-122">Un réseau autorisé.</span><span class="sxs-lookup"><span data-stu-id="c0d57-122">An allowed network.</span></span> <br/>                                                                |
| [<span data-ttu-id="c0d57-123">**réseaux**</span><span class="sxs-lookup"><span data-stu-id="c0d57-123">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)             | [<span data-ttu-id="c0d57-124">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="c0d57-124">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="c0d57-125">Un réseau bloqué.</span><span class="sxs-lookup"><span data-stu-id="c0d57-125">A blocked network.</span></span> <br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="c0d57-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0d57-126">Requirements</span></span>



| <span data-ttu-id="c0d57-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0d57-127">Requirement</span></span> | <span data-ttu-id="c0d57-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0d57-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0d57-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0d57-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c0d57-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0d57-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c0d57-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0d57-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c0d57-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0d57-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0d57-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0d57-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0d57-134">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="c0d57-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c0d57-135">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="c0d57-135">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="c0d57-136">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="c0d57-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c0d57-137">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="c0d57-137">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




