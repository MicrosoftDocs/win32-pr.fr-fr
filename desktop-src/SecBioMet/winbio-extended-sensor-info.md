---
title: Structure WINBIO_EXTENDED_SENSOR_INFO ( \_ types WINBIO. h)
description: Contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EXTENDED_SENSOR_INFO
- API du pointeur de structure PWINBIO_EXTENDED_SENSOR_INFO Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941774"
---
# <a name="winbio_extended_sensor_info-structure"></a><span data-ttu-id="13c7f-105">\_Structure d' \_ informations de capteur étendue WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="13c7f-105">WINBIO\_EXTENDED\_SENSOR\_INFO structure</span></span>

<span data-ttu-id="13c7f-106">Contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="13c7f-106">Contains information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c7f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13c7f-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a><span data-ttu-id="13c7f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="13c7f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="13c7f-109">**GenericSensorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="13c7f-109">**GenericSensorCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-110">Les fonctionnalités génériques du composant de capteur qui est connecté à une unité biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="13c7f-110">The generic capabilities of the sensor component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="13c7f-111">**Factor**</span><span class="sxs-lookup"><span data-stu-id="13c7f-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-112">Type d’unité biométrique pour lequel cette structure contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur.</span><span class="sxs-lookup"><span data-stu-id="13c7f-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the sensor adapter.</span></span> <span data-ttu-id="13c7f-113">Par exemple, si la valeur du membre **Factor** est **WINBIO \_ type \_ empreinte**, la structure d’informations sur le **\_ \_ capteur \_ étendu WINBIO** s’applique à un lecteur d’empreintes digitales et contient les informations pertinentes dans la structure **spécifique. Fingerprint** .</span><span class="sxs-lookup"><span data-stu-id="13c7f-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_SENSOR\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="13c7f-114">**Spécifique**</span><span class="sxs-lookup"><span data-stu-id="13c7f-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-115">Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique liée à un facteur biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="13c7f-115">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="13c7f-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="13c7f-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-117">Réservé.</span><span class="sxs-lookup"><span data-stu-id="13c7f-117">Reserved.</span></span> <span data-ttu-id="13c7f-118">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="13c7f-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="13c7f-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="13c7f-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-120">Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique liée aux caractéristiques du visage.</span><span class="sxs-lookup"><span data-stu-id="13c7f-120">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="13c7f-121">**Trame**</span><span class="sxs-lookup"><span data-stu-id="13c7f-121">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-122">Taille du cadre de l’appareil photo, indiquée sous la forme d’une longueur et d’une largeur en pixels par les membres à **droite** et en **bas** de la structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="13c7f-122">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="13c7f-123">Le point (0,0) représente l’angle supérieur gauche du frame.</span><span class="sxs-lookup"><span data-stu-id="13c7f-123">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="13c7f-124">**FrameOffset**</span><span class="sxs-lookup"><span data-stu-id="13c7f-124">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-125">Décalage du cadre de l’appareil photo de la caméra vidéo, en pixels.</span><span class="sxs-lookup"><span data-stu-id="13c7f-125">The offset of the camera frame for the face from the video camera, in pixels.</span></span> <span data-ttu-id="13c7f-126">La valeur (0, 0) indique que le cadre de l’appareil photo pour la face et la caméra vidéo se chevauchent complètement.</span><span class="sxs-lookup"><span data-stu-id="13c7f-126">A value of (0, 0) indicates that the camera frame for the face and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="13c7f-127">**MandatoryOrientation**</span><span class="sxs-lookup"><span data-stu-id="13c7f-127">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-128">Orientation par défaut de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="13c7f-128">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="13c7f-129">**Empreinte digitale**</span><span class="sxs-lookup"><span data-stu-id="13c7f-129">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-130">Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique liée aux modèles d’empreintes digitales.</span><span class="sxs-lookup"><span data-stu-id="13c7f-130">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="13c7f-131">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="13c7f-131">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-132">Réservé.</span><span class="sxs-lookup"><span data-stu-id="13c7f-132">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="13c7f-133">**IRI**</span><span class="sxs-lookup"><span data-stu-id="13c7f-133">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-134">Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique liée aux modèles d’IRIS.</span><span class="sxs-lookup"><span data-stu-id="13c7f-134">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="13c7f-135">**Trame**</span><span class="sxs-lookup"><span data-stu-id="13c7f-135">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-136">Taille du cadre de l’appareil photo, indiquée sous la forme d’une longueur et d’une largeur en pixels par les membres à **droite** et en **bas** de la structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="13c7f-136">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="13c7f-137">Le point (0,0) représente l’angle supérieur gauche du frame.</span><span class="sxs-lookup"><span data-stu-id="13c7f-137">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="13c7f-138">**FrameOffset**</span><span class="sxs-lookup"><span data-stu-id="13c7f-138">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-139">Décalage, en pixels, du cadre de l’appareil photo pour le diaphragme à partir de la caméra vidéo.</span><span class="sxs-lookup"><span data-stu-id="13c7f-139">The offset of the camera frame for the iris from the video camera, in pixels.</span></span> <span data-ttu-id="13c7f-140">La valeur (0, 0) indique que le cadre de l’appareil photo pour le diaphragme et la caméra vidéo se chevauchent complètement.</span><span class="sxs-lookup"><span data-stu-id="13c7f-140">A value of (0, 0) indicates that the camera frame for the iris and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="13c7f-141">**MandatoryOrientation**</span><span class="sxs-lookup"><span data-stu-id="13c7f-141">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-142">Orientation par défaut de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="13c7f-142">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="13c7f-143">**Voice**</span><span class="sxs-lookup"><span data-stu-id="13c7f-143">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-144">Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique liée aux modèles vocaux.</span><span class="sxs-lookup"><span data-stu-id="13c7f-144">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="13c7f-145">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="13c7f-145">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="13c7f-146">Réservé.</span><span class="sxs-lookup"><span data-stu-id="13c7f-146">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13c7f-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13c7f-147">Requirements</span></span>



| <span data-ttu-id="13c7f-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13c7f-148">Requirement</span></span> | <span data-ttu-id="13c7f-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="13c7f-149">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c7f-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13c7f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="13c7f-151">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13c7f-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="13c7f-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13c7f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="13c7f-153">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13c7f-153">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="13c7f-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="13c7f-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="13c7f-155"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="13c7f-155"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c7f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13c7f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c7f-157">**\_Constantes de capacité WINBIO**</span><span class="sxs-lookup"><span data-stu-id="13c7f-157">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="13c7f-158">**\_Constantes de type de biométrie WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="13c7f-158">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="13c7f-159">**\_Constantes d’orientation WINBIO**</span><span class="sxs-lookup"><span data-stu-id="13c7f-159">**WINBIO\_ORIENTATION Constants**</span></span>](winbio-orientation-constants.md)
</dt> </dl>

 

