---
description: Les \_ constantes PHONEINITIALIZEEXOPTION spécifient le mécanisme de notification d’événement à utiliser lors de l’initialisation d’une session.
ms.assetid: 7d8b122d-bebe-4904-abc8-d680b0899e25
title: Constantes PHONEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023f6801f65910bedf7d2637079694b4c6b6d85e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540721"
---
# <a name="phoneinitializeexoption_-constants"></a><span data-ttu-id="c3412-103">\_Constantes PHONEINITIALIZEEXOPTION</span><span class="sxs-lookup"><span data-stu-id="c3412-103">PHONEINITIALIZEEXOPTION\_ Constants</span></span>

<span data-ttu-id="c3412-104">Les constantes **PHONEINITIALIZEEXOPTION \_** spécifient le mécanisme de notification d’événement à utiliser lors de l’initialisation d’une session.</span><span class="sxs-lookup"><span data-stu-id="c3412-104">The **PHONEINITIALIZEEXOPTION\_** constants specify which event notification mechanism to use when initializing a session.</span></span>

<dl> <dt>

<span data-ttu-id="c3412-105"><span id="PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="phoneinitializeexoption_usecompletionport"></span>**PHONEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**</span><span class="sxs-lookup"><span data-stu-id="c3412-105"><span id="PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="phoneinitializeexoption_usecompletionport"></span>**PHONEINITIALIZEEXOPTION\_USECOMPLETIONPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3412-106">L’application souhaite utiliser le mécanisme de notification d’événement du port d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="c3412-106">The application desires to use the Completion Port event notification mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3412-107"><span id="PHONEINITIALIZEEXOPTION_USEEVENT"></span><span id="phoneinitializeexoption_useevent"></span>**PHONEINITIALIZEEXOPTION \_ USEEVENT**</span><span class="sxs-lookup"><span data-stu-id="c3412-107"><span id="PHONEINITIALIZEEXOPTION_USEEVENT"></span><span id="phoneinitializeexoption_useevent"></span>**PHONEINITIALIZEEXOPTION\_USEEVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3412-108">L’application souhaite utiliser le mécanisme de notification d’événement de handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="c3412-108">The application desires to use the Event Handle event notification mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3412-109"><span id="PHONEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="phoneinitializeexoption_usehiddenwindow"></span>**PHONEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**</span><span class="sxs-lookup"><span data-stu-id="c3412-109"><span id="PHONEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="phoneinitializeexoption_usehiddenwindow"></span>**PHONEINITIALIZEEXOPTION\_USEHIDDENWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3412-110">L’application souhaite utiliser le mécanisme de notification d’événements de fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="c3412-110">The application desires to use the Hidden Window event notification mechanism.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3412-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c3412-111">Remarks</span></span>

<span data-ttu-id="c3412-112">Pour plus d’informations sur le fonctionnement de ces options, consultez [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="c3412-112">See [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3412-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3412-113">Requirements</span></span>



| <span data-ttu-id="c3412-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3412-114">Requirement</span></span> | <span data-ttu-id="c3412-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3412-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c3412-116">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="c3412-116">TAPI version</span></span><br/> | <span data-ttu-id="c3412-117">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c3412-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c3412-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3412-118">Header</span></span><br/>       | <dl> <span data-ttu-id="c3412-119"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3412-119"><dt>Tapi.h</dt></span></span> </dl> |



 

 




