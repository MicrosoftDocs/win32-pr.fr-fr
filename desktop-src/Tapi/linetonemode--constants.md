---
description: Les \_ constantes LINETONEMODE décrivent les différentes sélections utilisées lors de la génération de tonalités de ligne.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: Constantes LINETONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528414"
---
# <a name="linetonemode_-constants"></a><span data-ttu-id="4e65f-103">\_Constantes LINETONEMODE</span><span class="sxs-lookup"><span data-stu-id="4e65f-103">LINETONEMODE\_ Constants</span></span>

<span data-ttu-id="4e65f-104">Les **\_ constantes LINETONEMODE** décrivent les différentes sélections utilisées lors de la génération de tonalités de ligne.</span><span class="sxs-lookup"><span data-stu-id="4e65f-104">The **LINETONEMODE\_ constants** describe different selections that are used when generating line tones.</span></span>

<dl> <dt>

<span data-ttu-id="4e65f-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**\_signal LINETONEMODE**</span><span class="sxs-lookup"><span data-stu-id="4e65f-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE\_BEEP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4e65f-106">Le ton est un bip, tel que celui utilisé pour annoncer le début d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="4e65f-106">The tone is a beep, such as that used to announce the beginning of a recording.</span></span> <span data-ttu-id="4e65f-107">La définition exacte est définie par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="4e65f-107">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e65f-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**\_facturation LINETONEMODE**</span><span class="sxs-lookup"><span data-stu-id="4e65f-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**LINETONEMODE\_BILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4e65f-109">Le ton est un titre d’information de facturation, tel qu’une tonalité de carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="4e65f-109">The tone is a billing information tone such as a credit card prompt tone.</span></span> <span data-ttu-id="4e65f-110">La définition exacte est définie par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="4e65f-110">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e65f-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="4e65f-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4e65f-112">Le ton est occupé.</span><span class="sxs-lookup"><span data-stu-id="4e65f-112">The tone is a busy tone.</span></span> <span data-ttu-id="4e65f-113">La définition exacte est définie par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="4e65f-113">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e65f-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ personnalisé**</span><span class="sxs-lookup"><span data-stu-id="4e65f-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4e65f-115">Le ton est un ton personnalisé défini par ses fréquences de composants, de type [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span><span class="sxs-lookup"><span data-stu-id="4e65f-115">The tone is a custom tone defined by its component frequencies, of type [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e65f-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**\_rappel LINETONEMODE**</span><span class="sxs-lookup"><span data-stu-id="4e65f-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4e65f-117">Le ton est un signal d’inversion.</span><span class="sxs-lookup"><span data-stu-id="4e65f-117">The tone is ringback tone.</span></span> <span data-ttu-id="4e65f-118">La définition exacte est définie par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="4e65f-118">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e65f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4e65f-119">Remarks</span></span>

<span data-ttu-id="4e65f-120">Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e65f-120">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="4e65f-121">Les 16 bits de poids faible sont réservés.</span><span class="sxs-lookup"><span data-stu-id="4e65f-121">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="4e65f-122">Ces constantes sont utilisées pour définir des tonalités à générer sur un appel au tiers distant.</span><span class="sxs-lookup"><span data-stu-id="4e65f-122">These constants are used to define tones to be generated inband over a call to the remote party.</span></span> <span data-ttu-id="4e65f-123">Notez que la détection de tons de tonalités non personnalisées n’utilise pas ces constantes.</span><span class="sxs-lookup"><span data-stu-id="4e65f-123">Note that tone detection of non-custom tones does not use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e65f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e65f-124">Requirements</span></span>



| <span data-ttu-id="4e65f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e65f-125">Requirement</span></span> | <span data-ttu-id="4e65f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e65f-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4e65f-127">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="4e65f-127">TAPI version</span></span><br/> | <span data-ttu-id="4e65f-128">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4e65f-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4e65f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e65f-129">Header</span></span><br/>       | <dl> <span data-ttu-id="4e65f-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e65f-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




