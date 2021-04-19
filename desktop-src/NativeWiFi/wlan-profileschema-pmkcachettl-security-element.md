---
description: Indique la durée, en minutes, pendant laquelle un cache PMK est conservé.
ms.assetid: d9e3b839-48f6-490c-ab83-067368cdcca2
title: Élément PMKCacheTTL (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheTTL
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bdfe0edb163dc2bc9766ba8562defb026bbe21fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513386"
---
# <a name="pmkcachettl-security-element"></a><span data-ttu-id="85311-103">Élément PMKCacheTTL (Security)</span><span class="sxs-lookup"><span data-stu-id="85311-103">PMKCacheTTL (security) Element</span></span>

<span data-ttu-id="85311-104">L’élément PMKCacheTTL (Security) indique la durée, en minutes, pendant laquelle un cache PMK est conservé.</span><span class="sxs-lookup"><span data-stu-id="85311-104">The PMKCacheTTL (security) element indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="85311-105">Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ».</span><span class="sxs-lookup"><span data-stu-id="85311-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span>

<span data-ttu-id="85311-106">La mise en cache de la clé PMK est décrite dans la spécification [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="85311-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="85311-107">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="85311-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheTTL"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="5"
             />
            <xs:maxInclusive
                value="1440"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="85311-108">L’élément est défini par l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="85311-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="85311-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85311-109">Requirements</span></span>



| <span data-ttu-id="85311-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85311-110">Requirement</span></span> | <span data-ttu-id="85311-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="85311-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85311-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85311-112">Minimum supported client</span></span><br/> | <span data-ttu-id="85311-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85311-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="85311-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85311-114">Minimum supported server</span></span><br/> | <span data-ttu-id="85311-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85311-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85311-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85311-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="85311-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="85311-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="85311-118">**caution**</span><span class="sxs-lookup"><span data-stu-id="85311-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="85311-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="85311-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="85311-120">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="85311-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




