---
description: Les \_ \_ constantes audio spatiale xxx définissent les valeurs relatives aux fonctions de son spatial.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: Constantes SPATIAL_AUDIO_XXX (SpatialAudioMetadata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541303"
---
# <a name="spatial_audio_xxx-constants"></a><span data-ttu-id="220f8-103">\_ \_ Constantes audio spatiale xxx</span><span class="sxs-lookup"><span data-stu-id="220f8-103">SPATIAL\_AUDIO\_XXX Constants</span></span>

<span data-ttu-id="220f8-104">Les \_ \_ constantes audio spatiale xxx définissent les valeurs relatives aux fonctions de son spatial.</span><span class="sxs-lookup"><span data-stu-id="220f8-104">The SPATIAL\_AUDIO\_XXX constants define values related to spatial sound features.</span></span>



| <span data-ttu-id="220f8-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="220f8-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="220f8-106">Description</span><span class="sxs-lookup"><span data-stu-id="220f8-106">Description</span></span>                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <span data-ttu-id="220f8-107"><dt>**Spatial \_ \_Position AUDIO**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="220f8-107"><dt>**SPATIAL\_AUDIO\_POSITION**</dt> <dt>200</dt></span></span> </dl>                                                   | <span data-ttu-id="220f8-108">Commande de métadonnées audio spatiales standard définie par Microsoft qui représente la position de l’écouteur dans le modèle standard utilisé par [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) où l’en-tête de l’écouteur est positionné au niveau des coordonnées (0, 0, 0), défini en mètres.</span><span class="sxs-lookup"><span data-stu-id="220f8-108">A standard Microsoft-defined spatial audio metadata command which represents the listener position in the standard model used by [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) where the listener's head is position at coordinates (0,0,0), defined in meters.</span></span><br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <span data-ttu-id="220f8-109"><dt>**Spatial \_ \_Nombre d' \_ octets \_ de position audio**</dt> <dt>sizeof (float) \* 3</dt></span><span class="sxs-lookup"><span data-stu-id="220f8-109"><dt>**SPATIAL\_AUDIO\_POSITION\_BYTE\_COUNT**</dt> <dt>sizeof(float) \* 3</dt></span></span> </dl> | <span data-ttu-id="220f8-110">Spécifie la taille de la valeur de **\_ \_ position audio spatiale** .</span><span class="sxs-lookup"><span data-stu-id="220f8-110">Specifies the size of the **SPATIAL\_AUDIO\_POSITION** value.</span></span><br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <span data-ttu-id="220f8-111"><dt>**Spatial \_ \_Commandes audio \_ STANDARD \_ Start**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="220f8-111"><dt>**SPATIAL\_AUDIO\_STANDARD\_COMMANDS\_START**</dt> <dt>200</dt></span></span> </dl>    | <span data-ttu-id="220f8-112">Spécifie le début de la plage de commandes de métadonnées audio spatiales réservées par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="220f8-112">Specifies the start of the range of Microsoft-reserved spatial audio metadata commands.</span></span> <span data-ttu-id="220f8-113">Les commandes de métadonnées personnalisées sont limitées à l’ID de commande 0-199.</span><span class="sxs-lookup"><span data-stu-id="220f8-113">Custom metadata commands are restricted to command IDs 0 - 199.</span></span> <span data-ttu-id="220f8-114">Les commandes 200 à 255 sont réservées à une utilisation par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="220f8-114">Commands 200 - 255 are reserved for Microsoft use.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="220f8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="220f8-115">Requirements</span></span>



| <span data-ttu-id="220f8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="220f8-116">Requirement</span></span> | <span data-ttu-id="220f8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="220f8-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="220f8-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="220f8-118">Header</span></span><br/> | <dl> <span data-ttu-id="220f8-119"><dt>SpatialAudioMetadata. h</dt></span><span class="sxs-lookup"><span data-stu-id="220f8-119"><dt>SpatialAudioMetadata.h</dt></span></span> </dl> |



 

 




