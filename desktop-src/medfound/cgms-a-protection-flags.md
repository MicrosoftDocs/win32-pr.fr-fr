---
description: Spécifiez les niveaux de protection pour le système de gestion de la génération de copie&\# 8212 ; Analogique (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: Indicateurs de protection de CGMS-A (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393307"
---
# <a name="cgms-a-protection-flags"></a><span data-ttu-id="5a93b-103">Indicateurs de protection de CGMS-A</span><span class="sxs-lookup"><span data-stu-id="5a93b-103">CGMS-A Protection Flags</span></span>

<span data-ttu-id="5a93b-104">Les constantes dans le tableau suivant spécifient les niveaux de protection pour la version analogique du système de gestion de la génération de copie (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="5a93b-104">The constants in the following table specify the protection levels for Copy Generation Management System Analog (CGMS-A).</span></span>



| <span data-ttu-id="5a93b-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="5a93b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="5a93b-106">Description</span><span class="sxs-lookup"><span data-stu-id="5a93b-106">Description</span></span>                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <span data-ttu-id="5a93b-107"><dt>**OPM \_ CGMSA \_ désactivé**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="5a93b-107"><dt>**OPM\_CGMSA\_OFF**</dt> <dt>0x00</dt></span></span> </dl>                                                                                       | <span data-ttu-id="5a93b-108">CGMS-A est désactivé.</span><span class="sxs-lookup"><span data-stu-id="5a93b-108">CGMS-A is disabled.</span></span> <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <span data-ttu-id="5a93b-109"><dt>**OPM \_ CGMSA \_ copier \_ librement**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="5a93b-109"><dt>**OPM\_CGMSA\_COPY\_FREELY**</dt> <dt>0x01</dt></span></span> </dl>                                                              | <span data-ttu-id="5a93b-110">Le niveau de protection est copie libre.</span><span class="sxs-lookup"><span data-stu-id="5a93b-110">The protection level is Copy Freely.</span></span><br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <span data-ttu-id="5a93b-111"><dt>**OPM \_ CGMSA \_ Copy \_ n’a \_ plus**</dt> de <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="5a93b-111"><dt>**OPM\_CGMSA\_COPY\_NO\_MORE**</dt> <dt>0x02</dt></span></span> </dl>                                                          | <span data-ttu-id="5a93b-112">Le niveau de protection n’est pas copié.</span><span class="sxs-lookup"><span data-stu-id="5a93b-112">The protection level is Copy No More.</span></span> <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <span data-ttu-id="5a93b-113"><dt>**OPM \_ CGMSA \_ copier \_ une \_**</dt> <dt>0x03</dt> de génération</span><span class="sxs-lookup"><span data-stu-id="5a93b-113"><dt>**OPM\_CGMSA\_COPY\_ONE\_GENERATION**</dt> <dt>0x03</dt></span></span> </dl>                                     | <span data-ttu-id="5a93b-114">Le niveau de protection est copier une génération.</span><span class="sxs-lookup"><span data-stu-id="5a93b-114">The protection level is Copy One Generation.</span></span> <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <span data-ttu-id="5a93b-115"><dt>**OPM \_ CGMSA \_ \_ ne jamais**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="5a93b-115"><dt>**OPM\_CGMSA\_COPY\_NEVER**</dt> <dt>0x04</dt></span></span> </dl>                                                                 | <span data-ttu-id="5a93b-116">Le niveau de protection est ne jamais copier.</span><span class="sxs-lookup"><span data-stu-id="5a93b-116">The protection level is Copy Never.</span></span><br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <span data-ttu-id="5a93b-117"><dt>**OPM \_ \_Le contrôle de redistribution CGMSA \_ \_ requis**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="5a93b-117"><dt>**OPM\_CGMSA\_REDISTRIBUTION\_CONTROL\_REQUIRED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="5a93b-118">Le contrôle de redistribution (également appelé *indicateur de diffusion*) est requis.</span><span class="sxs-lookup"><span data-stu-id="5a93b-118">Redistribution control (also called the *broadcast flag*) is required.</span></span> <span data-ttu-id="5a93b-119">Cet indicateur peut être combiné avec les autres indicateurs.</span><span class="sxs-lookup"><span data-stu-id="5a93b-119">This flag can be combined with the other flags.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5a93b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5a93b-120">Remarks</span></span>

<span data-ttu-id="5a93b-121">Ces indicateurs sont équivalents aux constantes d’énumération de **\_ niveau de \_ protection \_ Copp CGMSA** utilisées dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="5a93b-121">These flags are equivalent to the **COPP\_CGMSA\_Protection\_Level** enumeration constants used in the Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a93b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a93b-122">Requirements</span></span>



| <span data-ttu-id="5a93b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a93b-123">Requirement</span></span> | <span data-ttu-id="5a93b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a93b-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5a93b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a93b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5a93b-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a93b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5a93b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a93b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5a93b-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a93b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5a93b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a93b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a93b-130"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a93b-130"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a93b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a93b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a93b-132">Constantes Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a93b-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




