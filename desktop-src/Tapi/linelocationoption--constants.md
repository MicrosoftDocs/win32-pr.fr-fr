---
description: Les \_ constantes LINELOCATIONOPTION définissent les valeurs utilisées dans le membre dwOptions de la structure LINELOCATIONENTRY retournée dans le cadre de la structure LINETRANSLATECAPS retournée par lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: Constantes LINELOCATIONOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545945"
---
# <a name="linelocationoption_-constants"></a><span data-ttu-id="630fa-103">\_Constantes LINELOCATIONOPTION</span><span class="sxs-lookup"><span data-stu-id="630fa-103">LINELOCATIONOPTION\_ Constants</span></span>

<span data-ttu-id="630fa-104">Les constantes **LINELOCATIONOPTION \_** définissent les valeurs utilisées dans le membre **DwOptions** de la structure [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) retournée dans le cadre de la structure [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) retournée par [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span><span class="sxs-lookup"><span data-stu-id="630fa-104">The **LINELOCATIONOPTION\_** constants define values used in the **dwOptions** member of the [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span>

<dl> <dt>

<span data-ttu-id="630fa-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**</span><span class="sxs-lookup"><span data-stu-id="630fa-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION\_PULSEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="630fa-106">Le mode de numérotation par défaut à cet emplacement est la numérotation par impulsions.</span><span class="sxs-lookup"><span data-stu-id="630fa-106">The default dialing mode at this location is pulse dialing.</span></span> <span data-ttu-id="630fa-107">Si ce bit est défini, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) insère un modificateur de numérotation « P » au début de la chaîne de numérotation renvoyée lorsque cet emplacement est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="630fa-107">If this bit is set, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) will insert a "P" dial modifier at the beginning of the dialable string returned when this location is selected.</span></span> <span data-ttu-id="630fa-108">Si ce bit n’est pas défini, **lineTranslateAddress** insère un modificateur de numérotation « T » au début de la chaîne de numérotation.</span><span class="sxs-lookup"><span data-stu-id="630fa-108">If this bit is not set, **lineTranslateAddress** will insert a "T" dial modifier at the beginning of the dialable string.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="630fa-109">Notes</span><span class="sxs-lookup"><span data-stu-id="630fa-109">Remarks</span></span>

<span data-ttu-id="630fa-110">Non extensible.</span><span class="sxs-lookup"><span data-stu-id="630fa-110">Not extensible.</span></span> <span data-ttu-id="630fa-111">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="630fa-111">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="630fa-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="630fa-112">Requirements</span></span>



| <span data-ttu-id="630fa-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="630fa-113">Requirement</span></span> | <span data-ttu-id="630fa-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="630fa-114">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="630fa-115">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="630fa-115">TAPI version</span></span><br/> | <span data-ttu-id="630fa-116">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="630fa-116">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="630fa-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="630fa-117">Header</span></span><br/>       | <dl> <span data-ttu-id="630fa-118"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="630fa-118"><dt>Tapi.h</dt></span></span> </dl> |



 

 




