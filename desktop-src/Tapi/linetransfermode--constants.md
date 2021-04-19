---
description: Les \_ constantes d’indicateur de bit LINETRANSFERMODE décrivent les différentes façons de résoudre les demandes de transfert d’appel.
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: Constantes LINETRANSFERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530411"
---
# <a name="linetransfermode_-constants"></a><span data-ttu-id="992c2-103">\_Constantes LINETRANSFERMODE</span><span class="sxs-lookup"><span data-stu-id="992c2-103">LINETRANSFERMODE\_ Constants</span></span>

<span data-ttu-id="992c2-104">Les constantes d’indicateur de bit **LINETRANSFERMODE \_** décrivent les différentes façons de résoudre les demandes de transfert d’appel.</span><span class="sxs-lookup"><span data-stu-id="992c2-104">The **LINETRANSFERMODE\_** bit-flag constants describe different ways of resolving call transfer requests.</span></span>

<dl> <dt>

<span data-ttu-id="992c2-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**\_Conférence LINETRANSFERMODE**</span><span class="sxs-lookup"><span data-stu-id="992c2-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**LINETRANSFERMODE\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="992c2-106">Le transfert est résolu en établissant une conférence triple entre l’application, le tiers connecté à l’appel initial et le tiers connecté à l’appel de consultation.</span><span class="sxs-lookup"><span data-stu-id="992c2-106">The transfer is resolved by establishing a three-way conference between the application, the party connected to the initial call, and the party connected to the consultation call.</span></span> <span data-ttu-id="992c2-107">Un appel de conférence est créé lorsque cette option est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="992c2-107">A conference call is created when this option is selected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="992c2-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**\_transfert LINETRANSFERMODE**</span><span class="sxs-lookup"><span data-stu-id="992c2-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**LINETRANSFERMODE\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="992c2-109">Le transfert est résolu en transférant l’appel initial à l’appel de consultation.</span><span class="sxs-lookup"><span data-stu-id="992c2-109">The transfer is resolved by transferring the initial call to the consultation call.</span></span> <span data-ttu-id="992c2-110">Les deux appels deviennent inactifs pour l’application.</span><span class="sxs-lookup"><span data-stu-id="992c2-110">Both calls will become idle to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="992c2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="992c2-111">Remarks</span></span>

<span data-ttu-id="992c2-112">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="992c2-112">No extensibility.</span></span> <span data-ttu-id="992c2-113">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="992c2-113">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="992c2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="992c2-114">Requirements</span></span>



| <span data-ttu-id="992c2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="992c2-115">Requirement</span></span> | <span data-ttu-id="992c2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="992c2-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="992c2-117">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="992c2-117">TAPI version</span></span><br/> | <span data-ttu-id="992c2-118">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="992c2-118">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="992c2-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="992c2-119">Header</span></span><br/>       | <dl> <span data-ttu-id="992c2-120"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="992c2-120"><dt>Tapi.h</dt></span></span> </dl> |



 

 




