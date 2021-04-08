---
title: Propriété d’identificateur ITsSbTaskInfo
description: Récupère un GUID utilisé en tant qu’identificateur unique par l’agent de tâche.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- Propriété d’identificateur Services Bureau à distance
- Propriété d’identificateur Services Bureau à distance, interface ITsSbTaskInfo
- Services Bureau à distance de l’interface ITsSbTaskInfo, propriété de l’identificateur
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 241ed2966e9ec92aa420af20ce142bcb724ad222
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743637"
---
# <a name="itssbtaskinfoidentifier-property"></a><span data-ttu-id="39f19-106">ITsSbTaskInfo :: identifier, propriété</span><span class="sxs-lookup"><span data-stu-id="39f19-106">ITsSbTaskInfo::Identifier property</span></span>

<span data-ttu-id="39f19-107">Récupère un GUID utilisé en tant qu’identificateur unique par l’agent de tâche.</span><span class="sxs-lookup"><span data-stu-id="39f19-107">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

<span data-ttu-id="39f19-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="39f19-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f19-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39f19-109">Syntax</span></span>


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a><span data-ttu-id="39f19-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="39f19-110">Property value</span></span>

<span data-ttu-id="39f19-111">Pointeur vers une valeur **BSTR** qui reçoit le GUID.</span><span class="sxs-lookup"><span data-stu-id="39f19-111">A pointer to a **BSTR** value that receives the GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f19-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39f19-112">Requirements</span></span>



| <span data-ttu-id="39f19-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39f19-113">Requirement</span></span> | <span data-ttu-id="39f19-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="39f19-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39f19-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39f19-115">Minimum supported client</span></span><br/> | <span data-ttu-id="39f19-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="39f19-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="39f19-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39f19-117">Minimum supported server</span></span><br/> | <span data-ttu-id="39f19-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39f19-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="39f19-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="39f19-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39f19-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39f19-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f19-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39f19-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f19-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="39f19-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





