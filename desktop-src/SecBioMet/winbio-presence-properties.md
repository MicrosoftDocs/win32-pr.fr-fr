---
title: WINBIO_PRESENCE_PROPERTIES Union ( \_ types WINBIO. h)
description: Contient des valeurs biométriques que le Windows Biometric Framework utilisé pour déterminer qu’un individu était présent.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- API Windows Biometric Framework WINBIO_PRESENCE_PROPERTIES Union
- API Windows Biometric Framework du pointeur d’Union PWINBIO_PRESENCE_PROPERTIES
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464606"
---
# <a name="winbio_presence_properties-union"></a><span data-ttu-id="d16a0-105">WINBIO \_ Propriétés de présence de l' \_ Union</span><span class="sxs-lookup"><span data-stu-id="d16a0-105">WINBIO\_PRESENCE\_PROPERTIES union</span></span>

<span data-ttu-id="d16a0-106">Contient des valeurs biométriques que le Windows Biometric Framework utilisé pour déterminer qu’un individu était présent.</span><span class="sxs-lookup"><span data-stu-id="d16a0-106">Contains biometric values that the Windows Biometric Framework used to determine that an individual was present.</span></span>

## <a name="syntax"></a><span data-ttu-id="d16a0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d16a0-107">Syntax</span></span>


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a><span data-ttu-id="d16a0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d16a0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d16a0-109">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="d16a0-109">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="d16a0-110">Valeurs pour l’emplacement des caractéristiques du visage que le Windows Biometric Framework utilisé pour déterminer qu’un individu était présent.</span><span class="sxs-lookup"><span data-stu-id="d16a0-110">Values for the location of facial features that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="d16a0-111">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="d16a0-111">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="d16a0-112">Position dans le cadre de l’appareil photo de la personne, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d16a0-112">The position within the camera frame of the face of the individual, in pixels.</span></span> <span data-ttu-id="d16a0-113">La taille du cadre de l’appareil photo détermine la limite supérieure du nombre de pixels pour cette position.</span><span class="sxs-lookup"><span data-stu-id="d16a0-113">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="d16a0-114">Pour déterminer la taille du cadre de l’appareil photo, accédez à la propriété **WINBIO \_ étendue des \_ \_ \_ informations de capteur** .</span><span class="sxs-lookup"><span data-stu-id="d16a0-114">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="d16a0-115">Un client qui utilise le moniteur de présence doit effectuer l’opération de mise à l’échelle pour mapper la position au frame de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="d16a0-115">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame .</span></span>

</dd> <dt>

<span data-ttu-id="d16a0-116">**Distance**</span><span class="sxs-lookup"><span data-stu-id="d16a0-116">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="d16a0-117">Distance entre l’emplacement réel de la face et la distance focale idéale pour la face.</span><span class="sxs-lookup"><span data-stu-id="d16a0-117">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="d16a0-118">Cette valeur est comprise entre-100 et 100.</span><span class="sxs-lookup"><span data-stu-id="d16a0-118">This value ranges from -100 to 100.</span></span> <span data-ttu-id="d16a0-119">0 indique la distance idéale, les valeurs positives indiquent que l’emplacement réel du visage est trop éloigné, et les valeurs négatives indiquent que l’emplacement réel est trop proche.</span><span class="sxs-lookup"><span data-stu-id="d16a0-119">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d16a0-120">**IRI**</span><span class="sxs-lookup"><span data-stu-id="d16a0-120">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="d16a0-121">Valeurs de l’emplacement de l’IRIS que le Windows Biometric Framework utilisé pour déterminer qu’un individu était présent.</span><span class="sxs-lookup"><span data-stu-id="d16a0-121">Values for iris location that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="d16a0-122">**EyeBoundingBox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d16a0-122">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="d16a0-123">Position dans le cadre de l’appareil photo de l’un des Irises de l’individu à inscrire, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d16a0-123">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="d16a0-124">Si le système de reconnaissance de l’iris n’analyse qu’un œil, cette position est du diaphragme de cet oeil.</span><span class="sxs-lookup"><span data-stu-id="d16a0-124">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="d16a0-125">Si le système de reconnaissance de l’iris surveille les deux yeux, mais qu’un seul œil est dans le cadre de l’appareil photo, cette position est du diaphragme de l’oeil dans le cadre de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="d16a0-125">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="d16a0-126">Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est probablement celle du diaphragme de l’œil droit de l’individu.</span><span class="sxs-lookup"><span data-stu-id="d16a0-126">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="d16a0-127">La taille du cadre de l’appareil photo détermine la limite supérieure du nombre de pixels pour cette position.</span><span class="sxs-lookup"><span data-stu-id="d16a0-127">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="d16a0-128">Pour déterminer la taille du cadre de l’appareil photo, accédez à la propriété **WINBIO \_ étendue des \_ \_ \_ informations de capteur** .</span><span class="sxs-lookup"><span data-stu-id="d16a0-128">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="d16a0-129">Un client qui utilise le moniteur de présence doit effectuer l’opération de mise à l’échelle pour mapper la position au frame de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="d16a0-129">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="d16a0-130">**EyeBoundingBox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d16a0-130">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="d16a0-131">Position dans le cadre de l’appareil photo de l’un des Irises de l’individu à inscrire, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d16a0-131">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="d16a0-132">Si le système de reconnaissance de l’iris n’analyse qu’un œil, ou si un seul œil est présent dans le cadre de l’appareil photo, cette valeur est vide.</span><span class="sxs-lookup"><span data-stu-id="d16a0-132">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="d16a0-133">Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est probablement du diaphragme de l’œil gauche de la personne.</span><span class="sxs-lookup"><span data-stu-id="d16a0-133">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="d16a0-134">La taille du cadre de l’appareil photo détermine la limite supérieure du nombre de pixels pour cette position.</span><span class="sxs-lookup"><span data-stu-id="d16a0-134">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="d16a0-135">Pour déterminer la taille du cadre de l’appareil photo, accédez à la propriété **WINBIO \_ étendue des \_ \_ \_ informations de capteur** .</span><span class="sxs-lookup"><span data-stu-id="d16a0-135">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="d16a0-136">Un client qui utilise le moniteur de présence doit effectuer l’opération de mise à l’échelle pour mapper la position au frame de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="d16a0-136">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="d16a0-137">**PupilCenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d16a0-137">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="d16a0-138">Position du centre de l’une des pupilles de la personne à inscrire.</span><span class="sxs-lookup"><span data-stu-id="d16a0-138">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="d16a0-139">Si le système de reconnaissance de l’iris n’analyse qu’un œil, cette position est au centre de l’élève de cet oeil.</span><span class="sxs-lookup"><span data-stu-id="d16a0-139">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="d16a0-140">Si le système de reconnaissance de l’iris surveille les yeux, mais qu’un seul œil est dans le cadre de l’appareil photo, cette position est au centre de l’élève de l’oeil dans le cadre de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="d16a0-140">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="d16a0-141">Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est sans doute le centre de la pupille du droit de l’individu.</span><span class="sxs-lookup"><span data-stu-id="d16a0-141">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="d16a0-142">**PupilCenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d16a0-142">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="d16a0-143">Position du centre de l’une des pupilles de la personne à inscrire.</span><span class="sxs-lookup"><span data-stu-id="d16a0-143">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="d16a0-144">Si le système de reconnaissance de l’iris n’analyse qu’un œil, ou si un seul œil est présent dans le cadre de l’appareil photo, cette valeur est vide.</span><span class="sxs-lookup"><span data-stu-id="d16a0-144">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="d16a0-145">Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est sans doute le centre de la pupille de l’œil gauche de la personne.</span><span class="sxs-lookup"><span data-stu-id="d16a0-145">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="d16a0-146">**Distance**</span><span class="sxs-lookup"><span data-stu-id="d16a0-146">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="d16a0-147">Distance entre l’emplacement réel du diaphragme et la distance focale idéale pour le diaphragme.</span><span class="sxs-lookup"><span data-stu-id="d16a0-147">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="d16a0-148">Cette valeur est comprise entre-100 et 100.</span><span class="sxs-lookup"><span data-stu-id="d16a0-148">This value ranges from -100 to 100.</span></span> <span data-ttu-id="d16a0-149">0 indique la distance idéale, les valeurs positives indiquent que l’emplacement réel de l’iris est trop éloigné, et les valeurs négatives indiquent que l’emplacement réel est trop proche.</span><span class="sxs-lookup"><span data-stu-id="d16a0-149">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d16a0-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d16a0-150">Requirements</span></span>



| <span data-ttu-id="d16a0-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d16a0-151">Requirement</span></span> | <span data-ttu-id="d16a0-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="d16a0-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d16a0-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d16a0-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d16a0-154">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d16a0-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="d16a0-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d16a0-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d16a0-156">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d16a0-156">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="d16a0-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="d16a0-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="d16a0-158"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="d16a0-158"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





