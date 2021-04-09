---
title: Constantes WINBIO_BIR_PURPOSE ( \_ types WINBIO. h)
description: Spécifiez l’objectif pour lequel l’enregistrement d’informations biométriques (BIR) est prévu ou pour lequel il convient.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942184"
---
# <a name="winbio_bir_purpose-constants"></a><span data-ttu-id="937a7-103">\_ \_ Constantes WINBIO Bir Purpose</span><span class="sxs-lookup"><span data-stu-id="937a7-103">WINBIO\_BIR\_PURPOSE Constants</span></span>

<span data-ttu-id="937a7-104">Les indicateurs suivants sont utilisés par le membre **Purpose** de la structure d' [**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md) pour spécifier l’objectif pour lequel l’enregistrement d’informations biométriques (Bir) est destiné ou pour lequel il convient.</span><span class="sxs-lookup"><span data-stu-id="937a7-104">The following flags are used by the **Purpose** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the purpose for which the biometric information record (BIR) is intended or for which it is suitable.</span></span>



| <span data-ttu-id="937a7-105">Constante</span><span class="sxs-lookup"><span data-stu-id="937a7-105">Constant</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="937a7-106">Description</span><span class="sxs-lookup"><span data-stu-id="937a7-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <span data-ttu-id="937a7-107"><dt>**WINBIO \_ aucun \_ objet \_ disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="937a7-107"><dt>**WINBIO\_NO\_PURPOSE\_AVAILABLE**</dt></span></span> </dl>                                         | <span data-ttu-id="937a7-108">Aucun objet n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="937a7-108">No purpose is specified.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <span data-ttu-id="937a7-109"><dt>**vérification de l' \_ objectif WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="937a7-109"><dt>**WINBIO\_PURPOSE\_VERIFY**</dt></span></span> </dl>                                                            | <span data-ttu-id="937a7-110">Vérifiez l’identité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="937a7-110">Verify the identity of a user.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <span data-ttu-id="937a7-111"><dt>**identification de l’objectif de WINBIO \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="937a7-111"><dt>**WINBIO\_PURPOSE\_IDENTIFY**</dt></span></span> </dl>                                                      | <span data-ttu-id="937a7-112">Identifiez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="937a7-112">Identify a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <span data-ttu-id="937a7-113"><dt>**inscription à l’objectif de WINBIO \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="937a7-113"><dt>**WINBIO\_PURPOSE\_ENROLL**</dt></span></span> </dl>                                                            | <span data-ttu-id="937a7-114">Inscrire un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="937a7-114">Enroll a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <span data-ttu-id="937a7-115"><dt>**\_inscription de l’objectif WINBIO \_ pour la \_ \_ vérification**</dt></span><span class="sxs-lookup"><span data-stu-id="937a7-115"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION**</dt></span></span> </dl>       | <span data-ttu-id="937a7-116">Capturez un échantillon biométrique et déterminez si l’échantillon correspond à l’identité de l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="937a7-116">Capture a biometric sample and determine whether the sample corresponds to the specified user identity.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <span data-ttu-id="937a7-117"><dt>**\_inscription de l’objectif WINBIO \_ pour l' \_ \_ identification**</dt></span><span class="sxs-lookup"><span data-stu-id="937a7-117"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION**</dt></span></span> </dl> | <span data-ttu-id="937a7-118">Capturez un échantillon biométrique et déterminez s’il correspond à un modèle biométrique existant.</span><span class="sxs-lookup"><span data-stu-id="937a7-118">Capture a biometric sample and determine whether it matches an existing biometric template.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <span data-ttu-id="937a7-119"><dt>**\_ \_ audit d’objectif WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="937a7-119"><dt>**WINBIO\_PURPOSE\_AUDIT**</dt></span></span> </dl>                                                               | <span data-ttu-id="937a7-120">Informations supplémentaires qui peuvent être utilisées pour la journalisation ou l’affichage.</span><span class="sxs-lookup"><span data-stu-id="937a7-120">Extra information that can be used for logging or for display.</span></span> <span data-ttu-id="937a7-121">Cette valeur est ignorée à l’entrée par toutes les fonctions.</span><span class="sxs-lookup"><span data-stu-id="937a7-121">This value is ignored on input by all functions.</span></span> <span data-ttu-id="937a7-122">À la sortie, elle est disponible uniquement si elle est prise en charge par l’unité biométrique et que vous spécifiez **WINBIO \_ Data \_ Flag \_ RAW** dans le paramètre *Flags* de la fonction [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) .</span><span class="sxs-lookup"><span data-stu-id="937a7-122">On output, it will only be available if supported by the biometric unit and you specify **WINBIO\_DATA\_FLAG\_RAW** in the *Flags* parameter of the [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) function.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="937a7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="937a7-123">Requirements</span></span>



| <span data-ttu-id="937a7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="937a7-124">Requirement</span></span> | <span data-ttu-id="937a7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="937a7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="937a7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="937a7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="937a7-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="937a7-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="937a7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="937a7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="937a7-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="937a7-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="937a7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="937a7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="937a7-131"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="937a7-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="937a7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="937a7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="937a7-133">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="937a7-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="937a7-134">**\_ \_ en-tête Bir WINBIO**</span><span class="sxs-lookup"><span data-stu-id="937a7-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





