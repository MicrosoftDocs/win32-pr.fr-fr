---
title: Structure WINBIO_EXTENDED_STORAGE_INFO ( \_ types WINBIO. h)
description: Contient des informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EXTENDED_STORAGE_INFO
- API du pointeur de structure PWINBIO_EXTENDED_STORAGE_INFO Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941773"
---
# <a name="winbio_extended_storage_info-structure"></a><span data-ttu-id="d3f04-105">\_Structure des \_ informations de stockage étendu WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="d3f04-105">WINBIO\_EXTENDED\_STORAGE\_INFO structure</span></span>

<span data-ttu-id="d3f04-106">Contient des informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="d3f04-106">Contains information about the capabilities and enrollment requirements of the storage adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f04-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3f04-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="d3f04-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d3f04-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3f04-109">**GenericStorageCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d3f04-109">**GenericStorageCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-110">Fonctionnalités génériques du composant de stockage connecté à une unité biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="d3f04-110">The generic capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="d3f04-111">**Factor**</span><span class="sxs-lookup"><span data-stu-id="d3f04-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-112">Type d’unité biométrique pour lequel cette structure contient des informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage.</span><span class="sxs-lookup"><span data-stu-id="d3f04-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the storage adapter.</span></span> <span data-ttu-id="d3f04-113">Par exemple, si la valeur du membre **Factor** est **WINBIO \_ type \_ Fingerprint**, la structure **WINBIO \_ Extended \_ Storage \_ info** s’applique à un lecteur d’empreintes digitales et contient les informations pertinentes dans la structure **spécifique. Fingerprint** .</span><span class="sxs-lookup"><span data-stu-id="d3f04-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_STORAGE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="d3f04-114">**Spécifique**</span><span class="sxs-lookup"><span data-stu-id="d3f04-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-115">Informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique liée à un facteur biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="d3f04-115">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="d3f04-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="d3f04-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-117">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d3f04-117">Reserved.</span></span> <span data-ttu-id="d3f04-118">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d3f04-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d3f04-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="d3f04-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-120">Informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique liée aux caractéristiques du visage.</span><span class="sxs-lookup"><span data-stu-id="d3f04-120">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="d3f04-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d3f04-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-122">Fonctionnalités de reconnaissance faciale du composant de stockage connecté à une unité biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="d3f04-122">The facial recognition capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d3f04-123">**Empreinte digitale**</span><span class="sxs-lookup"><span data-stu-id="d3f04-123">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-124">Informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique liée aux modèles d’empreintes digitales.</span><span class="sxs-lookup"><span data-stu-id="d3f04-124">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="d3f04-125">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d3f04-125">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-126">Fonctionnalités de reconnaissance d’empreintes digitales du composant de stockage connecté à une unité biométrique spécifique</span><span class="sxs-lookup"><span data-stu-id="d3f04-126">The fingerprint recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d3f04-127">**IRI**</span><span class="sxs-lookup"><span data-stu-id="d3f04-127">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-128">Informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique liée aux modèles d’IRIS.</span><span class="sxs-lookup"><span data-stu-id="d3f04-128">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="d3f04-129">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d3f04-129">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-130">Fonctionnalités de reconnaissance de l’iris du composant de stockage connecté à une unité biométrique spécifique</span><span class="sxs-lookup"><span data-stu-id="d3f04-130">The iris recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d3f04-131">**Voice**</span><span class="sxs-lookup"><span data-stu-id="d3f04-131">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-132">Informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique liée aux modèles vocaux.</span><span class="sxs-lookup"><span data-stu-id="d3f04-132">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="d3f04-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d3f04-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="d3f04-134">Fonctionnalités de reconnaissance vocale du composant de stockage connecté à une unité biométrique spécifique</span><span class="sxs-lookup"><span data-stu-id="d3f04-134">The voice recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3f04-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3f04-135">Requirements</span></span>



| <span data-ttu-id="d3f04-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3f04-136">Requirement</span></span> | <span data-ttu-id="d3f04-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3f04-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f04-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3f04-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f04-139">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3f04-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="d3f04-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3f04-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f04-141">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3f04-141">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="d3f04-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3f04-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3f04-143"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f04-143"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f04-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3f04-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f04-145">**\_Constantes de type de biométrie WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="d3f04-145">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="d3f04-146">**\_Constantes de capacité WINBIO**</span><span class="sxs-lookup"><span data-stu-id="d3f04-146">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> </dl>

 

 





