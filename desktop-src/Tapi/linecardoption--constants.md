---
description: Les \_ constantes LINECARDOPTION définissent les valeurs utilisées dans le membre dwOptions de la structure LINECARDENTRY retournée dans le cadre de la structure LINETRANSLATECAPS retournée par lineGetTranslateCaps.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: Constantes LINECARDOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537706"
---
# <a name="linecardoption_-constants"></a><span data-ttu-id="9fa81-103">\_Constantes LINECARDOPTION</span><span class="sxs-lookup"><span data-stu-id="9fa81-103">LINECARDOPTION\_ Constants</span></span>

<span data-ttu-id="9fa81-104">Les **\_ constantes LINECARDOPTION** définissent les valeurs utilisées dans le membre **DwOptions** de la structure [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) retournée dans le cadre de la structure [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) retournée par [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span><span class="sxs-lookup"><span data-stu-id="9fa81-104">The **LINECARDOPTION\_constants** define values used in the **dwOptions** member of the [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span> <span data-ttu-id="9fa81-105">Les **\_ constantes LINECARDOPTION** t ont les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9fa81-105">The **LINECARDOPTION\_constants** t has the following values:</span></span>

<dl> <dt>

<span data-ttu-id="9fa81-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION \_ masqué**</span><span class="sxs-lookup"><span data-stu-id="9fa81-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION\_HIDDEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9fa81-107">Cette carte d’appel a été masquée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9fa81-107">This calling card has been hidden by the user.</span></span> <span data-ttu-id="9fa81-108">Elle n’est pas affichée par Dial Helper dans la liste principale des cartes d’appel disponibles, mais apparaît dans la liste des cartes à partir desquelles les règles de numérotation peuvent être copiées.</span><span class="sxs-lookup"><span data-stu-id="9fa81-108">It is not shown by Dial Helper in the main listing of available calling cards, but will be shown in the list of cards from which dialing rules can be copied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9fa81-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ prédéfini**</span><span class="sxs-lookup"><span data-stu-id="9fa81-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION\_PREDEFINED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9fa81-110">Cette carte d’appel est l’une des définitions prédéfinies de carte d’appel, incluse avec la téléphonie par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9fa81-110">This calling card is one of the predefined calling card definitions included with Telephony by Microsoft.</span></span> <span data-ttu-id="9fa81-111">Elle ne peut pas être entièrement supprimée à l’aide de Dial Helper. Si l’utilisateur tente de le supprimer, il est masqué.</span><span class="sxs-lookup"><span data-stu-id="9fa81-111">It cannot be removed entirely using Dial Helper; if the user attempts to remove it, it will become HIDDEN.</span></span> <span data-ttu-id="9fa81-112">Elle reste donc accessible pour la copie des règles de numérotation.</span><span class="sxs-lookup"><span data-stu-id="9fa81-112">It thus continues to be accessible for copying of dialing rules.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fa81-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9fa81-113">Remarks</span></span>

<span data-ttu-id="9fa81-114">Non extensible.</span><span class="sxs-lookup"><span data-stu-id="9fa81-114">Not extensible.</span></span> <span data-ttu-id="9fa81-115">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="9fa81-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa81-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fa81-116">Requirements</span></span>



| <span data-ttu-id="9fa81-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fa81-117">Requirement</span></span> | <span data-ttu-id="9fa81-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fa81-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9fa81-119">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="9fa81-119">TAPI version</span></span><br/> | <span data-ttu-id="9fa81-120">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9fa81-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9fa81-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9fa81-121">Header</span></span><br/>       | <dl> <span data-ttu-id="9fa81-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fa81-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




