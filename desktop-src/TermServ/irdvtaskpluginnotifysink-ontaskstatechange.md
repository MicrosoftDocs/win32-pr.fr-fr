---
title: Méthode IRDVTaskPluginNotifySink OnTaskStateChange
description: Permet d’informer l’agent déclencheur que l’état d’une tâche a changé.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnTaskStateChange
- Méthode OnTaskStateChange Services Bureau à distance, interface IRDVTaskPluginNotifySink
- Services Bureau à distance de l’interface IRDVTaskPluginNotifySink, méthode OnTaskStateChange
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510358"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a><span data-ttu-id="42e53-106">IRDVTaskPluginNotifySink :: OnTaskStateChange, méthode</span><span class="sxs-lookup"><span data-stu-id="42e53-106">IRDVTaskPluginNotifySink::OnTaskStateChange method</span></span>

<span data-ttu-id="42e53-107">Permet d’informer l’agent déclencheur que l’état d’une tâche a changé.</span><span class="sxs-lookup"><span data-stu-id="42e53-107">Used to notify the trigger agent that the state of a task has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e53-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42e53-108">Syntax</span></span>


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a><span data-ttu-id="42e53-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42e53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42e53-110">*bstrIdentifier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42e53-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e53-111">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="42e53-111">Type: **BSTR**</span></span>

<span data-ttu-id="42e53-112">Identificateur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="42e53-112">The identifier of the task.</span></span> <span data-ttu-id="42e53-113">Il s’agit de l’identificateur passé à la méthode [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="42e53-113">This is the identifier passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="42e53-114">*État* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42e53-114">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e53-115">Type : état de la **[ **\_ tâche \_ RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span><span class="sxs-lookup"><span data-stu-id="42e53-115">Type: **[**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span></span>

<span data-ttu-id="42e53-116">Valeur de l’énumération de l' [**\_ \_ État de la tâche RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) qui spécifie le nouvel état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="42e53-116">A value of the [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration that specifies the new state of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42e53-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42e53-117">Return value</span></span>

<span data-ttu-id="42e53-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="42e53-118">Type: **HRESULT**</span></span>

<span data-ttu-id="42e53-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="42e53-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42e53-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42e53-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="42e53-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42e53-121">Requirements</span></span>



| <span data-ttu-id="42e53-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42e53-122">Requirement</span></span> | <span data-ttu-id="42e53-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="42e53-123">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="42e53-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42e53-124">Minimum supported client</span></span><br/> | <span data-ttu-id="42e53-125">Windows 7 Entreprise</span><span class="sxs-lookup"><span data-stu-id="42e53-125">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="42e53-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42e53-126">Minimum supported server</span></span><br/> | <span data-ttu-id="42e53-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42e53-127">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42e53-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42e53-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e53-129">**État de la \_ tâche RDV \_**</span><span class="sxs-lookup"><span data-stu-id="42e53-129">**RDV\_TASK\_STATUS**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[<span data-ttu-id="42e53-130">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="42e53-130">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





