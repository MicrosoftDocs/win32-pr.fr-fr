---
description: L’interface IMulticastControl est implémentée par le MSP IPConf et disponible uniquement sur les objets d’appel de multidiffusion.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interface IMulticastControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526404"
---
# <a name="imulticastcontrol-interface"></a><span data-ttu-id="7f5f9-103">Interface IMulticastControl</span><span class="sxs-lookup"><span data-stu-id="7f5f9-103">IMulticastControl interface</span></span>

<span data-ttu-id="7f5f9-104">\[**IMulticastControl** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-104">\[**IMulticastControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7f5f9-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="7f5f9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7f5f9-106">L’interface **IMulticastControl** est implémentée par le MSP ipconf et disponible uniquement sur les objets d’appel de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-106">The **IMulticastControl** interface is implemented by the IPConf MSP and available only on multicast call objects.</span></span> <span data-ttu-id="7f5f9-107">Cette interface expose des méthodes qui permettent la création et la manipulation de terminaux qui peuvent communiquer entre des clients H323 et SDP.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="7f5f9-108">L’interface **IMulticastControl** contrôle le mode de bouclage de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-108">The **IMulticastControl** interface controls the multicast loopback mode.</span></span>

<span data-ttu-id="7f5f9-109">En mode de \_ \_ bouclage mm, la multidiffusion est désactivée, ce qui signifie que deux applications sur le même ordinateur qui rejoignent le même groupe de multidiffusion obtiendront les paquets de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-109">In the MM\_NO\_LOOPBACK mode, multicast loopback is disabled, which means two applications on the same machine who join the same multicast group will get each other's packets.</span></span> <span data-ttu-id="7f5f9-110">Ce mode offre les meilleures performances si une seule application est toujours jointe au groupe de multidiffusion sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-110">This mode has the best performance if there is always only one application joining the multicast group on the machine.</span></span> <span data-ttu-id="7f5f9-111">MM \_ aucun \_ mode de bouclage n’est le mode par défaut.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-111">MM\_NO\_LOOPBACK mode is the default mode.</span></span>

<span data-ttu-id="7f5f9-112">Le \_ \_ mode de bouclage complet mm est parfait uniquement pour les tests.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-112">The MM\_FULL\_LOOPBACK mode is good only for testing.</span></span> <span data-ttu-id="7f5f9-113">Tous les paquets envoyés sont également renvoyés en boucle.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="7f5f9-114">Cela peut être utilisé pour tester si les appareils fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-114">This can be used to test if the devices are working.</span></span>

<span data-ttu-id="7f5f9-115">Le \_ mode de \_ bouclage sélectif mm est utilisé pour permettre à plusieurs applications sur un ordinateur de rejoindre le même groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-115">The MM\_SELECTIVE\_LOOPBACK mode is used to enable multiple applications on one machine to join the same multicast group.</span></span> <span data-ttu-id="7f5f9-116">Les paquets sont rebouclés de la pile et chaque session RTP est chargée de filtrer les paquets indésirables.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-116">The packets are looped back from the stack, and each RTP session is responsible for filtering out unwanted packets.</span></span>

## <a name="members"></a><span data-ttu-id="7f5f9-117">Membres</span><span class="sxs-lookup"><span data-stu-id="7f5f9-117">Members</span></span>

<span data-ttu-id="7f5f9-118">L’interface **IMulticastControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7f5f9-118">The **IMulticastControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7f5f9-119">**IMulticastControl** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7f5f9-119">**IMulticastControl** also has these types of members:</span></span>

-   [<span data-ttu-id="7f5f9-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7f5f9-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7f5f9-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7f5f9-121">Methods</span></span>

<span data-ttu-id="7f5f9-122">L’interface **IMulticastControl** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-122">The **IMulticastControl** interface has these methods.</span></span>



| <span data-ttu-id="7f5f9-123">Méthode</span><span class="sxs-lookup"><span data-stu-id="7f5f9-123">Method</span></span>                                                          | <span data-ttu-id="7f5f9-124">Description</span><span class="sxs-lookup"><span data-stu-id="7f5f9-124">Description</span></span>                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="7f5f9-125">**Obtient \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="7f5f9-125">**get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md) | <span data-ttu-id="7f5f9-126">Obtient le mode de bouclage de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-126">Gets the multicast loopback mode.</span></span><br/> |
| [<span data-ttu-id="7f5f9-127">**put \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="7f5f9-127">**put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md) | <span data-ttu-id="7f5f9-128">Définit le mode de bouclage de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="7f5f9-128">Sets the multicast loopback mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7f5f9-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f5f9-129">Requirements</span></span>



| <span data-ttu-id="7f5f9-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f5f9-130">Requirement</span></span> | <span data-ttu-id="7f5f9-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f5f9-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f5f9-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="7f5f9-132">TAPI version</span></span><br/> | <span data-ttu-id="7f5f9-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7f5f9-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7f5f9-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f5f9-134">Header</span></span><br/>       | <dl> <span data-ttu-id="7f5f9-135"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f5f9-135"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="7f5f9-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7f5f9-136">Library</span></span><br/>      | <dl> <span data-ttu-id="7f5f9-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f5f9-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7f5f9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7f5f9-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="7f5f9-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f5f9-139"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7f5f9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f5f9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f5f9-141">MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="7f5f9-141">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

