---
title: Constantes WINBIO_INDICATOR_STATUS ( \_ types WINBIO. h)
description: Définissez un témoin lumineux.
ms.assetid: 1e00ff9d-6693-4763-8ac3-b42d2a3e987d
topic_type:
- apiref
api_name:
- WINBIO_INDICATOR_ON
- WINBIO_INDICATOR_OFF
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7693fbd2b9b37067738774d172f4bb482edb06e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106529085"
---
# <a name="winbio_indicator_status-constants"></a><span data-ttu-id="3db07-103">\_Constantes d’état de l’indicateur WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="3db07-103">WINBIO\_INDICATOR\_STATUS Constants</span></span>

<span data-ttu-id="3db07-104">Les valeurs suivantes peuvent être utilisées pour définir un témoin lumineux.</span><span class="sxs-lookup"><span data-stu-id="3db07-104">The following values can be used to set an indicator light.</span></span> <span data-ttu-id="3db07-105">Par défaut, les capteurs ne sont pas allumés, mais les applications peuvent utiliser ces valeurs pour activer ou désactiver les indicateurs d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="3db07-105">By default, sensors will not have a light on, but applications can use these values to enable or disable indicator lights.</span></span> <span data-ttu-id="3db07-106">La valeur d' **\_ \_ État du capteur WINBIO** fournit plus de détails sur l’état d’un voyant lumineux.</span><span class="sxs-lookup"><span data-stu-id="3db07-106">The **WINBIO\_SENSOR\_STATUS** value provides more detail about the status of an indicator light that is on.</span></span> <span data-ttu-id="3db07-107">Pour plus d’informations, consultez les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="3db07-107">For more information, see the following functions:</span></span>

-   [<span data-ttu-id="3db07-108">**SensorAdapterSetIndicatorStatus**</span><span class="sxs-lookup"><span data-stu-id="3db07-108">**SensorAdapterSetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [<span data-ttu-id="3db07-109">**SensorAdapterGetIndicatorStatus**</span><span class="sxs-lookup"><span data-stu-id="3db07-109">**SensorAdapterGetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [<span data-ttu-id="3db07-110">**SensorAdapterQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="3db07-110">**SensorAdapterQueryStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| <span data-ttu-id="3db07-111">Constante</span><span class="sxs-lookup"><span data-stu-id="3db07-111">Constant</span></span>                                                                                                                                                                            | <span data-ttu-id="3db07-112">Description</span><span class="sxs-lookup"><span data-stu-id="3db07-112">Description</span></span>                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <span data-ttu-id="3db07-113"><dt>**\_indicateur WINBIO \_ activé**</dt></span><span class="sxs-lookup"><span data-stu-id="3db07-113"><dt>**WINBIO\_INDICATOR\_ON**</dt></span></span> </dl>    | <span data-ttu-id="3db07-114">La lumière de l’indicateur de capteur est allumée.</span><span class="sxs-lookup"><span data-stu-id="3db07-114">The sensor indicator light is on.</span></span><br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <span data-ttu-id="3db07-115"><dt>**\_indicateur WINBIO \_ désactivé**</dt></span><span class="sxs-lookup"><span data-stu-id="3db07-115"><dt>**WINBIO\_INDICATOR\_OFF**</dt></span></span> </dl> | <span data-ttu-id="3db07-116">La lumière de l’indicateur de capteur est désactivée.</span><span class="sxs-lookup"><span data-stu-id="3db07-116">The sensor indicator light is off.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3db07-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3db07-117">Requirements</span></span>



| <span data-ttu-id="3db07-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3db07-118">Requirement</span></span> | <span data-ttu-id="3db07-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3db07-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3db07-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3db07-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3db07-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3db07-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="3db07-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3db07-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3db07-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3db07-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3db07-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3db07-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3db07-125"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3db07-125"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3db07-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3db07-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3db07-127">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="3db07-127">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





