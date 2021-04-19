---
description: L’énumération du mode de bouclage de multidiffusion \_ \_ décrit le mode de bouclage de multidiffusion.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: Énumération MULTICAST_LOOPBACK_MODE (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531157"
---
# <a name="multicast_loopback_mode-enumeration"></a><span data-ttu-id="2220b-103">\_Énumération du mode de bouclage multicast \_</span><span class="sxs-lookup"><span data-stu-id="2220b-103">MULTICAST\_LOOPBACK\_MODE enumeration</span></span>

<span data-ttu-id="2220b-104">\[**Multidiffusion \_ Le \_ mode de bouclage** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2220b-104">\[**MULTICAST\_LOOPBACK\_MODE** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2220b-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="2220b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2220b-106">L’énumération du **\_ \_ mode de bouclage de multidiffusion** décrit le mode de bouclage de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="2220b-106">The **MULTICAST\_LOOPBACK\_MODE** enum describes the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="2220b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2220b-107">Syntax</span></span>


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a><span data-ttu-id="2220b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="2220b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2220b-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ pas de \_ bouclage**</span><span class="sxs-lookup"><span data-stu-id="2220b-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM\_NO\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="2220b-110">Le bouclage de multidiffusion est désactivé.</span><span class="sxs-lookup"><span data-stu-id="2220b-110">Multicast loopback is disabled.</span></span> <span data-ttu-id="2220b-111">Cela signifie que deux applications sur le même ordinateur qui rejoignent le même groupe de multidiffusion peuvent se procurer les paquets de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="2220b-111">That means two applications on the same machine joining the same multicast group can get each other's packets.</span></span>

</dd> <dt>

<span data-ttu-id="2220b-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM \_ de \_ boucle complète**</span><span class="sxs-lookup"><span data-stu-id="2220b-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM\_FULL\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="2220b-113">Tous les paquets envoyés sont également renvoyés en boucle.</span><span class="sxs-lookup"><span data-stu-id="2220b-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="2220b-114">Ce mode est utile uniquement pour les tests.</span><span class="sxs-lookup"><span data-stu-id="2220b-114">This mode is useful only for testing.</span></span>

</dd> <dt>

<span data-ttu-id="2220b-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**\_boucle mm sélective \_**</span><span class="sxs-lookup"><span data-stu-id="2220b-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**MM\_SELECTIVE\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="2220b-116">Le bouclage sélectif est activé.</span><span class="sxs-lookup"><span data-stu-id="2220b-116">Selective loopback is enabled.</span></span> <span data-ttu-id="2220b-117">Cela signifie que l’activation de plusieurs applications sur un même ordinateur peut joindre le même groupe de multidiffusion sans confusion.</span><span class="sxs-lookup"><span data-stu-id="2220b-117">That means enabled multiple applications on one machine can join the same multicast group without confusion.</span></span> <span data-ttu-id="2220b-118">Les paquets sont rebouclés de la pile et chaque session RTP est chargée de filtrer les paquets indésirables.</span><span class="sxs-lookup"><span data-stu-id="2220b-118">The packets are looped back from the stack and each RTP session is responsible for filtering out unwanted packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2220b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2220b-119">Requirements</span></span>



| <span data-ttu-id="2220b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2220b-120">Requirement</span></span> | <span data-ttu-id="2220b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2220b-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2220b-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2220b-122">TAPI version</span></span><br/> | <span data-ttu-id="2220b-123">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2220b-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2220b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2220b-124">Header</span></span><br/>       | <dl> <span data-ttu-id="2220b-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="2220b-125"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2220b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2220b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2220b-127">**IMulticastControl :: obtient \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="2220b-127">**IMulticastControl::get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[<span data-ttu-id="2220b-128">**IMulticastControl ::p ut \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="2220b-128">**IMulticastControl::put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




