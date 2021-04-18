---
description: Spécifie le nom et le type d’un réseau sans fil.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: Type complexe networkItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526234"
---
# <a name="networkitemtype-complex-type"></a><span data-ttu-id="46535-103">Type complexe networkItemType</span><span class="sxs-lookup"><span data-stu-id="46535-103">networkItemType Complex Type</span></span>

<span data-ttu-id="46535-104">Le type complexe networkItemType spécifie le nom et le type d’un réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="46535-104">The networkItemType complex type specifies the name and type of a wireless network.</span></span>

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="46535-105">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="46535-105">Child elements</span></span>



| <span data-ttu-id="46535-106">Élément</span><span class="sxs-lookup"><span data-stu-id="46535-106">Element</span></span>                                                                      | <span data-ttu-id="46535-107">Type</span><span class="sxs-lookup"><span data-stu-id="46535-107">Type</span></span>                                                                    | <span data-ttu-id="46535-108">Description</span><span class="sxs-lookup"><span data-stu-id="46535-108">Description</span></span>                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="46535-109">**networkName**</span><span class="sxs-lookup"><span data-stu-id="46535-109">**networkName**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md) | [<span data-ttu-id="46535-110">**networkNameType**</span><span class="sxs-lookup"><span data-stu-id="46535-110">**networkNameType**</span></span>](wlan-policyschema-networknametype-simpletype.md) | <span data-ttu-id="46535-111">Identificateur SSID (Service Set Identifier) du réseau.</span><span class="sxs-lookup"><span data-stu-id="46535-111">The service set identifier (SSID) of the network.</span></span> <br/> |
| [<span data-ttu-id="46535-112">**networkType**</span><span class="sxs-lookup"><span data-stu-id="46535-112">**networkType**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md) | [<span data-ttu-id="46535-113">**networkTypeType**</span><span class="sxs-lookup"><span data-stu-id="46535-113">**networkTypeType**</span></span>](wlan-policyschema-networktypetype-simpletype.md) | <span data-ttu-id="46535-114">Type de réseau.</span><span class="sxs-lookup"><span data-stu-id="46535-114">The network type.</span></span> <br/>                                 |



## <a name="requirements"></a><span data-ttu-id="46535-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46535-115">Requirements</span></span>



| <span data-ttu-id="46535-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46535-116">Requirement</span></span> | <span data-ttu-id="46535-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="46535-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46535-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46535-118">Minimum supported client</span></span><br/> | <span data-ttu-id="46535-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46535-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46535-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46535-120">Minimum supported server</span></span><br/> | <span data-ttu-id="46535-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46535-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




