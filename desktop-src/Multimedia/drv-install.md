---
title: Message DRV_INSTALL (mmsystem. h)
description: Avertit le pilote qui est en cours d’installation. Le pilote doit créer et initialiser toutes les clés et valeurs de Registre nécessaires et vérifier que les pilotes et le matériel de prise en charge sont installés et correctement configurés.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- Message DRV_INSTALL Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942826"
---
# <a name="drv_install-message"></a><span data-ttu-id="ecbac-105">Message d’installation de DRV \_</span><span class="sxs-lookup"><span data-stu-id="ecbac-105">DRV\_INSTALL message</span></span>

<span data-ttu-id="ecbac-106">Avertit le pilote qui est en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="ecbac-106">Notifies the driver that is it being installed.</span></span> <span data-ttu-id="ecbac-107">Le pilote doit créer et initialiser toutes les clés et valeurs de Registre nécessaires et vérifier que les pilotes et le matériel de prise en charge sont installés et correctement configurés.</span><span class="sxs-lookup"><span data-stu-id="ecbac-107">The driver should create and initialize any needed registry keys and values and verify that the supporting drivers and hardware are installed and properly configured.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecbac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecbac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecbac-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="ecbac-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="ecbac-110">Identificateur du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="ecbac-110">Identifier of the installable driver.</span></span> <span data-ttu-id="ecbac-111">Il s’agit de la même valeur que celle précédemment retournée par le pilote à partir du message de l' [**\_ ouverture du DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="ecbac-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="ecbac-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="ecbac-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="ecbac-113">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="ecbac-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="ecbac-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ecbac-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ecbac-115">Adresse d’une structure [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="ecbac-115">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="ecbac-116">Si une structure est fournie, elle contient les noms de la clé de Registre et la valeur associée au pilote.</span><span class="sxs-lookup"><span data-stu-id="ecbac-116">If a structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecbac-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ecbac-117">Return Value</span></span>

<span data-ttu-id="ecbac-118">Retourne l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ecbac-118">Returns one of these values:</span></span>



| <span data-ttu-id="ecbac-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecbac-119">Requirement</span></span> | <span data-ttu-id="ecbac-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecbac-120">Value</span></span> |
|-----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbac-121">DRVCNF \_ OK</span><span class="sxs-lookup"><span data-stu-id="ecbac-121">DRVCNF\_OK</span></span>      | <span data-ttu-id="ecbac-122">L’installation a réussi ; aucune action supplémentaire n’est requise.</span><span class="sxs-lookup"><span data-stu-id="ecbac-122">The installation is successful; no further action is required.</span></span>                             |
| <span data-ttu-id="ecbac-123">DRVCNF \_ Annuler</span><span class="sxs-lookup"><span data-stu-id="ecbac-123">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="ecbac-124">L’installation a échoué..</span><span class="sxs-lookup"><span data-stu-id="ecbac-124">The installation failed..</span></span>                                                                  |
| <span data-ttu-id="ecbac-125">redémarrage de DRVCNF \_</span><span class="sxs-lookup"><span data-stu-id="ecbac-125">DRVCNF\_RESTART</span></span> | <span data-ttu-id="ecbac-126">L’installation a réussi, mais elle ne prend effet qu’après le redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="ecbac-126">The installation is successful, but it does not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ecbac-127">Notes</span><span class="sxs-lookup"><span data-stu-id="ecbac-127">Remarks</span></span>

<span data-ttu-id="ecbac-128">Le paramètre *lParam1* n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ecbac-128">The *lParam1* parameter is not used.</span></span>

<span data-ttu-id="ecbac-129">Certains pilotes installables ajoutent des informations de configuration à la valeur affectée à la valeur de registre associée au pilote.</span><span class="sxs-lookup"><span data-stu-id="ecbac-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbac-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecbac-130">Requirements</span></span>



| <span data-ttu-id="ecbac-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecbac-131">Requirement</span></span> | <span data-ttu-id="ecbac-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecbac-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbac-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecbac-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ecbac-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecbac-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ecbac-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecbac-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ecbac-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecbac-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ecbac-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecbac-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecbac-138"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecbac-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecbac-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecbac-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbac-140">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="ecbac-140">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="ecbac-141">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="ecbac-141">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

