---
title: Méthode IMsTscAxEvents OnRemoteProgramDisplayed
description: Appelé lorsqu’un programme RemoteApp est affiché.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRemoteProgramDisplayed
- Méthode OnRemoteProgramDisplayed Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRemoteProgramDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742109"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a><span data-ttu-id="872b8-106">IMsTscAxEvents :: OnRemoteProgramDisplayed, méthode</span><span class="sxs-lookup"><span data-stu-id="872b8-106">IMsTscAxEvents::OnRemoteProgramDisplayed method</span></span>

<span data-ttu-id="872b8-107">Appelé lorsqu’un programme RemoteApp est affiché.</span><span class="sxs-lookup"><span data-stu-id="872b8-107">Called when a RemoteApp program is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="872b8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="872b8-108">Syntax</span></span>


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a><span data-ttu-id="872b8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="872b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="872b8-110">*vbDisplayed* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="872b8-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872b8-111">Indique si le programme RemoteApp est affiché ou masqué.</span><span class="sxs-lookup"><span data-stu-id="872b8-111">Indicates whether the RemoteApp program is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="872b8-112">*uDisplayInformation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="872b8-112">*uDisplayInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872b8-113">Informations d’affichage.</span><span class="sxs-lookup"><span data-stu-id="872b8-113">The display information.</span></span>

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span data-ttu-id="872b8-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAIL \_ APPDISPLAY \_ reconnexion automatique**</span><span class="sxs-lookup"><span data-stu-id="872b8-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAIL\_APPDISPLAY\_AUTORECONNECT**</span></span>


</dt> <dd>

<span data-ttu-id="872b8-115">La reconnexion automatique est en cours.</span><span class="sxs-lookup"><span data-stu-id="872b8-115">Automatic reconnect is in progress.</span></span>

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span data-ttu-id="872b8-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAIL \_ APPDISPLAY \_ DESKTOPHOOKED**</span><span class="sxs-lookup"><span data-stu-id="872b8-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAIL\_APPDISPLAY\_DESKTOPHOOKED**</span></span>


</dt> <dd>

<span data-ttu-id="872b8-117">Le nombre de RemoteApp est passé à zéro.</span><span class="sxs-lookup"><span data-stu-id="872b8-117">The RemoteApp count just went to zero.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="872b8-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="872b8-118">Return value</span></span>

<span data-ttu-id="872b8-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="872b8-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="872b8-120">Notes</span><span class="sxs-lookup"><span data-stu-id="872b8-120">Remarks</span></span>

<span data-ttu-id="872b8-121">Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant qu’un RemoteApp a été affiché.</span><span class="sxs-lookup"><span data-stu-id="872b8-121">Implement this method in your event sink to receive notification that a RemoteApp has been displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="872b8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="872b8-122">Requirements</span></span>



| <span data-ttu-id="872b8-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="872b8-123">Requirement</span></span> | <span data-ttu-id="872b8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="872b8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="872b8-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="872b8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="872b8-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="872b8-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="872b8-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="872b8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="872b8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="872b8-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="872b8-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="872b8-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="872b8-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="872b8-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="872b8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="872b8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="872b8-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="872b8-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="872b8-133">IID</span><span class="sxs-lookup"><span data-stu-id="872b8-133">IID</span></span><br/>                      | <span data-ttu-id="872b8-134">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="872b8-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



 

 





