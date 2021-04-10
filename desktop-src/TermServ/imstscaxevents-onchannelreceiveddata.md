---
title: Méthode IMsTscAxEvents OnChannelReceivedData
description: Appelé lorsque le client reçoit des données sur un canal virtuel scriptable.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnChannelReceivedData
- Méthode OnChannelReceivedData Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnChannelReceivedData
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103524"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a><span data-ttu-id="ea538-106">IMsTscAxEvents :: OnChannelReceivedData, méthode</span><span class="sxs-lookup"><span data-stu-id="ea538-106">IMsTscAxEvents::OnChannelReceivedData method</span></span>

<span data-ttu-id="ea538-107">Appelé lorsque le client reçoit des données sur un canal virtuel scriptable.</span><span class="sxs-lookup"><span data-stu-id="ea538-107">Called when the client receives data on a scriptable virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea538-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea538-108">Syntax</span></span>


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a><span data-ttu-id="ea538-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea538-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea538-110">*chanName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea538-110">*chanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea538-111">Nom du canal virtuel sur lequel les données ont été reçues.</span><span class="sxs-lookup"><span data-stu-id="ea538-111">The name of the virtual channel on which data was received.</span></span> <span data-ttu-id="ea538-112">Ce nom correspond à l’un des canaux créés par l’appel à [**IMsTscAx :: CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span><span class="sxs-lookup"><span data-stu-id="ea538-112">This name matches one of the channels created by the call to [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea538-113">*données* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea538-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea538-114">Données reçues sur le canal virtuel scriptable.</span><span class="sxs-lookup"><span data-stu-id="ea538-114">The data received on the scriptable virtual channel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea538-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea538-115">Return value</span></span>

<span data-ttu-id="ea538-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ea538-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea538-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ea538-117">Remarks</span></span>

<span data-ttu-id="ea538-118">Pour plus d’informations sur cet événement, consultez [implémentation de canaux virtuels scriptables à l’aide de connexion Bureau à distance par le Web](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) .</span><span class="sxs-lookup"><span data-stu-id="ea538-118">Refer to [Implementing Scriptable Virtual Channels using Remote Desktop Web Connection](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) for more information about this event.</span></span>

<span data-ttu-id="ea538-119">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ea538-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea538-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea538-120">Requirements</span></span>



| <span data-ttu-id="ea538-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea538-121">Requirement</span></span> | <span data-ttu-id="ea538-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea538-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea538-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea538-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ea538-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea538-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ea538-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea538-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ea538-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea538-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ea538-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ea538-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea538-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea538-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ea538-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ea538-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea538-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea538-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ea538-131">IID</span><span class="sxs-lookup"><span data-stu-id="ea538-131">IID</span></span><br/>                      | <span data-ttu-id="ea538-132">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="ea538-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ea538-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea538-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea538-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="ea538-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





