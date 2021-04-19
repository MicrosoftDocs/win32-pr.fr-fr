---
description: Spécifie le nombre d’entrées dans le cache PMK sur le client.
ms.assetid: 3a53f7fd-7f12-43d3-94e6-a11bec389a34
title: Élément PMKCacheSize (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheSize
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b21054ddc97c51212ea3a06207617ad85228270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536328"
---
# <a name="pmkcachesize-security-element"></a><span data-ttu-id="14b14-103">Élément PMKCacheSize (Security)</span><span class="sxs-lookup"><span data-stu-id="14b14-103">PMKCacheSize (security) Element</span></span>

<span data-ttu-id="14b14-104">L’élément PMKCacheSize (Security) spécifie le nombre d’entrées dans le cache PMK sur le client.</span><span class="sxs-lookup"><span data-stu-id="14b14-104">The PMKCacheSize (security) element specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="14b14-105">Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ».</span><span class="sxs-lookup"><span data-stu-id="14b14-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="14b14-106">Si **PMKCacheMode** est activé et que cet élément est absent, la taille du cache est par défaut de 128 entrées.</span><span class="sxs-lookup"><span data-stu-id="14b14-106">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span>

<span data-ttu-id="14b14-107">La mise en cache de la clé PMK est décrite dans la spécification [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="14b14-107">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="14b14-108">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="14b14-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheSize"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="255"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="14b14-109">L’élément est défini par l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="14b14-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b14-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14b14-110">Requirements</span></span>



| <span data-ttu-id="14b14-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14b14-111">Requirement</span></span> | <span data-ttu-id="14b14-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="14b14-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14b14-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14b14-113">Minimum supported client</span></span><br/> | <span data-ttu-id="14b14-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14b14-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14b14-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14b14-115">Minimum supported server</span></span><br/> | <span data-ttu-id="14b14-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14b14-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14b14-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14b14-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="14b14-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="14b14-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="14b14-119">**caution**</span><span class="sxs-lookup"><span data-stu-id="14b14-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="14b14-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="14b14-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="14b14-121">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="14b14-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




