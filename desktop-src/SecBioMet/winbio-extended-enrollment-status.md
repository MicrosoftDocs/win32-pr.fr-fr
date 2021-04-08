---
title: Structure WINBIO_EXTENDED_ENROLLMENT_STATUS ( \_ types WINBIO. h)
description: Contient des informations supplémentaires sur l’état d’une inscription en cours.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EXTENDED_ENROLLMENT_STATUS
- API du pointeur de structure PWINBIO_EXTENDED_ENROLLMENT_STATUS Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103113"
---
# <a name="winbio_extended_enrollment_status-structure"></a><span data-ttu-id="ce60d-105">WINBIO \_ \_ structure d’état d’inscription étendue \_</span><span class="sxs-lookup"><span data-stu-id="ce60d-105">WINBIO\_EXTENDED\_ENROLLMENT\_STATUS structure</span></span>

<span data-ttu-id="ce60d-106">Contient des informations supplémentaires sur l’état d’une inscription en cours.</span><span class="sxs-lookup"><span data-stu-id="ce60d-106">Contains additional information about the status of an enrollment that is in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce60d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce60d-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="ce60d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ce60d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce60d-109">**TemplateStatus**</span><span class="sxs-lookup"><span data-stu-id="ce60d-109">**TemplateStatus**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-110">État de l’exemple de collection pour le modèle d’inscription.</span><span class="sxs-lookup"><span data-stu-id="ce60d-110">The status of sample collection for the enrollment template.</span></span> <span data-ttu-id="ce60d-111">Les valeurs suivantes sont possibles pour ce membre.</span><span class="sxs-lookup"><span data-stu-id="ce60d-111">The following values are possible for this member.</span></span>



| <span data-ttu-id="ce60d-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce60d-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="ce60d-113">Signification</span><span class="sxs-lookup"><span data-stu-id="ce60d-113">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="ce60d-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ce60d-114"><dt>**S\_OK**</dt></span></span> </dl>                                                                     | <span data-ttu-id="ce60d-115">L’inscription est prête à être enregistrée.</span><span class="sxs-lookup"><span data-stu-id="ce60d-115">The enrollment is ready to be saved.</span></span><br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <span data-ttu-id="ce60d-116"><dt>**WINBIO \_ E \_ opération non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce60d-116"><dt>**WINBIO\_E\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ce60d-117">Aucune inscription n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="ce60d-117">No enrollment is in progress.</span></span><br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <span data-ttu-id="ce60d-118"><dt>**WINBIO \_ d' \_ autres \_ données**</dt></span><span class="sxs-lookup"><span data-stu-id="ce60d-118"><dt>**WINBIO\_I\_MORE\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="ce60d-119">D’autres exemples sont requis pour terminer le modèle.</span><span class="sxs-lookup"><span data-stu-id="ce60d-119">More samples are required to complete the template.</span></span><br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <span data-ttu-id="ce60d-120"><dt>**WINBIO \_ E \_ mauvaise \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="ce60d-120"><dt>**WINBIO\_E\_BAD\_CAPTURE**</dt></span></span> </dl>                   | <span data-ttu-id="ce60d-121">L’exemple le plus récent n’est pas utilisable.</span><span class="sxs-lookup"><span data-stu-id="ce60d-121">The most recent sample is not usable.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="ce60d-122">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="ce60d-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-123">La raison pour laquelle l’exemple le plus récent est inutilisable, si la valeur du membre **TemplateStatus** est **WINBIO \_ E \_ Bad \_ capture**.</span><span class="sxs-lookup"><span data-stu-id="ce60d-123">The reason that the most recent sample is unusable, if the value of the **TemplateStatus** member is **WINBIO\_E\_BAD\_CAPTURE**.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-124">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="ce60d-124">**PercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-125">Meilleure estimation de l’adaptateur de moteur pour le pourcentage du modèle complet, en tant que valeur comprise entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="ce60d-125">The best estimate from the engine adapter for the percentage of the template that is complete, as a value from 0 to 100.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-126">**Factor**</span><span class="sxs-lookup"><span data-stu-id="ce60d-126">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-127">Type d’unité biométrique pour lequel cette structure contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur.</span><span class="sxs-lookup"><span data-stu-id="ce60d-127">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="ce60d-128">Par exemple, si la valeur du membre **Factor** est **WINBIO \_ type \_ Fingerprint**, la structure [**WINBIO \_ Extended \_ Engine \_ info**](winbio-extended-engine-info.md) s’applique à un lecteur d’empreintes digitales et contient les informations pertinentes dans la structure **spécifique. Fingerprint** .</span><span class="sxs-lookup"><span data-stu-id="ce60d-128">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-129">**Sous-fait**</span><span class="sxs-lookup"><span data-stu-id="ce60d-129">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-130">Valeur **de \_ sous- \_ type biométrique WINBIO** qui fournit des informations supplémentaires sur l’inscription.</span><span class="sxs-lookup"><span data-stu-id="ce60d-130">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that provides additional information about the enrollment.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-131">**Spécifique**</span><span class="sxs-lookup"><span data-stu-id="ce60d-131">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-132">Informations sur l’état d’une inscription en cours pour un facteur biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="ce60d-132">Information about the status of an enrollment that is in progress for a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="ce60d-133">**Null**</span><span class="sxs-lookup"><span data-stu-id="ce60d-133">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-134">Réservé.</span><span class="sxs-lookup"><span data-stu-id="ce60d-134">Reserved.</span></span> <span data-ttu-id="ce60d-135">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ce60d-135">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-136">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="ce60d-136">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-137">Informations sur l’état d’une inscription en cours pour les caractéristiques du visage.</span><span class="sxs-lookup"><span data-stu-id="ce60d-137">Information about the status of an enrollment that is in progress for facial features.</span></span>

<dl> <dt>

<span data-ttu-id="ce60d-138">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="ce60d-138">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-139">Position dans le cadre de l’appareil photo de la personne à inscrire, en pixels.</span><span class="sxs-lookup"><span data-stu-id="ce60d-139">The position within the camera frame of the face of the individual to enroll, in pixels.</span></span> <span data-ttu-id="ce60d-140">La taille du cadre de l’appareil photo détermine la limite supérieure du nombre de pixels pour cette position.</span><span class="sxs-lookup"><span data-stu-id="ce60d-140">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="ce60d-141">Pour déterminer la taille du cadre de l’appareil photo, accédez à la propriété **WINBIO \_ étendue des \_ \_ \_ informations de capteur** .</span><span class="sxs-lookup"><span data-stu-id="ce60d-141">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="ce60d-142">Un client qui utilise le moniteur de présence doit effectuer l’opération de mise à l’échelle pour mapper la position au frame de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="ce60d-142">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-143">**Distance**</span><span class="sxs-lookup"><span data-stu-id="ce60d-143">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-144">Distance entre l’emplacement réel de la face et la distance focale idéale pour la face.</span><span class="sxs-lookup"><span data-stu-id="ce60d-144">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="ce60d-145">Cette valeur est comprise entre-100 et 100.</span><span class="sxs-lookup"><span data-stu-id="ce60d-145">This value ranges from -100 to 100.</span></span> <span data-ttu-id="ce60d-146">0 indique la distance idéale, les valeurs positives indiquent que l’emplacement réel du visage est trop éloigné, et les valeurs négatives indiquent que l’emplacement réel est trop proche.</span><span class="sxs-lookup"><span data-stu-id="ce60d-146">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ce60d-147">**Empreinte digitale**</span><span class="sxs-lookup"><span data-stu-id="ce60d-147">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-148">Informations sur l’état d’une inscription en cours pour les modèles d’empreintes digitales.</span><span class="sxs-lookup"><span data-stu-id="ce60d-148">Information about the status of an enrollment that is in progress for fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="ce60d-149">**GeneralSamples**</span><span class="sxs-lookup"><span data-stu-id="ce60d-149">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-150">Nombre total d’échantillons requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="ce60d-150">The total number of samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-151">**Gestionnaire**</span><span class="sxs-lookup"><span data-stu-id="ce60d-151">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-152">Nombre d’échantillons pour le centre de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="ce60d-152">The number of samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-153">**Périphérie**</span><span class="sxs-lookup"><span data-stu-id="ce60d-153">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-154">Nombre d’échantillons pour le bord supérieur de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="ce60d-154">The number of samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-155">**BottomEdge**</span><span class="sxs-lookup"><span data-stu-id="ce60d-155">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-156">Nombre d’échantillons pour le bord inférieur de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="ce60d-156">The number of samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-157">**LeftEdge**</span><span class="sxs-lookup"><span data-stu-id="ce60d-157">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-158">Nombre d’échantillons pour le bord gauche de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="ce60d-158">The number of samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-159">**RightEdge**</span><span class="sxs-lookup"><span data-stu-id="ce60d-159">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-160">Nombre d’échantillons pour le bord droit de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="ce60d-160">The number of samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ce60d-161">**IRI**</span><span class="sxs-lookup"><span data-stu-id="ce60d-161">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-162">Informations sur l’état d’une inscription en cours pour les modèles d’IRIS.</span><span class="sxs-lookup"><span data-stu-id="ce60d-162">Information about the status of an enrollment that is in progress for iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="ce60d-163">**EyeBoundingBox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ce60d-163">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-164">Position dans le cadre de l’appareil photo de l’un des Irises de l’individu à inscrire, en pixels.</span><span class="sxs-lookup"><span data-stu-id="ce60d-164">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="ce60d-165">Si le système de reconnaissance de l’iris n’analyse qu’un œil, cette position est du diaphragme de cet oeil.</span><span class="sxs-lookup"><span data-stu-id="ce60d-165">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="ce60d-166">Si le système de reconnaissance de l’iris surveille les deux yeux, mais qu’un seul œil est dans le cadre de l’appareil photo, cette position est du diaphragme de l’oeil dans le cadre de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="ce60d-166">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="ce60d-167">Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est probablement celle du diaphragme de l’œil droit de l’individu.</span><span class="sxs-lookup"><span data-stu-id="ce60d-167">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="ce60d-168">La taille du cadre de l’appareil photo détermine la limite supérieure du nombre de pixels pour cette position.</span><span class="sxs-lookup"><span data-stu-id="ce60d-168">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="ce60d-169">Pour déterminer la taille du cadre de l’appareil photo, accédez à la propriété **WINBIO \_ étendue des \_ \_ \_ informations de capteur** .</span><span class="sxs-lookup"><span data-stu-id="ce60d-169">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="ce60d-170">Un client qui utilise le moniteur de présence doit effectuer l’opération de mise à l’échelle pour mapper la position au frame de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="ce60d-170">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-171">**EyeBoundingBox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ce60d-171">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-172">Position dans le cadre de l’appareil photo de l’un des Irises de l’individu à inscrire, en pixels.</span><span class="sxs-lookup"><span data-stu-id="ce60d-172">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="ce60d-173">Si le système de reconnaissance de l’iris n’analyse qu’un œil, ou si un seul œil est présent dans le cadre de l’appareil photo, cette valeur est vide.</span><span class="sxs-lookup"><span data-stu-id="ce60d-173">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="ce60d-174">Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est probablement du diaphragme de l’œil gauche de la personne.</span><span class="sxs-lookup"><span data-stu-id="ce60d-174">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="ce60d-175">La taille du cadre de l’appareil photo détermine la limite supérieure du nombre de pixels pour cette position.</span><span class="sxs-lookup"><span data-stu-id="ce60d-175">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="ce60d-176">Pour déterminer la taille du cadre de l’appareil photo, accédez à la propriété **WINBIO \_ étendue des \_ \_ \_ informations de capteur** .</span><span class="sxs-lookup"><span data-stu-id="ce60d-176">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="ce60d-177">Un client qui utilise le moniteur de présence doit effectuer l’opération de mise à l’échelle pour mapper la position au frame de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="ce60d-177">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-178">**PupilCenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ce60d-178">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-179">Position du centre de l’une des pupilles de la personne à inscrire.</span><span class="sxs-lookup"><span data-stu-id="ce60d-179">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="ce60d-180">Si le système de reconnaissance de l’iris n’analyse qu’un œil, cette position est au centre de l’élève de cet oeil.</span><span class="sxs-lookup"><span data-stu-id="ce60d-180">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="ce60d-181">Si le système de reconnaissance de l’iris surveille les yeux, mais qu’un seul œil est dans le cadre de l’appareil photo, cette position est au centre de l’élève de l’oeil dans le cadre de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="ce60d-181">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="ce60d-182">Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est sans doute le centre de la pupille du droit de l’individu.</span><span class="sxs-lookup"><span data-stu-id="ce60d-182">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-183">**PupilCenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ce60d-183">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-184">Position du centre de l’une des pupilles de la personne à inscrire.</span><span class="sxs-lookup"><span data-stu-id="ce60d-184">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="ce60d-185">Si le système de reconnaissance de l’iris n’analyse qu’un œil, ou si un seul œil est présent dans le cadre de l’appareil photo, cette valeur est vide.</span><span class="sxs-lookup"><span data-stu-id="ce60d-185">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="ce60d-186">Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est sans doute le centre de la pupille de l’œil gauche de la personne.</span><span class="sxs-lookup"><span data-stu-id="ce60d-186">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="ce60d-187">**Distance**</span><span class="sxs-lookup"><span data-stu-id="ce60d-187">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-188">Distance entre l’emplacement réel du diaphragme et la distance focale idéale pour le diaphragme.</span><span class="sxs-lookup"><span data-stu-id="ce60d-188">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="ce60d-189">Cette valeur est comprise entre-100 et 100.</span><span class="sxs-lookup"><span data-stu-id="ce60d-189">This value ranges from -100 to 100.</span></span> <span data-ttu-id="ce60d-190">0 indique la distance idéale, les valeurs positives indiquent que l’emplacement réel de l’iris est trop éloigné, et les valeurs négatives indiquent que l’emplacement réel est trop proche.</span><span class="sxs-lookup"><span data-stu-id="ce60d-190">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ce60d-191">**Voice**</span><span class="sxs-lookup"><span data-stu-id="ce60d-191">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-192">Informations sur l’état d’une inscription en cours pour les modèles vocaux.</span><span class="sxs-lookup"><span data-stu-id="ce60d-192">Information about the status of an enrollment that is in progress for voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="ce60d-193">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="ce60d-193">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="ce60d-194">Réservé.</span><span class="sxs-lookup"><span data-stu-id="ce60d-194">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce60d-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce60d-195">Requirements</span></span>



| <span data-ttu-id="ce60d-196">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce60d-196">Requirement</span></span> | <span data-ttu-id="ce60d-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce60d-197">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce60d-198">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce60d-198">Minimum supported client</span></span><br/> | <span data-ttu-id="ce60d-199">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce60d-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="ce60d-200">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce60d-200">Minimum supported server</span></span><br/> | <span data-ttu-id="ce60d-201">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce60d-201">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="ce60d-202">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce60d-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce60d-203"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="ce60d-203"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





