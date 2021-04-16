---
title: Méthode IRemoteDesktopClientEvents OnNetworkStatusChanged
description: Appelé lorsque l’état du réseau a changé. | Méthode IRemoteDesktopClientEvents OnNetworkStatusChanged
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnNetworkStatusChanged
- Méthode OnNetworkStatusChanged Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de64d8b16ea9acf9defc976d4baa91afd64f8fa7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530663"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a><span data-ttu-id="d5ec8-107">IRemoteDesktopClientEvents :: OnNetworkStatusChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="d5ec8-107">IRemoteDesktopClientEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="d5ec8-108">Appelé lorsque l’état du réseau a changé.</span><span class="sxs-lookup"><span data-stu-id="d5ec8-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ec8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5ec8-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a><span data-ttu-id="d5ec8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5ec8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ec8-111">*qualityLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5ec8-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ec8-112">Nouveau niveau de qualité de la connexion.</span><span class="sxs-lookup"><span data-stu-id="d5ec8-112">The new quality level of the connection.</span></span> <span data-ttu-id="d5ec8-113">Le niveau de qualité est déterminé à partir de la bande passante et des valeurs de temps d’aller-retour (RTT).</span><span class="sxs-lookup"><span data-stu-id="d5ec8-113">The quality level is determined from the bandwidth and round-trip time (rtt) values.</span></span>

<span data-ttu-id="d5ec8-114">Une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d5ec8-114">One of the following values.</span></span>



| <span data-ttu-id="d5ec8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5ec8-115">Value</span></span>                                                                        | <span data-ttu-id="d5ec8-116">Signification</span><span class="sxs-lookup"><span data-stu-id="d5ec8-116">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="d5ec8-117"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d5ec8-117"><dt>0</dt></span></span> </dl> | <span data-ttu-id="d5ec8-118">Impossible de déterminer le niveau de qualité.</span><span class="sxs-lookup"><span data-stu-id="d5ec8-118">The quality level could not be determined.</span></span><br/>       |
| <dl> <span data-ttu-id="d5ec8-119"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d5ec8-119"><dt>1</dt></span></span> </dl> | <span data-ttu-id="d5ec8-120">La qualité de la connexion est médiocre (une barre).</span><span class="sxs-lookup"><span data-stu-id="d5ec8-120">The connection quality is poor (one bar).</span></span><br/>        |
| <dl> <span data-ttu-id="d5ec8-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d5ec8-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d5ec8-122">La qualité de la connexion est équitable (deux barres).</span><span class="sxs-lookup"><span data-stu-id="d5ec8-122">The connection quality is fair (two bars).</span></span><br/>       |
| <dl> <span data-ttu-id="d5ec8-123"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d5ec8-123"><dt>3</dt></span></span> </dl> | <span data-ttu-id="d5ec8-124">La qualité de la connexion est bonne (trois barres).</span><span class="sxs-lookup"><span data-stu-id="d5ec8-124">The connection quality is good (three bars).</span></span><br/>     |
| <dl> <span data-ttu-id="d5ec8-125"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d5ec8-125"><dt>4</dt></span></span> </dl> | <span data-ttu-id="d5ec8-126">La qualité de la connexion est excellente (quatre barres).</span><span class="sxs-lookup"><span data-stu-id="d5ec8-126">The connection quality is excellent (four bars).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d5ec8-127">*bande passante* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5ec8-127">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ec8-128">Spécifie la nouvelle bande passante de connexion, en kilobits par seconde (Kbits/s).</span><span class="sxs-lookup"><span data-stu-id="d5ec8-128">Specifies the new connection bandwidth, in kilobits per second (Kbps).</span></span>

</dd> <dt>

<span data-ttu-id="d5ec8-129">*RTT* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5ec8-129">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ec8-130">Spécifie la nouvelle durée de bouclage de la connexion (latence), en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="d5ec8-130">Specifies the new connection roundtrip time (latency), in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ec8-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5ec8-131">Return value</span></span>

<span data-ttu-id="d5ec8-132">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d5ec8-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ec8-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5ec8-133">Requirements</span></span>



| <span data-ttu-id="d5ec8-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5ec8-134">Requirement</span></span> | <span data-ttu-id="d5ec8-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5ec8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ec8-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5ec8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d5ec8-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5ec8-137">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="d5ec8-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5ec8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d5ec8-139">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5ec8-139">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="d5ec8-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d5ec8-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="d5ec8-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5ec8-141"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="d5ec8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d5ec8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5ec8-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5ec8-143"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="d5ec8-144">IID</span><span class="sxs-lookup"><span data-stu-id="d5ec8-144">IID</span></span><br/>                      | <span data-ttu-id="d5ec8-145">DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="d5ec8-145">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5ec8-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5ec8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ec8-147">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="d5ec8-147">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





