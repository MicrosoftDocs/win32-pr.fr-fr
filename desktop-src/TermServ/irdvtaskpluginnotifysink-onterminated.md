---
title: Méthode IRDVTaskPluginNotifySink OnTerminated (Sbtsv. h)
description: Appelée par l’agent de tâche pour demander que l’agent de tâche soit arrêté.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnTerminated
- Méthode OnTerminated Services Bureau à distance, interface IRDVTaskPluginNotifySink
- Services Bureau à distance de l’interface IRDVTaskPluginNotifySink, méthode OnTerminated
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509346"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a><span data-ttu-id="9ae2c-106">IRDVTaskPluginNotifySink :: OnTerminated, méthode</span><span class="sxs-lookup"><span data-stu-id="9ae2c-106">IRDVTaskPluginNotifySink::OnTerminated method</span></span>

<span data-ttu-id="9ae2c-107">Appelée par l’agent de tâche pour demander que l’agent de tâche soit arrêté.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-107">Called by the task agent to request that the task agent be shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae2c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ae2c-108">Syntax</span></span>


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="9ae2c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ae2c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ae2c-110">*RH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ae2c-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ae2c-111">Indique si l’arrêt est dû à un arrêt normal ou à un échec.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-111">Indicates if the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="9ae2c-112">Si l’arrêt est normal, cela indique que **est \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="9ae2c-113">Sinon, elle contient un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ae2c-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ae2c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ae2c-114">Return value</span></span>

<span data-ttu-id="9ae2c-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9ae2c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ae2c-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ae2c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae2c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ae2c-117">Requirements</span></span>



| <span data-ttu-id="9ae2c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ae2c-118">Requirement</span></span> | <span data-ttu-id="9ae2c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ae2c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae2c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ae2c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae2c-121">Windows 7 Entreprise</span><span class="sxs-lookup"><span data-stu-id="9ae2c-121">Windows 7 Enterprise</span></span><br/>                                                    |
| <span data-ttu-id="9ae2c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ae2c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae2c-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ae2c-123">Windows Server 2008 R2</span></span><br/>                                                  |
| <span data-ttu-id="9ae2c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ae2c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ae2c-125"><dt>Sbtsv. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ae2c-125"><dt>Sbtsv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae2c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ae2c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae2c-127">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="9ae2c-127">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





