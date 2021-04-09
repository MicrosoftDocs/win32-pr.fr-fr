---
description: Sont utilisées pour définir une adresse MAC (Media Access Control).
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: DOT11_MAC_ADDRESS (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866041"
---
# <a name="dot11_mac_address"></a><span data-ttu-id="965ea-103">\_Adresse Mac \_ DOT11</span><span class="sxs-lookup"><span data-stu-id="965ea-103">DOT11\_MAC\_ADDRESS</span></span>

<span data-ttu-id="965ea-104">Les types d' **\_ \_ adresses Mac DOT11** sont utilisés pour définir une adresse Mac (Media Access Control).</span><span class="sxs-lookup"><span data-stu-id="965ea-104">The **DOT11\_MAC\_ADDRESS** types are used to define an IEEE media access control (MAC) address.</span></span>


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="965ea-105">**\_Adresse Mac \_ DOT11 \[ 6\]**</span><span class="sxs-lookup"><span data-stu-id="965ea-105">**DOT11\_MAC\_ADDRESS\[6\]**</span></span>
</dt> <dd>

<span data-ttu-id="965ea-106">Adresse MAC dans un format de monodiffusion, de multidiffusion ou de diffusion.</span><span class="sxs-lookup"><span data-stu-id="965ea-106">A MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> <dt>

<span data-ttu-id="965ea-107">**\_Adresse Mac \_ PDOT11**</span><span class="sxs-lookup"><span data-stu-id="965ea-107">**PDOT11\_MAC\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="965ea-108">Pointeur vers une adresse MAC dans un format de monodiffusion, de multidiffusion ou de diffusion.</span><span class="sxs-lookup"><span data-stu-id="965ea-108">Pointer to a MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="965ea-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="965ea-109">Requirements</span></span>



| <span data-ttu-id="965ea-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="965ea-110">Requirement</span></span> | <span data-ttu-id="965ea-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="965ea-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="965ea-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="965ea-112">Minimum supported client</span></span><br/> | <span data-ttu-id="965ea-113">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="965ea-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="965ea-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="965ea-114">Minimum supported server</span></span><br/> | <span data-ttu-id="965ea-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="965ea-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="965ea-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="965ea-116">Redistributable</span></span><br/>          | <span data-ttu-id="965ea-117">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="965ea-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="965ea-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="965ea-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="965ea-119"><dt>Windot11. h (inclure Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="965ea-119"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="965ea-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="965ea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="965ea-121">**\_Liste des BSSID DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="965ea-121">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> <dt>

[<span data-ttu-id="965ea-122">**\_attributs d’association WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="965ea-122">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="965ea-123">**entrée réseau local sans fil \_ \_**</span><span class="sxs-lookup"><span data-stu-id="965ea-123">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




