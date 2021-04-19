---
description: Indique si la pré-authentification est utilisée par le client.
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: Élément preAuthMode (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ac74f193fb89c260b1a121b673f239147658865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515629"
---
# <a name="preauthmode-security-element"></a><span data-ttu-id="18614-103">Élément preAuthMode (Security)</span><span class="sxs-lookup"><span data-stu-id="18614-103">preAuthMode (security) Element</span></span>

<span data-ttu-id="18614-104">L’élément preAuthMode (Security) indique si la pré-authentification est utilisée par le client.</span><span class="sxs-lookup"><span data-stu-id="18614-104">The preAuthMode (security) element indicates whether pre-authentication will be used by the client.</span></span> <span data-ttu-id="18614-105">La pré-authentification est nécessaire pour l’itinérance sécurisée sécurisée WPA2.</span><span class="sxs-lookup"><span data-stu-id="18614-105">Pre-authentication is necessary for WPA2 secure fast roaming.</span></span> <span data-ttu-id="18614-106">Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ».</span><span class="sxs-lookup"><span data-stu-id="18614-106">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="18614-107">Si **PMKCacheMode** est activé et que cet élément est absent, la valeur par défaut est « Disabled ».</span><span class="sxs-lookup"><span data-stu-id="18614-107">If **PMKCacheMode** is enabled, and this element is absent, the default value is "disabled".</span></span>

<span data-ttu-id="18614-108">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="18614-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthMode"
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

<span data-ttu-id="18614-109">L’élément est défini par l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="18614-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="18614-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18614-110">Requirements</span></span>



| <span data-ttu-id="18614-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18614-111">Requirement</span></span> | <span data-ttu-id="18614-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="18614-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="18614-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18614-113">Minimum supported client</span></span><br/> | <span data-ttu-id="18614-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18614-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="18614-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18614-115">Minimum supported server</span></span><br/> | <span data-ttu-id="18614-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18614-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18614-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18614-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="18614-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="18614-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="18614-119">**caution**</span><span class="sxs-lookup"><span data-stu-id="18614-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="18614-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="18614-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="18614-121">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="18614-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




