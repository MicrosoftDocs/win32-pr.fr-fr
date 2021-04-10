---
title: Constantes WINBIO_OPERATION_TYPE ( \_ types WINBIO. h)
description: Spécifiez le type d’opération asynchrone en cours d’exécution.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106495"
---
# <a name="winbio_operation_type-constants"></a><span data-ttu-id="0070d-103">\_Constantes de type d’opération WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="0070d-103">WINBIO\_OPERATION\_TYPE Constants</span></span>

<span data-ttu-id="0070d-104">Les constantes suivantes peuvent être retournées par l’Windows Biometric Framework dans un [**\_ \_ Résultat asynchrone WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) pour spécifier le type d’opération asynchrone en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0070d-104">The following constants can be returned by the Windows Biometric Framework in a [**WINBIO\_ASYNC\_RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) to specify the type of asynchronous operation being performed.</span></span>

<dl> <dt>

<span data-ttu-id="0070d-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**\_opération WINBIO \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="0070d-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**WINBIO\_OPERATION\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-106">0</span><span class="sxs-lookup"><span data-stu-id="0070d-106">0</span></span>
</dt> <dt>



<span data-ttu-id="0070d-107">Aucune opération n’a été identifiée.</span><span class="sxs-lookup"><span data-stu-id="0070d-107">No operation has been identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**\_opération WINBIO \_ ouverte**</span><span class="sxs-lookup"><span data-stu-id="0070d-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**WINBIO\_OPERATION\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-109">1</span><span class="sxs-lookup"><span data-stu-id="0070d-109">1</span></span>
</dt> <dt>



<span data-ttu-id="0070d-110">Une session biométrique a été ouverte.</span><span class="sxs-lookup"><span data-stu-id="0070d-110">A biometric session was opened.</span></span> <span data-ttu-id="0070d-111">Pour plus d’informations, consultez [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span><span class="sxs-lookup"><span data-stu-id="0070d-111">For more information see [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**\_opération WINBIO \_ Close**</span><span class="sxs-lookup"><span data-stu-id="0070d-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**WINBIO\_OPERATION\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-113">2</span><span class="sxs-lookup"><span data-stu-id="0070d-113">2</span></span>
</dt> <dt>



<span data-ttu-id="0070d-114">Une session biométrique a été fermée.</span><span class="sxs-lookup"><span data-stu-id="0070d-114">A biometric session was closed.</span></span> <span data-ttu-id="0070d-115">Pour plus d’informations, consultez [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span><span class="sxs-lookup"><span data-stu-id="0070d-115">For more information, see [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**vérification de l' \_ opération WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**WINBIO\_OPERATION\_VERIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-117">3</span><span class="sxs-lookup"><span data-stu-id="0070d-117">3</span></span>
</dt> <dt>



<span data-ttu-id="0070d-118">Un échantillon biométrique a été vérifié par rapport à une identité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0070d-118">A biometric sample was verified against a user identity.</span></span> <span data-ttu-id="0070d-119">Pour plus d’informations, consultez [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span><span class="sxs-lookup"><span data-stu-id="0070d-119">For more information, see [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**identification de l' \_ opération WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO\_OPERATION\_IDENTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-121">4</span><span class="sxs-lookup"><span data-stu-id="0070d-121">4</span></span>
</dt> <dt>



<span data-ttu-id="0070d-122">Un échantillon biométrique a été capturé et comparé à un modèle existant.</span><span class="sxs-lookup"><span data-stu-id="0070d-122">A biometric sample was captured and compared to an existing template.</span></span> <span data-ttu-id="0070d-123">Pour plus d’informations, consultez [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span><span class="sxs-lookup"><span data-stu-id="0070d-123">For more information, see [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**capteur de recherche de l' \_ opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**WINBIO\_OPERATION\_LOCATE\_SENSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-125">5</span><span class="sxs-lookup"><span data-stu-id="0070d-125">5</span></span>
</dt> <dt>



<span data-ttu-id="0070d-126">Le numéro d’identification d’une unité biométrique a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="0070d-126">The ID number of a biometric unit was retrieved.</span></span> <span data-ttu-id="0070d-127">Pour plus d’informations, consultez [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span><span class="sxs-lookup"><span data-stu-id="0070d-127">For more information, see [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**début de l’inscription de l' \_ opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO\_OPERATION\_ENROLL\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-129">6</span><span class="sxs-lookup"><span data-stu-id="0070d-129">6</span></span>
</dt> <dt>



<span data-ttu-id="0070d-130">Une séquence d’inscription biométrique a été lancée.</span><span class="sxs-lookup"><span data-stu-id="0070d-130">A biometric enrollment sequence was initiated.</span></span> <span data-ttu-id="0070d-131">Pour plus d’informations, consultez [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span><span class="sxs-lookup"><span data-stu-id="0070d-131">For more information, see [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**CAPTURE d’inscription de l' \_ opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO\_OPERATION\_ENROLL\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-133">7</span><span class="sxs-lookup"><span data-stu-id="0070d-133">7</span></span>
</dt> <dt>



<span data-ttu-id="0070d-134">Un échantillon biométrique a été capturé et ajouté au modèle.</span><span class="sxs-lookup"><span data-stu-id="0070d-134">A biometric sample was captured and added to the template.</span></span> <span data-ttu-id="0070d-135">Pour plus d’informations, consultez [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span><span class="sxs-lookup"><span data-stu-id="0070d-135">For more information, see [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**validation d’inscription de l' \_ opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**WINBIO\_OPERATION\_ENROLL\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-137">8</span><span class="sxs-lookup"><span data-stu-id="0070d-137">8</span></span>
</dt> <dt>



<span data-ttu-id="0070d-138">Un modèle biométrique en attente a été finalisé.</span><span class="sxs-lookup"><span data-stu-id="0070d-138">A pending biometric template was finalized.</span></span> <span data-ttu-id="0070d-139">Pour plus d’informations, consultez [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span><span class="sxs-lookup"><span data-stu-id="0070d-139">For more information, see [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**annulation de l’inscription de l' \_ opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**WINBIO\_OPERATION\_ENROLL\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-141">9</span><span class="sxs-lookup"><span data-stu-id="0070d-141">9</span></span>
</dt> <dt>



<span data-ttu-id="0070d-142">Un modèle biométrique en attente a été ignoré.</span><span class="sxs-lookup"><span data-stu-id="0070d-142">A pending biometric template was discarded.</span></span> <span data-ttu-id="0070d-143">Pour plus d’informations, consultez [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span><span class="sxs-lookup"><span data-stu-id="0070d-143">For more information, see [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_ \_ inscriptions enum de l’opération WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**WINBIO\_OPERATION\_ENUM\_ENROLLMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-145">10</span><span class="sxs-lookup"><span data-stu-id="0070d-145">10</span></span>
</dt> <dt>



<span data-ttu-id="0070d-146">Les sous-facteurs d’un modèle donné ont été énumérés.</span><span class="sxs-lookup"><span data-stu-id="0070d-146">The sub-factors for a given template were enumerated.</span></span> <span data-ttu-id="0070d-147">Pour plus d’informations, consultez [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span><span class="sxs-lookup"><span data-stu-id="0070d-147">For more information, see [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO \_ opération \_ supprimer le \_ modèle**</span><span class="sxs-lookup"><span data-stu-id="0070d-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO\_OPERATION\_DELETE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-149">11</span><span class="sxs-lookup"><span data-stu-id="0070d-149">11</span></span>
</dt> <dt>



<span data-ttu-id="0070d-150">Un modèle biométrique a été supprimé du magasin.</span><span class="sxs-lookup"><span data-stu-id="0070d-150">A biometric template was deleted from the store.</span></span> <span data-ttu-id="0070d-151">Pour plus d’informations, consultez [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span><span class="sxs-lookup"><span data-stu-id="0070d-151">For more information, see [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**\_exemple de \_ capture d’opération WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**WINBIO\_OPERATION\_CAPTURE\_SAMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-153">12</span><span class="sxs-lookup"><span data-stu-id="0070d-153">12</span></span>
</dt> <dt>



<span data-ttu-id="0070d-154">Un échantillon biométrique a été capturé.</span><span class="sxs-lookup"><span data-stu-id="0070d-154">A biometric sample was captured.</span></span> <span data-ttu-id="0070d-155">Pour plus d’informations, consultez [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="0070d-155">For more information, see [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**propriété d’extraction de l' \_ opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**WINBIO\_OPERATION\_GET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-157">13</span><span class="sxs-lookup"><span data-stu-id="0070d-157">13</span></span>
</dt> <dt>



<span data-ttu-id="0070d-158">Une session biométrique, une unité ou une propriété de modèle a été récupérée.</span><span class="sxs-lookup"><span data-stu-id="0070d-158">A biometric session, unit, or template property was retrieved.</span></span> <span data-ttu-id="0070d-159">Pour plus d’informations, consultez [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span><span class="sxs-lookup"><span data-stu-id="0070d-159">For more information, see [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO \_ operation \_ Set, \_ propriété**</span><span class="sxs-lookup"><span data-stu-id="0070d-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO\_OPERATION\_SET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-161">14</span><span class="sxs-lookup"><span data-stu-id="0070d-161">14</span></span>
</dt> <dt>



<span data-ttu-id="0070d-162">Une session biométrique, une unité, un modèle ou une propriété de compte a été définie.</span><span class="sxs-lookup"><span data-stu-id="0070d-162">A biometric session, unit, template, or account property was set.</span></span> <span data-ttu-id="0070d-163">Pour plus d’informations, consultez [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span><span class="sxs-lookup"><span data-stu-id="0070d-163">For more information, see [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**événement d’extraction de l' \_ opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**WINBIO\_OPERATION\_GET\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-165">15</span><span class="sxs-lookup"><span data-stu-id="0070d-165">15</span></span>
</dt> <dt>



<span data-ttu-id="0070d-166">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="0070d-166">Not used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**unité de verrouillage de l' \_ opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**WINBIO\_OPERATION\_LOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-168">16</span><span class="sxs-lookup"><span data-stu-id="0070d-168">16</span></span>
</dt> <dt>



<span data-ttu-id="0070d-169">Une unité biométrique a été verrouillée pour une utilisation exclusive par une session.</span><span class="sxs-lookup"><span data-stu-id="0070d-169">A biometric unit was locked for exclusive use by a session.</span></span> <span data-ttu-id="0070d-170">Pour plus d’informations, consultez [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span><span class="sxs-lookup"><span data-stu-id="0070d-170">For more information, see [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**\_unité de \_ déverrouillage de l’opération WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**WINBIO\_OPERATION\_UNLOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-172">17</span><span class="sxs-lookup"><span data-stu-id="0070d-172">17</span></span>
</dt> <dt>



<span data-ttu-id="0070d-173">Le verrou de session sur une unité biométrique a été relâché.</span><span class="sxs-lookup"><span data-stu-id="0070d-173">The session lock on a biometric unit was released.</span></span> <span data-ttu-id="0070d-174">Pour plus d’informations, consultez [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span><span class="sxs-lookup"><span data-stu-id="0070d-174">For more information, see [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**unité de contrôle de l' \_ opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-176">18</span><span class="sxs-lookup"><span data-stu-id="0070d-176">18</span></span>
</dt> <dt>



<span data-ttu-id="0070d-177">Les opérations définies par le fournisseur ont été effectuées sur une unité de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0070d-177">Vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="0070d-178">Pour plus d’informations, consultez [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span><span class="sxs-lookup"><span data-stu-id="0070d-178">For more information, see [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**\_unité de contrôle d’opération WINBIO \_ \_ \_ privilégiée**</span><span class="sxs-lookup"><span data-stu-id="0070d-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-180">19</span><span class="sxs-lookup"><span data-stu-id="0070d-180">19</span></span>
</dt> <dt>



<span data-ttu-id="0070d-181">Les opérations définies par le fournisseur privilégié ont été effectuées sur une unité de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0070d-181">Privileged vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="0070d-182">Pour plus d’informations, consultez [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="0070d-182">For more information, see [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**\_ \_ infrastructure ouverte de l’opération WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO\_OPERATION\_OPEN\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-184">20</span><span class="sxs-lookup"><span data-stu-id="0070d-184">20</span></span>
</dt> <dt>



<span data-ttu-id="0070d-185">Un descripteur de l’infrastructure biométrique a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="0070d-185">A handle to the biometric framework was opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**Framework de fermeture de l' \_ opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO\_OPERATION\_CLOSE\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-187">21</span><span class="sxs-lookup"><span data-stu-id="0070d-187">21</span></span>
</dt> <dt>



<span data-ttu-id="0070d-188">Un descripteur de l’infrastructure biométrique a été fermé.</span><span class="sxs-lookup"><span data-stu-id="0070d-188">A handle to the biometric framework was closed.</span></span> <span data-ttu-id="0070d-189">Pour plus d’informations, consultez [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span><span class="sxs-lookup"><span data-stu-id="0070d-189">For more information, see [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_fournisseurs de \_ services d’énumération d’opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**WINBIO\_OPERATION\_ENUM\_SERVICE\_PROVIDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-191">22</span><span class="sxs-lookup"><span data-stu-id="0070d-191">22</span></span>
</dt> <dt>



<span data-ttu-id="0070d-192">Les fournisseurs de services biométriques installés ont été énumérés.</span><span class="sxs-lookup"><span data-stu-id="0070d-192">The installed biometric service providers were enumerated.</span></span> <span data-ttu-id="0070d-193">Pour plus d’informations, consultez [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span><span class="sxs-lookup"><span data-stu-id="0070d-193">For more information, see [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**\_ \_ \_ unités biométriques de l’opération WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO\_OPERATION\_ENUM\_BIOMETRIC\_UNITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-195">23</span><span class="sxs-lookup"><span data-stu-id="0070d-195">23</span></span>
</dt> <dt>



<span data-ttu-id="0070d-196">Les unités biométriques attachées ont été énumérées.</span><span class="sxs-lookup"><span data-stu-id="0070d-196">The attached biometric units were enumerated.</span></span> <span data-ttu-id="0070d-197">Pour plus d’informations, consultez [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span><span class="sxs-lookup"><span data-stu-id="0070d-197">For more information, see [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_opération WINBIO \_ énumérer les \_ bases de données**</span><span class="sxs-lookup"><span data-stu-id="0070d-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**WINBIO\_OPERATION\_ENUM\_DATABASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-199">24</span><span class="sxs-lookup"><span data-stu-id="0070d-199">24</span></span>
</dt> <dt>



<span data-ttu-id="0070d-200">Les bases de données inscrites ont été énumérées.</span><span class="sxs-lookup"><span data-stu-id="0070d-200">The registered databases were enumerated.</span></span> <span data-ttu-id="0070d-201">Pour plus d’informations, consultez [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span><span class="sxs-lookup"><span data-stu-id="0070d-201">For more information, see [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**arrivée de l' \_ unité d’opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**WINBIO\_OPERATION\_UNIT\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-203">25</span><span class="sxs-lookup"><span data-stu-id="0070d-203">25</span></span>
</dt> <dt>



<span data-ttu-id="0070d-204">Une unité biométrique a été créée.</span><span class="sxs-lookup"><span data-stu-id="0070d-204">A biometric unit was created.</span></span> <span data-ttu-id="0070d-205">Pour plus d’informations, consultez [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="0070d-205">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**suppression de l' \_ unité d’opération WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**WINBIO\_OPERATION\_UNIT\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-207">26</span><span class="sxs-lookup"><span data-stu-id="0070d-207">26</span></span>
</dt> <dt>



<span data-ttu-id="0070d-208">Une unité biométrique a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="0070d-208">A biometric unit was deleted.</span></span> <span data-ttu-id="0070d-209">Pour plus d’informations, consultez [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="0070d-209">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO \_ d' \_ identifier \_ et de \_ libérer le \_ ticket de l’opération**</span><span class="sxs-lookup"><span data-stu-id="0070d-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO\_OPERATION\_IDENTIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-211">27</span><span class="sxs-lookup"><span data-stu-id="0070d-211">27</span></span>
</dt> <dt>



<span data-ttu-id="0070d-212">Réservé.</span><span class="sxs-lookup"><span data-stu-id="0070d-212">Reserved.</span></span> <span data-ttu-id="0070d-213">Cette valeur est prise en charge à partir de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0070d-213">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**\_ \_ \_ ticket de vérification et de \_ libération de \_ l’opération WINBIO**</span><span class="sxs-lookup"><span data-stu-id="0070d-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**WINBIO\_OPERATION\_VERIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-215">28</span><span class="sxs-lookup"><span data-stu-id="0070d-215">28</span></span>
</dt> <dt>



<span data-ttu-id="0070d-216">Réservé.</span><span class="sxs-lookup"><span data-stu-id="0070d-216">Reserved.</span></span> <span data-ttu-id="0070d-217">Cette valeur est prise en charge à partir de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0070d-217">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**\_présence du \_ moniteur d’opération WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="0070d-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**WINBIO\_OPERATION\_MONITOR\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-219">29</span><span class="sxs-lookup"><span data-stu-id="0070d-219">29</span></span>
</dt> <dt>



<span data-ttu-id="0070d-220">La reconnaissance faciale ou le mécanisme de surveillance de l’IRIS a été activé.</span><span class="sxs-lookup"><span data-stu-id="0070d-220">The facial recognition or iris monitoring mechanism was turned on.</span></span> <span data-ttu-id="0070d-221">Pour plus d’informations, consultez [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span><span class="sxs-lookup"><span data-stu-id="0070d-221">For more information, see [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span></span> <span data-ttu-id="0070d-222">Cette valeur est prise en charge à partir de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0070d-222">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0070d-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**\_opération WINBIO \_ inscrire \_ Select**</span><span class="sxs-lookup"><span data-stu-id="0070d-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO\_OPERATION\_ENROLL\_SELECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0070d-224">30</span><span class="sxs-lookup"><span data-stu-id="0070d-224">30</span></span>
</dt> <dt>



<span data-ttu-id="0070d-225">Un individu d’un groupe de personnes qui sont représentées par des données dans l’exemple de mémoire tampon a été spécifié comme individu à inscrire.</span><span class="sxs-lookup"><span data-stu-id="0070d-225">An individual from a group of individuals that are represented by data in the sample buffer was specified as the individual to enroll.</span></span> <span data-ttu-id="0070d-226">Pour plus d’informations, consultez [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span><span class="sxs-lookup"><span data-stu-id="0070d-226">For more information, see [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span></span> <span data-ttu-id="0070d-227">Cette valeur est prise en charge à partir de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0070d-227">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0070d-228">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0070d-228">Requirements</span></span>



| <span data-ttu-id="0070d-229">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0070d-229">Requirement</span></span> | <span data-ttu-id="0070d-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="0070d-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0070d-231">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0070d-231">Minimum supported client</span></span><br/> | <span data-ttu-id="0070d-232">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0070d-232">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="0070d-233">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0070d-233">Minimum supported server</span></span><br/> | <span data-ttu-id="0070d-234">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0070d-234">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="0070d-235">En-tête</span><span class="sxs-lookup"><span data-stu-id="0070d-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="0070d-236"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="0070d-236"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0070d-237">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0070d-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0070d-238">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="0070d-238">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





