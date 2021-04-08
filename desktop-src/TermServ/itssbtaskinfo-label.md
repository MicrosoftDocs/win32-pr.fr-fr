---
title: Propriété d’étiquette ITsSbTaskInfo
description: Récupère l’étiquette qui décrit l’objectif de la tâche.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Propriété étiquette Services Bureau à distance
- Label, propriété Services Bureau à distance, ITsSbTaskInfo, interface
- Services Bureau à distance de l’interface ITsSbTaskInfo, propriété label
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f85aaea366cf002d4ec1bacce8f29a6aa67fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743508"
---
# <a name="itssbtaskinfolabel-property"></a><span data-ttu-id="9d3b3-106">ITsSbTaskInfo :: label, propriété</span><span class="sxs-lookup"><span data-stu-id="9d3b3-106">ITsSbTaskInfo::Label property</span></span>

<span data-ttu-id="9d3b3-107">Récupère l’étiquette qui décrit l’objectif de la tâche.</span><span class="sxs-lookup"><span data-stu-id="9d3b3-107">Retrieves the label that describes the purpose of the task.</span></span>

<span data-ttu-id="9d3b3-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9d3b3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3b3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d3b3-109">Syntax</span></span>


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a><span data-ttu-id="9d3b3-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9d3b3-110">Property value</span></span>

<span data-ttu-id="9d3b3-111">Pointeur vers une valeur **BSTR** qui contient l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="9d3b3-111">A pointer to a **BSTR** value that contains the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d3b3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d3b3-112">Requirements</span></span>



| <span data-ttu-id="9d3b3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d3b3-113">Requirement</span></span> | <span data-ttu-id="9d3b3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d3b3-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9d3b3-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d3b3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9d3b3-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d3b3-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="9d3b3-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d3b3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9d3b3-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d3b3-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="9d3b3-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="9d3b3-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9d3b3-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d3b3-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d3b3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d3b3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d3b3-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="9d3b3-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





