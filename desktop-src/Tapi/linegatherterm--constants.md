---
description: Les \_ constantes d’indicateur de bit LINEGATHERTERM décrivent les conditions dans lesquelles la collecte de chiffres mis en mémoire tampon est terminée.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Constantes LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541540"
---
# <a name="linegatherterm_-constants"></a><span data-ttu-id="572eb-103">\_Constantes LINEGATHERTERM</span><span class="sxs-lookup"><span data-stu-id="572eb-103">LINEGATHERTERM\_ Constants</span></span>

<span data-ttu-id="572eb-104">Les constantes d’indicateur de bit **LINEGATHERTERM \_** décrivent les conditions dans lesquelles la collecte de chiffres mis en mémoire tampon est terminée.</span><span class="sxs-lookup"><span data-stu-id="572eb-104">The **LINEGATHERTERM\_** bit-flag constants describe the conditions under which buffered digit gathering is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="572eb-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**</span><span class="sxs-lookup"><span data-stu-id="572eb-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM\_BUFFERFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="572eb-106">Le nombre de chiffres demandé a été collecté.</span><span class="sxs-lookup"><span data-stu-id="572eb-106">The requested number of digits has been gathered.</span></span> <span data-ttu-id="572eb-107">La mémoire tampon est saturée.</span><span class="sxs-lookup"><span data-stu-id="572eb-107">The buffer is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="572eb-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM \_ Annuler**</span><span class="sxs-lookup"><span data-stu-id="572eb-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="572eb-109">La demande a été annulée par cette application, par une autre application ou par l’appel terminé.</span><span class="sxs-lookup"><span data-stu-id="572eb-109">The request was canceled by this application, by another application, or because the call terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="572eb-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="572eb-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM\_FIRSTTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="572eb-111">Le premier chiffre d’expiration a expiré.</span><span class="sxs-lookup"><span data-stu-id="572eb-111">The first digit timeout expired.</span></span> <span data-ttu-id="572eb-112">La mémoire tampon ne contient pas de chiffres.</span><span class="sxs-lookup"><span data-stu-id="572eb-112">The buffer contains no digits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="572eb-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM \_ INTERtimeout**</span><span class="sxs-lookup"><span data-stu-id="572eb-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM\_INTERTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="572eb-114">Le délai d’expiration inter-chiffres est arrivé à expiration.</span><span class="sxs-lookup"><span data-stu-id="572eb-114">The inter-digit timeout expired.</span></span> <span data-ttu-id="572eb-115">La mémoire tampon contient au moins un chiffre.</span><span class="sxs-lookup"><span data-stu-id="572eb-115">The buffer contains at least one digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="572eb-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**</span><span class="sxs-lookup"><span data-stu-id="572eb-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM\_TERMDIGIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="572eb-117">L’un des chiffres de fin correspond à un chiffre reçu.</span><span class="sxs-lookup"><span data-stu-id="572eb-117">One of the termination digits matched a received digit.</span></span> <span data-ttu-id="572eb-118">Le chiffre d’arrêt mis en correspondance est le dernier chiffre dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="572eb-118">The matched termination digit is the last digit in the buffer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="572eb-119">Notes</span><span class="sxs-lookup"><span data-stu-id="572eb-119">Remarks</span></span>

<span data-ttu-id="572eb-120">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="572eb-120">No extensibility.</span></span> <span data-ttu-id="572eb-121">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="572eb-121">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="572eb-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="572eb-122">Requirements</span></span>



| <span data-ttu-id="572eb-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="572eb-123">Requirement</span></span> | <span data-ttu-id="572eb-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="572eb-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="572eb-125">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="572eb-125">TAPI version</span></span><br/> | <span data-ttu-id="572eb-126">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="572eb-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="572eb-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="572eb-127">Header</span></span><br/>       | <dl> <span data-ttu-id="572eb-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="572eb-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




