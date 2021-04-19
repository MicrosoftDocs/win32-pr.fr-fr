---
description: Spécifie le nombre maximal d’objets audio dynamiques qui peuvent être rendus par le point de terminaison audio simulataneously.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: Attribut MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518721"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a><span data-ttu-id="2febe-103">\_ \_ \_ \_ \_ Attribut objets dynamiques Max audio spatial \_ MF</span><span class="sxs-lookup"><span data-stu-id="2febe-103">MF\_MT\_SPATIAL\_AUDIO\_MAX\_DYNAMIC\_OBJECTS attribute</span></span>

<span data-ttu-id="2febe-104">Spécifie le nombre maximal d’objets audio dynamiques qui peuvent être rendus par le point de terminaison audio simulataneously.</span><span class="sxs-lookup"><span data-stu-id="2febe-104">Specifies the maximum number of dynamic audio objects that can be rendered by the audio endpoint simulataneously.</span></span>

## <a name="data-type"></a><span data-ttu-id="2febe-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2febe-105">Data type</span></span>

<span data-ttu-id="2febe-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2febe-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2febe-107">Notes</span><span class="sxs-lookup"><span data-stu-id="2febe-107">Remarks</span></span>

<span data-ttu-id="2febe-108">Un [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) peut contenir moins d’échantillons que le nombre spécifié par cet attribut.</span><span class="sxs-lookup"><span data-stu-id="2febe-108">An [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) may contain fewer samples than the number specified by this attribute.</span></span> <span data-ttu-id="2febe-109">Si un exemple contient plus d’objets audio que ce qui est spécifié par cet attribut, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="2febe-109">If a sample contains more audio objects than specified by this attribute, the behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="2febe-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2febe-110">Requirements</span></span>



| <span data-ttu-id="2febe-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2febe-111">Requirement</span></span> | <span data-ttu-id="2febe-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="2febe-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2febe-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2febe-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2febe-114">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2febe-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2febe-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2febe-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2febe-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2febe-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="2febe-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="2febe-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2febe-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2febe-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




