---
title: Propriété du nom d’utilisateur ITsSbSession
description: Récupère le nom d’utilisateur pour cette session.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Propriété UserName Services Bureau à distance
- Propriété UserName Services Bureau à distance, interface ITsSbSession
- Services Bureau à distance de l’interface ITsSbSession, propriété UserName
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510361"
---
# <a name="itssbsessionusername-property"></a><span data-ttu-id="10a05-106">ITsSbSession :: username, propriété</span><span class="sxs-lookup"><span data-stu-id="10a05-106">ITsSbSession::Username property</span></span>

<span data-ttu-id="10a05-107">Récupère le nom d’utilisateur pour cette session.</span><span class="sxs-lookup"><span data-stu-id="10a05-107">Retrieves the user name for this session.</span></span>

<span data-ttu-id="10a05-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="10a05-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a05-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10a05-109">Syntax</span></span>


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a><span data-ttu-id="10a05-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="10a05-110">Property value</span></span>

<span data-ttu-id="10a05-111">Pointeur vers une variable **BSTR** qui reçoit le nom d’utilisateur pour cette session.</span><span class="sxs-lookup"><span data-stu-id="10a05-111">A pointer to a **BSTR** variable that receives the user name for this session.</span></span>

## <a name="requirements"></a><span data-ttu-id="10a05-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10a05-112">Requirements</span></span>



| <span data-ttu-id="10a05-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10a05-113">Requirement</span></span> | <span data-ttu-id="10a05-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="10a05-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10a05-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10a05-115">Minimum supported client</span></span><br/> | <span data-ttu-id="10a05-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="10a05-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="10a05-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10a05-117">Minimum supported server</span></span><br/> | <span data-ttu-id="10a05-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10a05-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="10a05-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="10a05-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10a05-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10a05-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10a05-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10a05-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a05-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="10a05-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





