---
title: Structure WINBIO_EXTENDED_ENGINE_INFO ( \_ types WINBIO. h)
description: Contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EXTENDED_ENGINE_INFO
- API du pointeur de structure PWINBIO_EXTENDED_ENGINE_INFO Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844318"
---
# <a name="winbio_extended_engine_info-structure"></a><span data-ttu-id="8ffd5-105">\_Structure d' \_ informations du moteur étendu WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="8ffd5-105">WINBIO\_EXTENDED\_ENGINE\_INFO structure</span></span>

<span data-ttu-id="8ffd5-106">Contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-106">Contains information about the capabilities and enrollment requirements of the engine adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffd5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ffd5-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a><span data-ttu-id="8ffd5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8ffd5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ffd5-109">**GenericEngineCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-109">**GenericEngineCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-110">Fonctionnalités génériques du composant moteur qui est connecté à une unité biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-110">The generic capabilities of the engine component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-111">**Factor**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-112">Type d’unité biométrique pour lequel cette structure contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="8ffd5-113">Par exemple, si la valeur du membre **Factor** est **WINBIO \_ type \_ Fingerprint**, la structure **WINBIO \_ Extended \_ Engine \_ info** s’applique à un lecteur d’empreintes digitales et contient les informations pertinentes dans la structure **spécifique. Fingerprint** .</span><span class="sxs-lookup"><span data-stu-id="8ffd5-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_ENGINE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-114">**Spécifique**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-115">Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique liée à un facteur biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-115">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="8ffd5-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-117">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-117">Reserved.</span></span> <span data-ttu-id="8ffd5-118">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-120">Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique liée aux caractéristiques du visage.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-120">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="8ffd5-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-122">Reserved.</span></span> <span data-ttu-id="8ffd5-123">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-123">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-124">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-124">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ffd5-125">**Null**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-125">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-126">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-126">Reserved.</span></span> <span data-ttu-id="8ffd5-127">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-127">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="8ffd5-128">**Empreinte digitale**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-128">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-129">Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique liée aux modèles d’empreintes digitales.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-129">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="8ffd5-130">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-130">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-131">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-131">Reserved.</span></span> <span data-ttu-id="8ffd5-132">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-132">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-133">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-133">**EnrollmentRequirements**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-134">Nombre d’exemples corrects requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-134">The number of good samples required to create a new fingerprint template.</span></span>

<dl> <dt>

<span data-ttu-id="8ffd5-135">**GeneralSamples**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-135">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-136">Nombre total d’exemples corrects nécessaires à la création d’un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-136">The total number of good samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-137">**Gestionnaire**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-137">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-138">Nombre d’échantillons corrects pour le centre de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-138">The number of good samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-139">**Périphérie**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-139">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-140">Nombre d’échantillons corrects pour le bord supérieur de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-140">The number of good samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-141">**BottomEdge**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-141">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-142">Nombre d’échantillons corrects pour le bord inférieur de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-142">The number of good samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-143">**LeftEdge**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-143">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-144">Nombre d’échantillons corrects pour le bord gauche de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-144">The number of good samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-145">**RightEdge**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-145">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-146">Nombre d’échantillons corrects pour le bord droit de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-146">The number of good samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="8ffd5-147">**IRI**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-147">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-148">Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique liée aux modèles d’IRIS.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-148">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="8ffd5-149">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-149">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-150">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-150">Reserved.</span></span> <span data-ttu-id="8ffd5-151">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-151">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-152">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-152">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ffd5-153">**Null**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-153">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-154">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-154">Reserved.</span></span> <span data-ttu-id="8ffd5-155">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-155">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="8ffd5-156">**Voice**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-156">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-157">Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique liée aux modèles vocaux.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-157">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="8ffd5-158">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-158">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-159">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-159">Reserved.</span></span> <span data-ttu-id="8ffd5-160">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-160">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd5-161">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-161">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ffd5-162">**Null**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-162">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="8ffd5-163">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-163">Reserved.</span></span> <span data-ttu-id="8ffd5-164">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8ffd5-164">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ffd5-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ffd5-165">Requirements</span></span>



| <span data-ttu-id="8ffd5-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ffd5-166">Requirement</span></span> | <span data-ttu-id="8ffd5-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ffd5-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffd5-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ffd5-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8ffd5-169">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ffd5-169">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="8ffd5-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ffd5-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8ffd5-171">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ffd5-171">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="8ffd5-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ffd5-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ffd5-173"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="8ffd5-173"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ffd5-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ffd5-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ffd5-175">**\_Constantes de capacité WINBIO**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-175">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="8ffd5-176">**\_Constantes de type de biométrie WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="8ffd5-176">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> </dl>

 

 





