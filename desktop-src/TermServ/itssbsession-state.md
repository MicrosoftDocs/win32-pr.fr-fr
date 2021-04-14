---
title: Propriété d’État ITsSbSession
description: Récupère ou spécifie l’état de session.
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété d’État
- Propriété State Services Bureau à distance, interface ITsSbSession
- Services Bureau à distance de l’interface ITsSbSession, propriété d’État
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb939a518ab1050d932349cd70c85bcd22edf3d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466898"
---
# <a name="itssbsessionstate-property"></a><span data-ttu-id="7cd58-106">ITsSbSession :: State, propriété</span><span class="sxs-lookup"><span data-stu-id="7cd58-106">ITsSbSession::State property</span></span>

<span data-ttu-id="7cd58-107">Récupère ou spécifie l’état de session.</span><span class="sxs-lookup"><span data-stu-id="7cd58-107">Retrieves or specifies the session state.</span></span>

<span data-ttu-id="7cd58-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7cd58-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd58-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cd58-109">Syntax</span></span>


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a><span data-ttu-id="7cd58-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7cd58-110">Property value</span></span>

<span data-ttu-id="7cd58-111">Valeur de l’énumération d' [**\_ État TSSESSION**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) qui indique l’état d’une session.</span><span class="sxs-lookup"><span data-stu-id="7cd58-111">A value of the [**TSSESSION\_STATE**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) enumeration that indicates the state of a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd58-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cd58-112">Requirements</span></span>



| <span data-ttu-id="7cd58-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cd58-113">Requirement</span></span> | <span data-ttu-id="7cd58-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cd58-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd58-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd58-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd58-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd58-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="7cd58-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd58-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd58-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7cd58-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="7cd58-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="7cd58-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7cd58-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7cd58-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cd58-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cd58-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd58-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="7cd58-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[<span data-ttu-id="7cd58-123">**État de TSSESSION \_**</span><span class="sxs-lookup"><span data-stu-id="7cd58-123">**TSSESSION\_STATE**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





