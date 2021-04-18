---
title: Propriété de domaine ITsSbSession
description: Récupère le nom de domaine de l’utilisateur.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété de domaine
- Services Bureau à distance de propriété de domaine, interface ITsSbSession
- Services Bureau à distance de l’interface ITsSbSession, propriété de domaine
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4501413888d17a70610160117df3ad03fde73b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512207"
---
# <a name="itssbsessiondomain-property"></a><span data-ttu-id="d4c2b-106">ITsSbSession ::D propriété omaine</span><span class="sxs-lookup"><span data-stu-id="d4c2b-106">ITsSbSession::Domain property</span></span>

<span data-ttu-id="d4c2b-107">Récupère le nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-107">Retrieves the domain name of the user.</span></span>

<span data-ttu-id="d4c2b-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c2b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4c2b-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a><span data-ttu-id="d4c2b-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d4c2b-110">Property value</span></span>

<span data-ttu-id="d4c2b-111">Pointeur vers une variable **BSTR** qui reçoit le nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-111">A pointer to a **BSTR** variable that receives the domain name of the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c2b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4c2b-112">Requirements</span></span>



| <span data-ttu-id="d4c2b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4c2b-113">Requirement</span></span> | <span data-ttu-id="d4c2b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4c2b-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c2b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4c2b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c2b-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4c2b-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="d4c2b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4c2b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c2b-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4c2b-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="d4c2b-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="d4c2b-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4c2b-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4c2b-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4c2b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4c2b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c2b-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="d4c2b-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





