---
description: Définit un type de réseau BSS (Service Set) de base.
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: Énumération DOT11_BSS_TYPE (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSS_TYPE
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 7815e75f3ef7ef8d908b7d2b26f2e5f9d3630009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527539"
---
# <a name="dot11_bss_type-enumeration"></a><span data-ttu-id="5ec22-103">\_ \_ Énumération des types BSS DOT11</span><span class="sxs-lookup"><span data-stu-id="5ec22-103">DOT11\_BSS\_TYPE enumeration</span></span>

<span data-ttu-id="5ec22-104">Le type d’énumération de **\_ \_ type BSS DOT11** définit un type de réseau BSS (Basic Service Set).</span><span class="sxs-lookup"><span data-stu-id="5ec22-104">The **DOT11\_BSS\_TYPE** enumerated type defines a basic service set (BSS) network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec22-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ec22-105">Syntax</span></span>


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="5ec22-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="5ec22-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5ec22-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**\_infrastructure de \_ type \_ BSS dot11**</span><span class="sxs-lookup"><span data-stu-id="5ec22-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**dot11\_BSS\_type\_infrastructure**</span></span>
</dt> <dd>

<span data-ttu-id="5ec22-108">Spécifie un réseau BSS d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="5ec22-108">Specifies an infrastructure BSS network.</span></span>

</dd> <dt>

<span data-ttu-id="5ec22-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**\_type BSS \_ dot11 \_ indépendant**</span><span class="sxs-lookup"><span data-stu-id="5ec22-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**dot11\_BSS\_type\_independent**</span></span>
</dt> <dd>

<span data-ttu-id="5ec22-110">Spécifie un réseau indépendant BSS (IBSS).</span><span class="sxs-lookup"><span data-stu-id="5ec22-110">Specifies an independent BSS (IBSS) network.</span></span>

</dd> <dt>

<span data-ttu-id="5ec22-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**\_types BSS \_ dot11 \_ any**</span><span class="sxs-lookup"><span data-stu-id="5ec22-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11\_BSS\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="5ec22-112">Spécifie l’infrastructure ou le réseau IBSS.</span><span class="sxs-lookup"><span data-stu-id="5ec22-112">Specifies either infrastructure or IBSS network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ec22-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ec22-113">Requirements</span></span>



| <span data-ttu-id="5ec22-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ec22-114">Requirement</span></span> | <span data-ttu-id="5ec22-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ec22-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec22-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ec22-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5ec22-117">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ec22-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5ec22-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ec22-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5ec22-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ec22-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="5ec22-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="5ec22-120">Redistributable</span></span><br/>          | <span data-ttu-id="5ec22-121">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="5ec22-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="5ec22-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ec22-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ec22-123"><dt>Wlantypes. h (inclure Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ec22-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec22-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ec22-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec22-125">**entrée réseau local sans fil \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ec22-125">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[<span data-ttu-id="5ec22-126">**\_paramètres de connexion WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="5ec22-126">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="5ec22-127">**WlanGetNetworkBssList**</span><span class="sxs-lookup"><span data-stu-id="5ec22-127">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




