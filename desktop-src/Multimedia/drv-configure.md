---
title: Message DRV_CONFIGURE (mmsystem. h)
description: Indique au pilote installable d’afficher sa boîte de dialogue de configuration et de permettre à l’utilisateur de spécifier de nouveaux paramètres pour l’instance de pilote d’installation donnée.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- Message DRV_CONFIGURE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942829"
---
# <a name="drv_configure-message"></a><span data-ttu-id="b0c5b-104">DRV \_ configurer le message</span><span class="sxs-lookup"><span data-stu-id="b0c5b-104">DRV\_CONFIGURE message</span></span>

<span data-ttu-id="b0c5b-105">Indique au pilote installable d’afficher sa boîte de dialogue de configuration et de permettre à l’utilisateur de spécifier de nouveaux paramètres pour l’instance de pilote d’installation donnée.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-105">Directs the installable driver to display its configuration dialog box and let the user specify new settings for the given installable driver instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0c5b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0c5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0c5b-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="b0c5b-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="b0c5b-108">Identificateur du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-108">Identifier of the installable driver.</span></span> <span data-ttu-id="b0c5b-109">Il s’agit de la même valeur que celle précédemment retournée par le pilote à partir du message de l' [**\_ ouverture du DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="b0c5b-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="b0c5b-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="b0c5b-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="b0c5b-111">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-111">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="b0c5b-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b0c5b-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b0c5b-113">Handle de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-113">Handle of the parent window.</span></span> <span data-ttu-id="b0c5b-114">Cette fenêtre est utilisée comme fenêtre parente pour la boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-114">This window is used as the parent window for the configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b0c5b-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b0c5b-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b0c5b-116">Adresse d’une structure [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-116">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="b0c5b-117">Si la structure est donnée, elle contient les noms de la clé de Registre et la valeur associée au pilote.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-117">If the structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0c5b-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0c5b-118">Return Value</span></span>

<span data-ttu-id="b0c5b-119">Retourne l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0c5b-119">Returns one of these values:</span></span>



| <span data-ttu-id="b0c5b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0c5b-120">Requirement</span></span> | <span data-ttu-id="b0c5b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0c5b-121">Value</span></span> |
|-----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c5b-122">DRVCNF \_ OK</span><span class="sxs-lookup"><span data-stu-id="b0c5b-122">DRVCNF\_OK</span></span>      | <span data-ttu-id="b0c5b-123">La configuration a réussi ; aucune action supplémentaire n’est requise.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-123">The configuration is successful; no further action is required.</span></span>                                    |
| <span data-ttu-id="b0c5b-124">DRVCNF \_ Annuler</span><span class="sxs-lookup"><span data-stu-id="b0c5b-124">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="b0c5b-125">L’utilisateur a annulé la boîte de dialogue ; aucune action supplémentaire n’est requise.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-125">The user canceled the dialog box; no further action is required.</span></span>                                   |
| <span data-ttu-id="b0c5b-126">redémarrage de DRVCNF \_</span><span class="sxs-lookup"><span data-stu-id="b0c5b-126">DRVCNF\_RESTART</span></span> | <span data-ttu-id="b0c5b-127">La configuration est réussie, mais les modifications ne prennent effet qu’après le redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-127">The configuration is successful, but the changes do not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b0c5b-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b0c5b-128">Remarks</span></span>

<span data-ttu-id="b0c5b-129">Certains pilotes installables ajoutent des informations de configuration à la valeur affectée à la valeur de registre associée au pilote.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

<span data-ttu-id="b0c5b-130">Les valeurs de retour de DRV \_ Cancel, DRV \_ OK et DRV \_ restart sont obsolètes. elles ont été remplacées par DRVCNF \_ Cancel, DRVCNF \_ OK et DRVCNF \_ Restart, respectivement.</span><span class="sxs-lookup"><span data-stu-id="b0c5b-130">The DRV\_CANCEL, DRV\_OK, and DRV\_RESTART return values are obsolete; they have been replaced by DRVCNF\_CANCEL, DRVCNF\_OK, and DRVCNF\_RESTART, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0c5b-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0c5b-131">Requirements</span></span>



| <span data-ttu-id="b0c5b-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0c5b-132">Requirement</span></span> | <span data-ttu-id="b0c5b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0c5b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c5b-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0c5b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b0c5b-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0c5b-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b0c5b-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0c5b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b0c5b-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0c5b-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b0c5b-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0c5b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0c5b-139"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0c5b-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0c5b-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0c5b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0c5b-141">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="b0c5b-141">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="b0c5b-142">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="b0c5b-142">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

