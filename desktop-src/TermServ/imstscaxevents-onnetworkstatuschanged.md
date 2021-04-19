---
title: Méthode IMsTscAxEvents OnNetworkStatusChanged
description: Appelé lorsque l’état du réseau a changé. | Méthode IMsTscAxEvents OnNetworkStatusChanged
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnNetworkStatusChanged
- Méthode OnNetworkStatusChanged Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535760"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a><span data-ttu-id="0ed55-107">IMsTscAxEvents :: OnNetworkStatusChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="0ed55-107">IMsTscAxEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="0ed55-108">Appelé lorsque l’état du réseau a changé.</span><span class="sxs-lookup"><span data-stu-id="0ed55-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed55-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ed55-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a><span data-ttu-id="0ed55-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ed55-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ed55-111">*qualityLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ed55-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed55-112">Spécifie la nouvelle vitesse de connexion.</span><span class="sxs-lookup"><span data-stu-id="0ed55-112">Specifies the new connection speed.</span></span> <span data-ttu-id="0ed55-113">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ed55-113">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="0ed55-114">1</span><span class="sxs-lookup"><span data-stu-id="0ed55-114">1</span></span>
</dt> <dd>

<span data-ttu-id="0ed55-115">Moins de 512 kilo-octets par seconde (Kbits/s).</span><span class="sxs-lookup"><span data-stu-id="0ed55-115">Less than 512 kilobytes per second (KBps).</span></span>

</dd> <dt>

<span data-ttu-id="0ed55-116">2</span><span class="sxs-lookup"><span data-stu-id="0ed55-116">2</span></span>
</dt> <dd>

<span data-ttu-id="0ed55-117">de 512 à 1 999 KBps.</span><span class="sxs-lookup"><span data-stu-id="0ed55-117">512 to 1,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="0ed55-118">3</span><span class="sxs-lookup"><span data-stu-id="0ed55-118">3</span></span>
</dt> <dd>

<span data-ttu-id="0ed55-119">de 2 000 à 9 999 KBps.</span><span class="sxs-lookup"><span data-stu-id="0ed55-119">2,000 to 9,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="0ed55-120">4</span><span class="sxs-lookup"><span data-stu-id="0ed55-120">4</span></span>
</dt> <dd>

<span data-ttu-id="0ed55-121">Supérieur ou égal à 10 000 Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="0ed55-121">Greater than or equal to 10,000 KBps.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0ed55-122">*bande passante* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ed55-122">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed55-123">Spécifie la bande passante de la connexion.</span><span class="sxs-lookup"><span data-stu-id="0ed55-123">Specifies the connection bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="0ed55-124">*RTT* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ed55-124">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed55-125">Spécifie la latence de la connexion.</span><span class="sxs-lookup"><span data-stu-id="0ed55-125">Specifies the connection latency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ed55-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ed55-126">Return value</span></span>

<span data-ttu-id="0ed55-127">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0ed55-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ed55-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ed55-128">Requirements</span></span>



| <span data-ttu-id="0ed55-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ed55-129">Requirement</span></span> | <span data-ttu-id="0ed55-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ed55-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed55-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ed55-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0ed55-132">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0ed55-132">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="0ed55-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ed55-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0ed55-134">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0ed55-134">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="0ed55-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0ed55-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="0ed55-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ed55-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0ed55-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0ed55-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ed55-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ed55-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0ed55-139">IID</span><span class="sxs-lookup"><span data-stu-id="0ed55-139">IID</span></span><br/>                      | <span data-ttu-id="0ed55-140">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="0ed55-140">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="0ed55-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ed55-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed55-142">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="0ed55-142">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





