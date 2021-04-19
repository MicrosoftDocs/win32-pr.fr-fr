---
description: Définit un réseau bloqué.
ms.assetid: ccf24d45-cae0-4eb7-951a-004a5f71e04a
title: Élément de réseau (de blocage)
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
ms.openlocfilehash: f58948573db281aacb00e227ff0fbc2f1cdf82b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541998"
---
# <a name="network-blocklist-element"></a><span data-ttu-id="3802e-103">Élément de réseau (de blocage)</span><span class="sxs-lookup"><span data-stu-id="3802e-103">network (blockList) Element</span></span>

<span data-ttu-id="3802e-104">L’élément réseau (de blocage) définit un réseau bloqué.</span><span class="sxs-lookup"><span data-stu-id="3802e-104">The network (blockList) element defines a blocked network.</span></span> <span data-ttu-id="3802e-105">Un ordinateur ne peut pas se connecter à un réseau bloqué.</span><span class="sxs-lookup"><span data-stu-id="3802e-105">A machine cannot connect to a blocked network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="3802e-106">L’élément **réseau** est défini [**par l’élément de la**](wlan-policyschema-blocklist-networkfilter-element.md) en-dessus.</span><span class="sxs-lookup"><span data-stu-id="3802e-106">The **network** element is defined by the [**blockList**](wlan-policyschema-blocklist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3802e-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3802e-107">Requirements</span></span>



| <span data-ttu-id="3802e-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3802e-108">Requirement</span></span> | <span data-ttu-id="3802e-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="3802e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3802e-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3802e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="3802e-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3802e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3802e-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3802e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="3802e-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3802e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3802e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3802e-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="3802e-115">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="3802e-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3802e-116">**Noires**</span><span class="sxs-lookup"><span data-stu-id="3802e-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="3802e-117">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="3802e-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3802e-118">**Blocage (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="3802e-118">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> </dl>

 

 




