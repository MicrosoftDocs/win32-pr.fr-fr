---
description: Les \_ constantes d’indicateur de bit LINEGENERATETERM décrivent les conditions dans lesquelles la génération de chiffre ou de tonalité est terminée.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: Constantes LINEGENERATETERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543970"
---
# <a name="linegenerateterm_-constants"></a><span data-ttu-id="73734-103">\_Constantes LINEGENERATETERM</span><span class="sxs-lookup"><span data-stu-id="73734-103">LINEGENERATETERM\_ Constants</span></span>

<span data-ttu-id="73734-104">Les constantes d’indicateur de bit **LINEGENERATETERM \_** décrivent les conditions dans lesquelles la génération de chiffre ou de tonalité est terminée.</span><span class="sxs-lookup"><span data-stu-id="73734-104">The **LINEGENERATETERM\_** bit-flag constants describe the conditions under which digit or tone generation is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="73734-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM \_ Annuler**</span><span class="sxs-lookup"><span data-stu-id="73734-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73734-106">La demande de génération de chiffres ou de tonalités a été annulée par cette application, par une autre application ou par l’appel terminé.</span><span class="sxs-lookup"><span data-stu-id="73734-106">The digit or tone generation request was canceled by this application, by another application, or because the call terminated.</span></span> <span data-ttu-id="73734-107">Cette valeur peut également être retournée lorsque la génération d’un chiffre ou d’un ton ne peut pas être effectuée en raison d’une défaillance interne du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="73734-107">This value can also be returned when digit or tone generation cannot be completed due to internal failure of the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73734-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="73734-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM\_DONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73734-109">Le nombre demandé de chiffres ou de tonalités demandés a été généré pour la durée demandée.</span><span class="sxs-lookup"><span data-stu-id="73734-109">The requested number of digits or requested tones have been generated for the requested duration.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73734-110">Notes</span><span class="sxs-lookup"><span data-stu-id="73734-110">Remarks</span></span>

<span data-ttu-id="73734-111">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="73734-111">No extensibility.</span></span> <span data-ttu-id="73734-112">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="73734-112">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="73734-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73734-113">Requirements</span></span>



| <span data-ttu-id="73734-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73734-114">Requirement</span></span> | <span data-ttu-id="73734-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="73734-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="73734-116">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="73734-116">TAPI version</span></span><br/> | <span data-ttu-id="73734-117">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="73734-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="73734-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="73734-118">Header</span></span><br/>       | <dl> <span data-ttu-id="73734-119"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="73734-119"><dt>Tapi.h</dt></span></span> </dl> |



 

 




