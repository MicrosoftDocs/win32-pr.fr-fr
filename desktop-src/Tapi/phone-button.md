---
description: Le \_ message de bouton téléphone TAPI est envoyé pour notifier l’application que la surveillance de l’appui sur les boutons est activée si elle a détecté une pression de bouton sur le téléphone local.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: Message PHONE_BUTTON (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532670"
---
# <a name="phone_button-message"></a><span data-ttu-id="f8abb-103">\_Message du bouton téléphone</span><span class="sxs-lookup"><span data-stu-id="f8abb-103">PHONE\_BUTTON message</span></span>

<span data-ttu-id="f8abb-104">Le message **de \_ bouton téléphone** TAPI est envoyé pour notifier l’application que la surveillance de l’appui sur les boutons est activée si elle a détecté une pression de bouton sur le téléphone local.</span><span class="sxs-lookup"><span data-stu-id="f8abb-104">The TAPI **PHONE\_BUTTON** message is sent to notify the application that button press monitoring is enabled if it has detected a button press on the local phone.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f8abb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8abb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8abb-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="f8abb-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="f8abb-107">Handle vers l’appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="f8abb-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="f8abb-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f8abb-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f8abb-109">Instance de rappel de l’application fournie lors de l’ouverture du périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="f8abb-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="f8abb-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f8abb-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f8abb-111">Identificateur de bouton/lampe du bouton sur lequel l’utilisateur a appuyé.</span><span class="sxs-lookup"><span data-stu-id="f8abb-111">The button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="f8abb-112">Notez que les identificateurs de bouton allant de 0 à 11 sont toujours les boutons du clavier, « 0 » étant l’identificateur de bouton zéro, « 1 » étant l’identificateur de bouton 1 (et ainsi de suite jusqu’à l’identificateur de bouton 9) et « » est l’identificateur de \* bouton 10 et « » \# est l’identificateur de bouton 11.</span><span class="sxs-lookup"><span data-stu-id="f8abb-112">Note that button identifiers zero through 11 are always the KEYPAD buttons, with '0' being button identifier zero, '1' being button identifier 1 (and so on through button identifier 9), and with '\*' being button identifier 10, and '\#' being button identifier 11.</span></span> <span data-ttu-id="f8abb-113">Des informations supplémentaires sur un identificateur de bouton sont disponibles avec [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) et [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span><span class="sxs-lookup"><span data-stu-id="f8abb-113">Additional information about a button identifier is available with [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span></span>

</dd> <dt>

<span data-ttu-id="f8abb-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f8abb-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f8abb-115">Mode du bouton.</span><span class="sxs-lookup"><span data-stu-id="f8abb-115">The button mode of the button.</span></span> <span data-ttu-id="f8abb-116">Ce paramètre utilise l’une des [**\_ constantes PHONEBUTTONMODE**](phonebuttonmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="f8abb-116">This parameter uses one of the [**PHONEBUTTONMODE\_ constants**](phonebuttonmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8abb-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f8abb-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f8abb-118">Spécifie s’il s’agit d’un événement de bouton ou de bouton.</span><span class="sxs-lookup"><span data-stu-id="f8abb-118">Specifies whether this is a button-down event or a button-up event.</span></span> <span data-ttu-id="f8abb-119">Ce paramètre utilise l’une des [**\_ constantes PHONEBUTTONSTATE**](phonebuttonstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="f8abb-119">This parameter uses one of the [**PHONEBUTTONSTATE\_ constants**](phonebuttonstate--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8abb-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8abb-120">Return value</span></span>

<span data-ttu-id="f8abb-121">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f8abb-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8abb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f8abb-122">Remarks</span></span>

<span data-ttu-id="f8abb-123">Un message de **\_ bouton téléphone** est envoyé chaque fois qu’un bouton change d’État.</span><span class="sxs-lookup"><span data-stu-id="f8abb-123">A **PHONE\_BUTTON** message is sent whenever a button changes state.</span></span> <span data-ttu-id="f8abb-124">Une application garantit que pour chaque événement de clic de bouton, il reçoit finalement un événement de rebours de bouton correspondant.</span><span class="sxs-lookup"><span data-stu-id="f8abb-124">An application is guaranteed that for each button down event, it is eventually sent a corresponding button up event.</span></span> <span data-ttu-id="f8abb-125">Un fournisseur de services qui ne peut pas détecter le bouton vers le haut est requis pour générer le message de bouton vers le haut peu après le bouton enfoncé pour chaque pression sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="f8abb-125">A service provider that is incapable of detecting the actual button up is required to generate the button up message shortly after the button down message for each button press.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8abb-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8abb-126">Requirements</span></span>



| <span data-ttu-id="f8abb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8abb-127">Requirement</span></span> | <span data-ttu-id="f8abb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8abb-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f8abb-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f8abb-129">TAPI version</span></span><br/> | <span data-ttu-id="f8abb-130">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f8abb-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f8abb-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8abb-131">Header</span></span><br/>       | <dl> <span data-ttu-id="f8abb-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8abb-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8abb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8abb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8abb-134">**phoneGetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="f8abb-134">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[<span data-ttu-id="f8abb-135">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="f8abb-135">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




