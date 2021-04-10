---
title: Propriété de contexte ITsSbTaskInfo
description: Récupère les octets de contexte associés à la tâche.
ms.assetid: ce55ce2a-957f-4b50-b632-42079277102b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété de contexte
- Services Bureau à distance de propriété de contexte, interface ITsSbTaskInfo
- Services Bureau à distance de l’interface ITsSbTaskInfo, propriété de contexte
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Context
- ITsSbTaskInfo.get_Context
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2adc4715f23b2c23ac6dfbdcdd8a489b2b0f5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106084"
---
# <a name="itssbtaskinfocontext-property"></a><span data-ttu-id="e1e92-106">ITsSbTaskInfo :: Context, propriété</span><span class="sxs-lookup"><span data-stu-id="e1e92-106">ITsSbTaskInfo::Context property</span></span>

<span data-ttu-id="e1e92-107">Récupère les octets de contexte associés à la tâche.</span><span class="sxs-lookup"><span data-stu-id="e1e92-107">Retrieves the context bytes associated with the task.</span></span>

<span data-ttu-id="e1e92-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e1e92-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1e92-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1e92-109">Syntax</span></span>


```C++
HRESULT get_Context(
  [out, retval] SAFEARRAY(BYTE) *pContext
);
```



## <a name="property-value"></a><span data-ttu-id="e1e92-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e1e92-110">Property value</span></span>

<span data-ttu-id="e1e92-111">Contexte de la tâche.</span><span class="sxs-lookup"><span data-stu-id="e1e92-111">The context of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1e92-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1e92-112">Requirements</span></span>



| <span data-ttu-id="e1e92-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1e92-113">Requirement</span></span> | <span data-ttu-id="e1e92-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1e92-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e92-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e92-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e1e92-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e92-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e1e92-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e92-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e1e92-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e1e92-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="e1e92-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="e1e92-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1e92-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1e92-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1e92-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1e92-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1e92-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="e1e92-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





