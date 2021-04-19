---
description: Les \_ constantes d’indicateur de bit LINECALLHUBTRACKING décrivent le type de suivi de hub d’appel fourni.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Constantes LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525469"
---
# <a name="linecallhubtracking_-constants"></a><span data-ttu-id="35d9a-103">\_Constantes LINECALLHUBTRACKING</span><span class="sxs-lookup"><span data-stu-id="35d9a-103">LINECALLHUBTRACKING\_ Constants</span></span>

<span data-ttu-id="35d9a-104">Les constantes d’indicateur de bit **LINECALLHUBTRACKING \_** décrivent le type de suivi de hub d’appel fourni.</span><span class="sxs-lookup"><span data-stu-id="35d9a-104">The **LINECALLHUBTRACKING\_** bit-flag constants describe the type of call hub tracking provided.</span></span>

<dl> <dt>

<span data-ttu-id="35d9a-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING \_ ALLCALLS**</span><span class="sxs-lookup"><span data-stu-id="35d9a-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING\_ALLCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35d9a-106">Le suivi des concentrateurs d’appels est fourni au niveau de l’appel.</span><span class="sxs-lookup"><span data-stu-id="35d9a-106">Call hub tracking is provided at the call level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35d9a-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="35d9a-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35d9a-108">Aucun suivi d’appel du Hub n’est fourni.</span><span class="sxs-lookup"><span data-stu-id="35d9a-108">No call hub tracking is provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35d9a-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING \_ PROVIDERLEVEL**</span><span class="sxs-lookup"><span data-stu-id="35d9a-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING\_PROVIDERLEVEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35d9a-110">Les hubs d’appel sont suivis au niveau du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="35d9a-110">Call hubs are tracked at the service provider level.</span></span> <span data-ttu-id="35d9a-111">Les appels par modification des appels ne sont pas signalés.</span><span class="sxs-lookup"><span data-stu-id="35d9a-111">Call by call changes are not reported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35d9a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="35d9a-112">Remarks</span></span>

<span data-ttu-id="35d9a-113">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="35d9a-113">No extensibility.</span></span> <span data-ttu-id="35d9a-114">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="35d9a-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="35d9a-115">Lorsque des modifications se produisent dans cette structure de données, un message [**\_ CALLINFO de ligne**](line-callinfo.md) est envoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="35d9a-115">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="35d9a-116">Les paramètres de ce message sont un descripteur de l’appel et une indication de l’élément d’information qui a changé.</span><span class="sxs-lookup"><span data-stu-id="35d9a-116">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="35d9a-117">La structure de données [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) indique le type de suivi fourni.</span><span class="sxs-lookup"><span data-stu-id="35d9a-117">The [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) data structure indicates which tracking type is provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d9a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35d9a-118">Requirements</span></span>



| <span data-ttu-id="35d9a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35d9a-119">Requirement</span></span> | <span data-ttu-id="35d9a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="35d9a-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="35d9a-121">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="35d9a-121">TAPI version</span></span><br/> | <span data-ttu-id="35d9a-122">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="35d9a-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="35d9a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="35d9a-123">Header</span></span><br/>       | <dl> <span data-ttu-id="35d9a-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="35d9a-124"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d9a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35d9a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d9a-126">**CALLINFO de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="35d9a-126">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="35d9a-127">**LINECALLHUBTRACKINGINFO**</span><span class="sxs-lookup"><span data-stu-id="35d9a-127">**LINECALLHUBTRACKINGINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[<span data-ttu-id="35d9a-128">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="35d9a-128">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




