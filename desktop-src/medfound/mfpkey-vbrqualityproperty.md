---
description: Spécifie le niveau de qualité réel pour l’encodage VBR (variable-bit-rate) basé sur la qualité (1 passe).
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: MFPKEY_VBRQUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951658"
---
# <a name="mfpkey_vbrquality-property"></a><span data-ttu-id="ea34e-103">MFPKEY \_ propriété VBRQUALITY</span><span class="sxs-lookup"><span data-stu-id="ea34e-103">MFPKEY\_VBRQUALITY Property</span></span>

<span data-ttu-id="ea34e-104">Spécifie le niveau de qualité réel pour l’encodage VBR (variable-bit-rate) basé sur la qualité (1 passe).</span><span class="sxs-lookup"><span data-stu-id="ea34e-104">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ea34e-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ea34e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ea34e-106">g \_ wszWMVCVBRQuality, g \_ wszWMCPAudioVBRQuality</span><span class="sxs-lookup"><span data-stu-id="ea34e-106">g\_wszWMVCVBRQuality, g\_wszWMCPAudioVBRQuality</span></span>

## <a name="data-type"></a><span data-ttu-id="ea34e-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="ea34e-107">Data Type</span></span>

<span data-ttu-id="ea34e-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="ea34e-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="ea34e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ea34e-109">Remarks</span></span>

<span data-ttu-id="ea34e-110">Toutes les valeurs de la plage n’ont pas une signification unique.</span><span class="sxs-lookup"><span data-stu-id="ea34e-110">Not all of the values in the range have a unique meaning.</span></span> <span data-ttu-id="ea34e-111">Les valeurs qui représentent un pas à pas détaillé dans la qualité du niveau précédent sont les suivantes : 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97 et 100.</span><span class="sxs-lookup"><span data-stu-id="ea34e-111">The values that represent a step up in quality from the previous level are: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, and 100.</span></span>

<span data-ttu-id="ea34e-112">Pour les objets d’encodeur audio, les modes de qualité sont fournis dans la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) des types de sortie que vous récupérez à l’aide de [**IMediaObject :: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span><span class="sxs-lookup"><span data-stu-id="ea34e-112">For audio encoder objects, the quality modes are provided in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the output types that you retrieve using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea34e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea34e-113">Requirements</span></span>



| <span data-ttu-id="ea34e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea34e-114">Requirement</span></span> | <span data-ttu-id="ea34e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea34e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea34e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea34e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ea34e-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea34e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ea34e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea34e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ea34e-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea34e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ea34e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea34e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea34e-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea34e-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea34e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea34e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea34e-123">Énumération des types audio pour des modes d’encodage spécifiques</span><span class="sxs-lookup"><span data-stu-id="ea34e-123">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[<span data-ttu-id="ea34e-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea34e-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
