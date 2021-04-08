---
title: Propriété d’État ITsSbTaskInfo
description: Récupère une valeur d' \_ \_ énumération de l’état de la tâche RDV qui représente l’état de la tâche.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété Status
- Services Bureau à distance de propriété Status, interface ITsSbTaskInfo
- Services Bureau à distance de l’interface ITsSbTaskInfo, propriété Status
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3206013c32ee6cf3323f19c9e95e89c8d6756eb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741309"
---
# <a name="itssbtaskinfostatus-property"></a><span data-ttu-id="4c5d8-106">ITsSbTaskInfo :: Status, propriété</span><span class="sxs-lookup"><span data-stu-id="4c5d8-106">ITsSbTaskInfo::Status property</span></span>

<span data-ttu-id="4c5d8-107">Récupère une valeur d’énumération de l' [**\_ \_ État de la tâche RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) qui représente l’état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="4c5d8-107">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

<span data-ttu-id="4c5d8-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4c5d8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5d8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c5d8-109">Syntax</span></span>


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a><span data-ttu-id="4c5d8-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4c5d8-110">Property value</span></span>

<span data-ttu-id="4c5d8-111">Valeur d’énumération de l' [**\_ \_ État de la tâche RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) qui représente l’état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="4c5d8-111">An [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c5d8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c5d8-112">Requirements</span></span>



| <span data-ttu-id="4c5d8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c5d8-113">Requirement</span></span> | <span data-ttu-id="4c5d8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c5d8-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5d8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c5d8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4c5d8-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c5d8-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="4c5d8-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c5d8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4c5d8-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4c5d8-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="4c5d8-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="4c5d8-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c5d8-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c5d8-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c5d8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c5d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c5d8-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="4c5d8-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





