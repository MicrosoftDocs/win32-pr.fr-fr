---
title: Méthode IRDVTaskPluginNotifySink DeleteSchedule
description: Appelé par l’agent de tâche pour supprimer une tâche planifiée.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeleteSchedule
- Méthode DeleteSchedule Services Bureau à distance, interface IRDVTaskPluginNotifySink
- Services Bureau à distance de l’interface IRDVTaskPluginNotifySink, méthode DeleteSchedule
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f00bcc740f87acb7f051decd5f2fc9b55ffbf642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106168"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a><span data-ttu-id="063b7-106">IRDVTaskPluginNotifySink ::D méthode eleteSchedule</span><span class="sxs-lookup"><span data-stu-id="063b7-106">IRDVTaskPluginNotifySink::DeleteSchedule method</span></span>

<span data-ttu-id="063b7-107">Appelé par l’agent de tâche pour supprimer une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="063b7-107">Called by the task agent to delete a scheduled task.</span></span>

## <a name="syntax"></a><span data-ttu-id="063b7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="063b7-108">Syntax</span></span>


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a><span data-ttu-id="063b7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="063b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="063b7-110">*bstrIdentifier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="063b7-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="063b7-111">Identificateur de la tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="063b7-111">The identifier of the scheduled task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="063b7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="063b7-112">Return value</span></span>

<span data-ttu-id="063b7-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="063b7-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="063b7-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="063b7-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="063b7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="063b7-115">Requirements</span></span>



| <span data-ttu-id="063b7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="063b7-116">Requirement</span></span> | <span data-ttu-id="063b7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="063b7-117">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="063b7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="063b7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="063b7-119">Windows 7 Entreprise</span><span class="sxs-lookup"><span data-stu-id="063b7-119">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="063b7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="063b7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="063b7-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="063b7-121">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="063b7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="063b7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="063b7-123">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="063b7-123">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





