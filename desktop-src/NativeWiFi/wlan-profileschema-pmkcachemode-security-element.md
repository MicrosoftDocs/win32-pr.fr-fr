---
description: Indique si la mise en cache PMK sera utilisée.
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: Élément PMKCacheMode (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 609660d6f3161cbaaa5e0505daf9c6b9180b6c32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112731"
---
# <a name="pmkcachemode-security-element"></a><span data-ttu-id="906b6-103">Élément PMKCacheMode (Security)</span><span class="sxs-lookup"><span data-stu-id="906b6-103">PMKCacheMode (security) Element</span></span>

<span data-ttu-id="906b6-104">L’élément PMKCacheMode (Security) indique si la mise en cache PMK sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="906b6-104">The PMKCacheMode (security) element indicates whether PMK caching will be used.</span></span> <span data-ttu-id="906b6-105">Cet élément est valide uniquement pour les réseaux définis par WPA2.</span><span class="sxs-lookup"><span data-stu-id="906b6-105">This element is valid only for WPA2-defined networks.</span></span> <span data-ttu-id="906b6-106">La mise en cache de la clé PMK est décrite dans la spécification [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="906b6-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="906b6-107">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="906b6-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="906b6-108">L’élément est défini par l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="906b6-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="906b6-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="906b6-109">Requirements</span></span>



| <span data-ttu-id="906b6-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="906b6-110">Requirement</span></span> | <span data-ttu-id="906b6-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="906b6-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="906b6-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="906b6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="906b6-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="906b6-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="906b6-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="906b6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="906b6-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="906b6-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="906b6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="906b6-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="906b6-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="906b6-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="906b6-118">**caution**</span><span class="sxs-lookup"><span data-stu-id="906b6-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="906b6-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="906b6-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="906b6-120">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="906b6-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




