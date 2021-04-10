---
description: Spécifie la liste des réseaux locaux sans fil auxquels un ordinateur ne doit pas se connecter.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: Élément de blocage (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e852286d00d93904bd185fef6c2f3444bb5987f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950927"
---
# <a name="blocklist-networkfilter-element"></a><span data-ttu-id="0549c-103">Élément de blocage (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="0549c-103">blockList (networkFilter) Element</span></span>

<span data-ttu-id="0549c-104">L’élément de liste de blocage (networkFilter) spécifie la liste des réseaux locaux sans fil auxquels un ordinateur ne doit pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="0549c-104">The blockList (networkFilter) element specifies the list of wireless LAN networks to which a machine must not connect.</span></span>

``` syntax
<xs:element name="blockList">
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

<span data-ttu-id="0549c-105">L' **élément de la** en-dessus est défini par l’élément [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0549c-105">The **blockList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0549c-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0549c-106">Child elements</span></span>



| <span data-ttu-id="0549c-107">Élément</span><span class="sxs-lookup"><span data-stu-id="0549c-107">Element</span></span>                                                        | <span data-ttu-id="0549c-108">Type</span><span class="sxs-lookup"><span data-stu-id="0549c-108">Type</span></span>                                                                     | <span data-ttu-id="0549c-109">Description</span><span class="sxs-lookup"><span data-stu-id="0549c-109">Description</span></span>                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="0549c-110">**réseaux**</span><span class="sxs-lookup"><span data-stu-id="0549c-110">**network**</span></span>](wlan-policyschema-network-blocklist-element.md) | [<span data-ttu-id="0549c-111">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="0549c-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="0549c-112">Réseau bloqué.</span><span class="sxs-lookup"><span data-stu-id="0549c-112">The blocked network.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="0549c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0549c-113">Requirements</span></span>



| <span data-ttu-id="0549c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0549c-114">Requirement</span></span> | <span data-ttu-id="0549c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0549c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0549c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0549c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0549c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0549c-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0549c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0549c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0549c-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0549c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0549c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0549c-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="0549c-121">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="0549c-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0549c-122">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="0549c-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="0549c-123">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="0549c-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0549c-124">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="0549c-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




