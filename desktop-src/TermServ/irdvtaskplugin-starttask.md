---
title: Méthode IRDVTaskPlugin StartTask
description: Appelé pour démarrer la tâche de mise à jour sur la machine virtuelle.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode StartTask
- Méthode StartTask Services Bureau à distance, interface IRDVTaskPlugin
- Services Bureau à distance de l’interface IRDVTaskPlugin, méthode StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465782"
---
# <a name="irdvtaskpluginstarttask-method"></a><span data-ttu-id="156bc-106">IRDVTaskPlugin :: StartTask, méthode</span><span class="sxs-lookup"><span data-stu-id="156bc-106">IRDVTaskPlugin::StartTask method</span></span>

<span data-ttu-id="156bc-107">Appelé pour démarrer la tâche de mise à jour sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="156bc-107">Called to start the update task on the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="156bc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="156bc-108">Syntax</span></span>


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a><span data-ttu-id="156bc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="156bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="156bc-110">*Étiquette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="156bc-110">*Label* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="156bc-111">Étiquette de la tâche.</span><span class="sxs-lookup"><span data-stu-id="156bc-111">The label for the task.</span></span> <span data-ttu-id="156bc-112">Il s’agit de l’étiquette qui a été transmise à l’agent déclencheur dans la méthode [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="156bc-112">This is the label that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="156bc-113">*Identificateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="156bc-113">*Identifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="156bc-114">Identificateur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="156bc-114">The identifier of the task.</span></span> <span data-ttu-id="156bc-115">Il s’agit de l’identificateur qui a été passé à l’agent déclencheur dans la méthode [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="156bc-115">This is the identifier that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="156bc-116">*Contexte* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="156bc-116">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="156bc-117">Données facultatives pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="156bc-117">Optional data for the task.</span></span> <span data-ttu-id="156bc-118">Il s’agit des données qui ont été passées à l’agent déclencheur dans la méthode [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="156bc-118">This is the data that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="156bc-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="156bc-119">Return value</span></span>

<span data-ttu-id="156bc-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="156bc-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="156bc-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="156bc-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="156bc-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="156bc-122">Requirements</span></span>



| <span data-ttu-id="156bc-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="156bc-123">Requirement</span></span> | <span data-ttu-id="156bc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="156bc-124">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="156bc-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="156bc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="156bc-126">Windows 7 Entreprise</span><span class="sxs-lookup"><span data-stu-id="156bc-126">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="156bc-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="156bc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="156bc-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="156bc-128">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="156bc-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="156bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="156bc-130">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="156bc-130">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





