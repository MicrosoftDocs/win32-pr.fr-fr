---
title: IRDVTaskPlugin Initialize, méthode
description: Appelé pour initialiser l’agent de tâche.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Initialize, méthode Services Bureau à distance
- Initialize, méthode Services Bureau à distance, IRDVTaskPlugin, interface
- Services Bureau à distance de l’interface IRDVTaskPlugin, méthode Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384156"
---
# <a name="irdvtaskplugininitialize-method"></a><span data-ttu-id="6c058-106">IRDVTaskPlugin :: Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="6c058-106">IRDVTaskPlugin::Initialize method</span></span>

<span data-ttu-id="6c058-107">Appelé pour initialiser l’agent de tâche.</span><span class="sxs-lookup"><span data-stu-id="6c058-107">Called to initialize the task agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c058-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c058-108">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a><span data-ttu-id="6c058-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c058-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c058-110">*pNotifySink* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c058-110">*pNotifySink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c058-111">Tapez : \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) \** _</span><span class="sxs-lookup"><span data-stu-id="6c058-111">Type: \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\** _</span></span>

<span data-ttu-id="6c058-112">Pointeur vers une interface [_ *IRDVTaskPluginNotifySink* \*](irdvtaskpluginnotifysink.md) que l’agent de tâche utilise pour communiquer avec l’agent déclencheur.</span><span class="sxs-lookup"><span data-stu-id="6c058-112">A pointer to an [_ *IRDVTaskPluginNotifySink*\*](irdvtaskpluginnotifysink.md) interface that the task agent uses to communicate with the trigger agent.</span></span> <span data-ttu-id="6c058-113">Vous devez libérer cette interface lorsqu’elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6c058-113">You must release this interface when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c058-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c058-114">Return value</span></span>

<span data-ttu-id="6c058-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6c058-115">Type: **HRESULT**</span></span>

<span data-ttu-id="6c058-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6c058-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c058-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6c058-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c058-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c058-118">Requirements</span></span>



| <span data-ttu-id="6c058-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c058-119">Requirement</span></span> | <span data-ttu-id="6c058-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c058-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="6c058-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c058-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6c058-122">Windows 7 Entreprise</span><span class="sxs-lookup"><span data-stu-id="6c058-122">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="6c058-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c058-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6c058-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c058-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c058-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c058-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c058-126">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="6c058-126">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





