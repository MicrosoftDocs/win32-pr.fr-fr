---
description: GUID défini par décodeur qui identifie le format de métadonnées audio spatial, en avertissant les composants en aval du type d’objet de métadonnées que le décodeur produira.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: Attribut MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203110"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a><span data-ttu-id="3f752-103">\_Attribut d' \_ \_ ID de \_ \_ format de métadonnées d’objet audio \_ spatial \_ MF</span><span class="sxs-lookup"><span data-stu-id="3f752-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_FORMAT\_ID attribute</span></span>

<span data-ttu-id="3f752-104">GUID défini par décodeur qui identifie le format de métadonnées audio spatial, en avertissant les composants en aval du type d’objet de métadonnées que le décodeur produira.</span><span class="sxs-lookup"><span data-stu-id="3f752-104">A decoder-defined GUID that identifies the spatial audio metadata format, notifying downstream components of the metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="3f752-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="3f752-105">Data type</span></span>

<span data-ttu-id="3f752-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="3f752-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="3f752-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3f752-107">Remarks</span></span>

<span data-ttu-id="3f752-108">L’objet blob de métadonnées avec le format spécifié est écrit à l’aide de l’interface [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) et lu à l’aide de l’interface [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) .</span><span class="sxs-lookup"><span data-stu-id="3f752-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="3f752-109">L’objet blob de métadonnées est opaque pour le pipeline Media Foundation et les composants.</span><span class="sxs-lookup"><span data-stu-id="3f752-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="3f752-110">L’attribut est appliqué au type de média audio spatial.</span><span class="sxs-lookup"><span data-stu-id="3f752-110">The attribute is applied to the spatial audio media type.</span></span> <span data-ttu-id="3f752-111">Si un composant en aval ne prend pas en charge le format de métadonnées spécifié par le GUID, le composant doit rejeter le type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3f752-111">If a downstream component does not support the metadata format specified by the GUID, the component should reject the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f752-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f752-112">Requirements</span></span>



| <span data-ttu-id="3f752-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f752-113">Requirement</span></span> | <span data-ttu-id="3f752-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f752-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f752-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f752-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3f752-116">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f752-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3f752-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f752-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3f752-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f752-118">None supported</span></span><br/>                                                          |
| <span data-ttu-id="3f752-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f752-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f752-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f752-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
