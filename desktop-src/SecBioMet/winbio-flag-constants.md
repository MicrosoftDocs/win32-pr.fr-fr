---
title: Constantes WINBIO_FLAG ( \_ types WINBIO. h)
description: Spécifiez la configuration de l’unité biométrique et les caractéristiques d’accès pour la nouvelle session.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384115"
---
# <a name="winbio_flag-constants"></a><span data-ttu-id="9316b-103">\_Constantes d’indicateur WINBIO</span><span class="sxs-lookup"><span data-stu-id="9316b-103">WINBIO\_FLAG Constants</span></span>

<span data-ttu-id="9316b-104">Les constantes suivantes peuvent être utilisées dans la fonction [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour spécifier la configuration de l’unité biométrique et les caractéristiques d’accès pour la nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="9316b-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify biometric unit configuration and access characteristics for the new session.</span></span>



| <span data-ttu-id="9316b-105">Constante</span><span class="sxs-lookup"><span data-stu-id="9316b-105">Constant</span></span>                                                                                                                                                                                     | <span data-ttu-id="9316b-106">Description</span><span class="sxs-lookup"><span data-stu-id="9316b-106">Description</span></span>                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <span data-ttu-id="9316b-107"><dt>**\_indicateur WINBIO \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="9316b-107"><dt>**WINBIO\_FLAG\_DEFAULT**</dt></span></span> </dl>             | <span data-ttu-id="9316b-108">Indicateur de configuration du capteur.</span><span class="sxs-lookup"><span data-stu-id="9316b-108">Sensor configuration flag.</span></span> <span data-ttu-id="9316b-109">Les unités biométriques fonctionnent de la manière spécifiée pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="9316b-109">The biometric units operate in the manner specified during installation.</span></span><br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <span data-ttu-id="9316b-110"><dt>**indicateur WINBIO de \_ \_ base**</dt></span><span class="sxs-lookup"><span data-stu-id="9316b-110"><dt>**WINBIO\_FLAG\_BASIC**</dt></span></span> </dl>                   | <span data-ttu-id="9316b-111">Indicateur de configuration du capteur.</span><span class="sxs-lookup"><span data-stu-id="9316b-111">Sensor configuration flag.</span></span> <span data-ttu-id="9316b-112">Les unités biométriques fonctionnent uniquement comme des périphériques de capture de base.</span><span class="sxs-lookup"><span data-stu-id="9316b-112">The biometric units operate only as basic capture devices.</span></span><br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <span data-ttu-id="9316b-113"><dt>**\_indicateur WINBIO \_ avancé**</dt></span><span class="sxs-lookup"><span data-stu-id="9316b-113"><dt>**WINBIO\_FLAG\_ADVANCED**</dt></span></span> </dl>          | <span data-ttu-id="9316b-114">Indicateur de configuration du capteur.</span><span class="sxs-lookup"><span data-stu-id="9316b-114">Sensor configuration flag.</span></span> <span data-ttu-id="9316b-115">Les unités biométriques utilisent les capacités de traitement et de stockage interne.</span><span class="sxs-lookup"><span data-stu-id="9316b-115">The biometric units use internal processing and storage capabilities.</span></span><br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <span data-ttu-id="9316b-116"><dt>**\_indicateur WINBIO \_ RAW**</dt></span><span class="sxs-lookup"><span data-stu-id="9316b-116"><dt>**WINBIO\_FLAG\_RAW**</dt></span></span> </dl>                         | <span data-ttu-id="9316b-117">Indicateur d’accès souhaité.</span><span class="sxs-lookup"><span data-stu-id="9316b-117">Desired access flag.</span></span> <span data-ttu-id="9316b-118">L’application cliente capture les données biométriques brutes à l’aide de [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="9316b-118">The client application captures raw biometric data using [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span><br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <span data-ttu-id="9316b-119"><dt>**MAINTENANCE de l' \_ indicateur WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9316b-119"><dt>**WINBIO\_FLAG\_MAINTENANCE**</dt></span></span> </dl> | <span data-ttu-id="9316b-120">Indicateur d’accès souhaité.</span><span class="sxs-lookup"><span data-stu-id="9316b-120">Desired access flag.</span></span> <span data-ttu-id="9316b-121">Le client effectue des opérations de contrôle définies par le fournisseur sur une unité biométrique en appelant [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="9316b-121">The client performs vendor-defined control operations on a biometric unit by calling [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9316b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9316b-122">Requirements</span></span>



| <span data-ttu-id="9316b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9316b-123">Requirement</span></span> | <span data-ttu-id="9316b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9316b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9316b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9316b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9316b-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9316b-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="9316b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9316b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9316b-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9316b-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9316b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="9316b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9316b-130"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9316b-130"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9316b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9316b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9316b-132">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="9316b-132">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





