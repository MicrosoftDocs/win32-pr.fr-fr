---
description: Valeur spécifiant la taille, en octets, du type d’objet de métadonnées audio spatiales que le décodeur produira.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: Attribut MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2cd0b3cab788dbc724ab896d2cbfeb0d42f633f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203109"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a><span data-ttu-id="936dd-103">\_Attribut de \_ \_ longueur des \_ métadonnées de l’objet audio spatial \_ \_ MF</span><span class="sxs-lookup"><span data-stu-id="936dd-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_LENGTH attribute</span></span>

<span data-ttu-id="936dd-104">Valeur spécifiant la taille, en octets, du type d’objet de métadonnées audio spatiales que le décodeur produira.</span><span class="sxs-lookup"><span data-stu-id="936dd-104">A value specifying the size, in bytes, of the spatial audio metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="936dd-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="936dd-105">Data type</span></span>

<span data-ttu-id="936dd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="936dd-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="936dd-107">Notes</span><span class="sxs-lookup"><span data-stu-id="936dd-107">Remarks</span></span>

<span data-ttu-id="936dd-108">L’objet blob de métadonnées avec le format spécifié est écrit à l’aide de l’interface [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) et lu à l’aide de l’interface [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) .</span><span class="sxs-lookup"><span data-stu-id="936dd-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="936dd-109">L’objet blob de métadonnées est opaque pour le pipeline Media Foundation et les composants.</span><span class="sxs-lookup"><span data-stu-id="936dd-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="936dd-110">L’attribut est appliqué au type de média audio spatial.</span><span class="sxs-lookup"><span data-stu-id="936dd-110">The attribute is applied to the spatial audio media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="936dd-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="936dd-111">Requirements</span></span>



| <span data-ttu-id="936dd-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="936dd-112">Requirement</span></span> | <span data-ttu-id="936dd-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="936dd-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="936dd-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="936dd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="936dd-115">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="936dd-115">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="936dd-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="936dd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="936dd-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="936dd-117">None supported</span></span><br/>                                                          |
| <span data-ttu-id="936dd-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="936dd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="936dd-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="936dd-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
