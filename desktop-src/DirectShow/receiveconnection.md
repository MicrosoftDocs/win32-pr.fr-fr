---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109282"
---
# <a name="receiveconnection"></a><span data-ttu-id="02de5-103">ReceiveConnection</span><span class="sxs-lookup"><span data-stu-id="02de5-103">ReceiveConnection</span></span>

<span data-ttu-id="02de5-104">Ce mécanisme permet à une broche de sortie de proposer une modification de format à son homologue en aval, lorsque le nouveau format requiert une mémoire tampon plus grande.</span><span class="sxs-lookup"><span data-stu-id="02de5-104">This mechanism enables an output pin to propose a format change to its downstream peer, when the new format requires a larger buffer.</span></span> <span data-ttu-id="02de5-105">La broche de sortie effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="02de5-105">The output pin does the following:</span></span>

1.  <span data-ttu-id="02de5-106">Appelle [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sur la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="02de5-106">Calls [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the downstream input pin.</span></span>
2.  <span data-ttu-id="02de5-107">Si `ReceiveConnection` elle est réussie, appelle [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="02de5-107">If `ReceiveConnection` succeeds, calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) on the input pin.</span></span>

<span data-ttu-id="02de5-108">En outre, la broche de sortie devra peut-être appeler [**IMemAllocator :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) , puis dévalider et revalider l’allocateur afin de modifier les tailles de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="02de5-108">In addition, the output pin may need to call [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) and then decommit and recommit the allocator in order to change buffer sizes.</span></span> <span data-ttu-id="02de5-109">Veillez à remettre tous les échantillons en attente dans l’ancien format avant de modifier la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="02de5-109">Make sure to deliver all pending samples in the old format before changing the buffer size.</span></span>

<span data-ttu-id="02de5-110">Certains décodeurs MPEG-2 utilisent ce mécanisme pour basculer entre la sortie MPEG-1 et MPEG-2, ou si la taille de la vidéo change.</span><span class="sxs-lookup"><span data-stu-id="02de5-110">Some MPEG-2 decoders use this mechanism to switch between MPEG-1 and MPEG-2 output or if the video size changes.</span></span>

 

 



