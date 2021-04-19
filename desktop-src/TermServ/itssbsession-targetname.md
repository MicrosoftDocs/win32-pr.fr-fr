---
title: Propriété TargetName de ITsSbSession
description: Récupère le nom de la cible sur laquelle cette session a été créée.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Propriété TargetName Services Bureau à distance
- TargetName, propriété Services Bureau à distance, ITsSbSession, interface
- Services Bureau à distance de l’interface ITsSbSession, propriété TargetName
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc703a32faedd250115da0b95215e620a8c15e19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510362"
---
# <a name="itssbsessiontargetname-property"></a><span data-ttu-id="f3388-106">ITsSbSession :: TargetName, propriété</span><span class="sxs-lookup"><span data-stu-id="f3388-106">ITsSbSession::TargetName property</span></span>

<span data-ttu-id="f3388-107">Récupère le nom de la cible sur laquelle cette session a été créée.</span><span class="sxs-lookup"><span data-stu-id="f3388-107">Retrieves the name of the target on which this session was created.</span></span>

<span data-ttu-id="f3388-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f3388-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3388-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3388-109">Syntax</span></span>


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a><span data-ttu-id="f3388-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f3388-110">Property value</span></span>

<span data-ttu-id="f3388-111">Pointeur vers une variable **BSTR** qui reçoit le nom de la cible sur laquelle cette session a été créée.</span><span class="sxs-lookup"><span data-stu-id="f3388-111">A pointer to a **BSTR** variable that receives the name of the target on which this session was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3388-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3388-112">Requirements</span></span>



| <span data-ttu-id="f3388-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3388-113">Requirement</span></span> | <span data-ttu-id="f3388-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3388-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3388-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3388-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f3388-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3388-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="f3388-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3388-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f3388-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3388-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="f3388-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="f3388-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3388-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3388-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3388-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3388-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3388-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="f3388-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





