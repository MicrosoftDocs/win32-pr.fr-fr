---
title: IRDVTaskPlugin Terminate (méthode)
description: Appelé lorsque l’agent de tâche est arrêté.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Terminate, méthode Services Bureau à distance
- Terminate, méthode Services Bureau à distance, IRDVTaskPlugin, interface
- Services Bureau à distance de l’interface IRDVTaskPlugin, méthode Terminate
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384872"
---
# <a name="irdvtaskpluginterminate-method"></a><span data-ttu-id="30dd5-106">IRDVTaskPlugin :: Terminate, méthode</span><span class="sxs-lookup"><span data-stu-id="30dd5-106">IRDVTaskPlugin::Terminate method</span></span>

<span data-ttu-id="30dd5-107">Appelé lorsque l’agent de tâche est arrêté.</span><span class="sxs-lookup"><span data-stu-id="30dd5-107">Called when the task agent is being shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="30dd5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30dd5-108">Syntax</span></span>


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="30dd5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30dd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30dd5-110">*RH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30dd5-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd5-111">Indique si l’arrêt est dû à un arrêt normal ou à un échec.</span><span class="sxs-lookup"><span data-stu-id="30dd5-111">Indicates whether the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="30dd5-112">Si l’arrêt est normal, cela indique que **est \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="30dd5-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="30dd5-113">Sinon, elle contient un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30dd5-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30dd5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30dd5-114">Return value</span></span>

<span data-ttu-id="30dd5-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="30dd5-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30dd5-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30dd5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="30dd5-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30dd5-117">Requirements</span></span>



| <span data-ttu-id="30dd5-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30dd5-118">Requirement</span></span> | <span data-ttu-id="30dd5-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="30dd5-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="30dd5-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30dd5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30dd5-121">Windows 7 Entreprise</span><span class="sxs-lookup"><span data-stu-id="30dd5-121">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="30dd5-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30dd5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30dd5-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30dd5-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30dd5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30dd5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30dd5-125">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="30dd5-125">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





