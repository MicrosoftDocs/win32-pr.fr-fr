---
title: Constantes WINBIO_SENSOR_MODE ( \_ types WINBIO. h)
description: Définissez le mode d’adaptateur de capteur.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743669"
---
# <a name="winbio_sensor_mode-constants"></a><span data-ttu-id="220f9-103">\_Constantes du mode de capteur WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="220f9-103">WINBIO\_SENSOR\_MODE Constants</span></span>

<span data-ttu-id="220f9-104">Les valeurs suivantes sont utilisées dans la fonction [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) pour définir le mode d’adaptateur de capteur.</span><span class="sxs-lookup"><span data-stu-id="220f9-104">The following values are used in the [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) function to set the sensor adapter mode.</span></span>



| <span data-ttu-id="220f9-105">Constante</span><span class="sxs-lookup"><span data-stu-id="220f9-105">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="220f9-106">Description</span><span class="sxs-lookup"><span data-stu-id="220f9-106">Description</span></span>                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <span data-ttu-id="220f9-107"><dt>**\_capteur WINBIO \_ \_ mode inconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="220f9-107"><dt>**WINBIO\_SENSOR\_UNKNOWN\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="220f9-108">Le mode d’opération n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="220f9-108">The operating mode is not known.</span></span><br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <span data-ttu-id="220f9-109"><dt>**WINBIO \_ - \_ mode de base du capteur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="220f9-109"><dt>**WINBIO\_SENSOR\_BASIC\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="220f9-110">Faire fonctionner le capteur en mode de base.</span><span class="sxs-lookup"><span data-stu-id="220f9-110">Operate the sensor in basic mode.</span></span> <span data-ttu-id="220f9-111">Le capteur agit uniquement comme un appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="220f9-111">The sensor acts only as a capture device.</span></span> <span data-ttu-id="220f9-112">Les capacités de traitement ou de stockage intégrées qui existent ne sont pas utilisées.</span><span class="sxs-lookup"><span data-stu-id="220f9-112">Any onboard processing or storage capabilities that exist are not used.</span></span><br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <span data-ttu-id="220f9-113"><dt>**\_ \_ mode avancé du capteur WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="220f9-113"><dt>**WINBIO\_SENSOR\_ADVANCED\_MODE**</dt></span></span> </dl>       | <span data-ttu-id="220f9-114">Faire fonctionner le capteur en mode avancé.</span><span class="sxs-lookup"><span data-stu-id="220f9-114">Operate the sensor in advanced mode.</span></span> <span data-ttu-id="220f9-115">Le capteur peut capturer des exemples et effectuer des fonctions de correspondance et de stockage.</span><span class="sxs-lookup"><span data-stu-id="220f9-115">The sensor can capture samples and perform matching and storage functions.</span></span><br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <span data-ttu-id="220f9-116"><dt>**\_mode de \_ navigation du capteur WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="220f9-116"><dt>**WINBIO\_SENSOR\_NAVIGATION\_MODE**</dt></span></span> </dl> | <span data-ttu-id="220f9-117">Faire fonctionner le capteur comme un tapis de souris.</span><span class="sxs-lookup"><span data-stu-id="220f9-117">Operate the sensor as a mouse pad.</span></span> <span data-ttu-id="220f9-118">Cela n’est actuellement pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="220f9-118">This is not currently supported.</span></span><br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <span data-ttu-id="220f9-119"><dt>**\_ \_ mode veille du capteur WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="220f9-119"><dt>**WINBIO\_SENSOR\_SLEEP\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="220f9-120">Faire fonctionner le capteur en mode veille.</span><span class="sxs-lookup"><span data-stu-id="220f9-120">Operate the sensor in sleep mode.</span></span><br/>                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="220f9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="220f9-121">Requirements</span></span>



| <span data-ttu-id="220f9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="220f9-122">Requirement</span></span> | <span data-ttu-id="220f9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="220f9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="220f9-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="220f9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="220f9-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="220f9-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="220f9-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="220f9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="220f9-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="220f9-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="220f9-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="220f9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="220f9-129"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="220f9-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="220f9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="220f9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="220f9-131">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="220f9-131">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





