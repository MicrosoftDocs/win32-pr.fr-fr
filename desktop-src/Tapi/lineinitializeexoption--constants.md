---
description: Les \_ constantes LINEINITIALIZEEXOPTION spécifient le mécanisme de notification d’événement à utiliser lors de l’initialisation d’une session.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: Constantes LINEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544034"
---
# <a name="lineinitializeexoption_-constants"></a><span data-ttu-id="f8e1a-103">\_Constantes LINEINITIALIZEEXOPTION</span><span class="sxs-lookup"><span data-stu-id="f8e1a-103">LINEINITIALIZEEXOPTION\_ Constants</span></span>

<span data-ttu-id="f8e1a-104">Les constantes **LINEINITIALIZEEXOPTION \_** spécifient le mécanisme de notification d’événement à utiliser lors de l’initialisation d’une session.</span><span class="sxs-lookup"><span data-stu-id="f8e1a-104">The **LINEINITIALIZEEXOPTION\_** constants specify which event notification mechanism to use when initializing a session.</span></span>

<dl> <dt>

<span data-ttu-id="f8e1a-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**</span><span class="sxs-lookup"><span data-stu-id="f8e1a-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e1a-106">L’application souhaite utiliser le mécanisme de notification d’événement de suivi de hub d’appel.</span><span class="sxs-lookup"><span data-stu-id="f8e1a-106">The application desires to use the call hub tracking event notification mechanism.</span></span> <span data-ttu-id="f8e1a-107">Cette constante est exposée uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f8e1a-107">This constant is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e1a-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**</span><span class="sxs-lookup"><span data-stu-id="f8e1a-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION\_USECOMPLETIONPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e1a-109">L’application souhaite utiliser le mécanisme de notification d’événement du port d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="f8e1a-109">The application desires to use the Completion Port event notification mechanism.</span></span> <span data-ttu-id="f8e1a-110">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f8e1a-110">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e1a-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**</span><span class="sxs-lookup"><span data-stu-id="f8e1a-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION\_USEEVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e1a-112">L’application souhaite utiliser le mécanisme de notification d’événement de handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="f8e1a-112">The application desires to use the Event Handle event notification mechanism.</span></span> <span data-ttu-id="f8e1a-113">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f8e1a-113">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8e1a-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**</span><span class="sxs-lookup"><span data-stu-id="f8e1a-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION\_USEHIDDENWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8e1a-115">L’application souhaite utiliser le mécanisme de notification d’événements de fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="f8e1a-115">The application desires to use the Hidden Window event notification mechanism.</span></span> <span data-ttu-id="f8e1a-116">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f8e1a-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8e1a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f8e1a-117">Remarks</span></span>

<span data-ttu-id="f8e1a-118">Pour plus d’informations sur le fonctionnement de ces options, consultez [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="f8e1a-118">See [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e1a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8e1a-119">Requirements</span></span>



| <span data-ttu-id="f8e1a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8e1a-120">Requirement</span></span> | <span data-ttu-id="f8e1a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8e1a-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f8e1a-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f8e1a-122">TAPI version</span></span><br/> | <span data-ttu-id="f8e1a-123">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f8e1a-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f8e1a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8e1a-124">Header</span></span><br/>       | <dl> <span data-ttu-id="f8e1a-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8e1a-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




