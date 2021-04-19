---
description: Signale que le nombre de boutons de menu DVD a changé ou que la sélection du bouton a été modifiée.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540607"
---
# <a name="ec_dvd_button_change"></a><span data-ttu-id="c62cc-103">\_changement du \_ bouton \_ DVD EC</span><span class="sxs-lookup"><span data-stu-id="c62cc-103">EC\_DVD\_BUTTON\_CHANGE</span></span>

<span data-ttu-id="c62cc-104">Signale que le nombre de boutons de menu DVD a changé ou que la sélection du bouton a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="c62cc-104">Signals that the number of DVD menu buttons has changed, or that the button selection has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="c62cc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c62cc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c62cc-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c62cc-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c62cc-107">Valeur **DWORD** indiquant le nombre de boutons disponibles.</span><span class="sxs-lookup"><span data-stu-id="c62cc-107">**DWORD** value indicating the number of available buttons.</span></span>

</dd> <dt>

<span data-ttu-id="c62cc-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c62cc-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c62cc-109">Valeur **DWORD** indiquant le numéro de bouton actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c62cc-109">**DWORD** value indicating the currently selected button number.</span></span> <span data-ttu-id="c62cc-110">Le numéro de bouton sélectionné zéro signifie qu’aucun bouton n’est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c62cc-110">Selected button number zero implies that no button is selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c62cc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c62cc-111">Remarks</span></span>

<span data-ttu-id="c62cc-112">Les numéros de bouton vont de 1 à 36.</span><span class="sxs-lookup"><span data-stu-id="c62cc-112">Button numbers range from 1 to 36.</span></span>

<span data-ttu-id="c62cc-113">Le bouton actuellement sélectionné peut changer automatiquement à l’aide d’une commande de navigation créée sur le disque, ainsi que via le contrôle d’application à l’aide de l’interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="c62cc-113">The currently selected button can change automatically with a navigation command authored on the disc as well as through application control by using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="c62cc-114">Cet événement peut signaler n’importe quel numéro de bouton disponible.</span><span class="sxs-lookup"><span data-stu-id="c62cc-114">This event can signal any of the available button numbers.</span></span> <span data-ttu-id="c62cc-115">Ces nombres ne correspondent pas toujours aux numéros de bouton utilisés pour [**IDvdControl2 :: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) , car cette méthode ne peut activer qu’un sous-ensemble de boutons.</span><span class="sxs-lookup"><span data-stu-id="c62cc-115">These numbers do not always correspond to button numbers used for [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) because that method can activate only a subset of buttons.</span></span>

<span data-ttu-id="c62cc-116">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="c62cc-116">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="c62cc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c62cc-117">Requirements</span></span>



| <span data-ttu-id="c62cc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c62cc-118">Requirement</span></span> | <span data-ttu-id="c62cc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c62cc-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c62cc-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c62cc-120">Header</span></span><br/> | <dl> <span data-ttu-id="c62cc-121"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c62cc-121"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c62cc-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c62cc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62cc-123">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="c62cc-123">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="c62cc-124">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="c62cc-124">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c62cc-125">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="c62cc-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




