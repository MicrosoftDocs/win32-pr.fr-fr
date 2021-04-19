---
description: Définit un réseau autorisé.
ms.assetid: 6dd90924-ded4-427d-a6cd-7742acf89c21
title: Élément Network (allowList)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: eb89a3037b7684c4e20e26ef3a2b0502be69251a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541237"
---
# <a name="network-allowlist-element"></a><span data-ttu-id="58e6b-103">Élément Network (allowList)</span><span class="sxs-lookup"><span data-stu-id="58e6b-103">network (allowList) Element</span></span>

<span data-ttu-id="58e6b-104">L’élément allowList (Network) définit un réseau autorisé.</span><span class="sxs-lookup"><span data-stu-id="58e6b-104">The network (allowList) element defines an allowed network.</span></span> <span data-ttu-id="58e6b-105">Un ordinateur doit être autorisé à se connecter à un réseau autorisé.</span><span class="sxs-lookup"><span data-stu-id="58e6b-105">A machine must be allowed to connect to an allowed network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="58e6b-106">L’élément **réseau** est défini par l’élément [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md) .</span><span class="sxs-lookup"><span data-stu-id="58e6b-106">The **network** element is defined by the [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e6b-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58e6b-107">Requirements</span></span>



| <span data-ttu-id="58e6b-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58e6b-108">Requirement</span></span> | <span data-ttu-id="58e6b-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="58e6b-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58e6b-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58e6b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="58e6b-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58e6b-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="58e6b-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58e6b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="58e6b-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58e6b-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58e6b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58e6b-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="58e6b-115">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="58e6b-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="58e6b-116">**allowList**</span><span class="sxs-lookup"><span data-stu-id="58e6b-116">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="58e6b-117">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="58e6b-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="58e6b-118">**allowList (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="58e6b-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> </dl>

 

 




