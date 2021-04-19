---
description: Spécifie la géométrie du tableau du microphone pour le DSP de capture vocale.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: MFPKEY_WMAAECMA_MICARRAY_DESCPTR, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524094"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a><span data-ttu-id="57a0e-103">MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR, propriété</span><span class="sxs-lookup"><span data-stu-id="57a0e-103">MFPKEY\_WMAAECMA\_MICARRAY\_DESCPTR Property</span></span>

<span data-ttu-id="57a0e-104">Spécifie la géométrie du tableau du microphone pour le DSP de capture vocale.</span><span class="sxs-lookup"><span data-stu-id="57a0e-104">Specifies the microphone array geometry for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="57a0e-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="57a0e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="57a0e-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="57a0e-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="57a0e-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="57a0e-107">Data Type</span></span>

<span data-ttu-id="57a0e-108">\_objet BLOB VT</span><span class="sxs-lookup"><span data-stu-id="57a0e-108">VT\_BLOB</span></span>

## <a name="applies-to"></a><span data-ttu-id="57a0e-109">S'applique à</span><span class="sxs-lookup"><span data-stu-id="57a0e-109">Applies To</span></span>

-   [<span data-ttu-id="57a0e-110">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="57a0e-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="57a0e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="57a0e-111">Remarks</span></span>

<span data-ttu-id="57a0e-112">La valeur de cette propriété est une [**structure \_ \_ \_ Geometry de tableau KSAUDIO MIC**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) .</span><span class="sxs-lookup"><span data-stu-id="57a0e-112">The value of this property is a [**KSAUDIO\_MIC\_ARRAY\_GEOMETRY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) structure.</span></span> <span data-ttu-id="57a0e-113">Cette structure est définie dans le fichier d’en-tête KsMedia. h.</span><span class="sxs-lookup"><span data-stu-id="57a0e-113">This structure is defined in the header file KsMedia.h.</span></span> <span data-ttu-id="57a0e-114">Pour obtenir la géométrie du tableau du microphone, interrogez le périphérique audio pour la \_ \_ \_ propriété Geometry du tableau MIC audio KSPROPERTY \_ en appelant la méthode **IKsControl :: KSPROPERTY** sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="57a0e-114">To get the microphone array geometry, query the audio device for the KSPROPERTY\_AUDIO\_MIC\_ARRAY\_GEOMETRY property by calling the **IKsControl::KSProperty** method on the device.</span></span> <span data-ttu-id="57a0e-115">Pour plus d’informations sur les tableaux de microphones, téléchargez le livre blanc [comment créer et utiliser des tableaux de microphone pour Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span><span class="sxs-lookup"><span data-stu-id="57a0e-115">For more information on microphone arrays, download the white paper [How to Build and Use Microphone Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span></span>

<span data-ttu-id="57a0e-116">Définissez cette propriété si vous utilisez le DSP en mode filtre et si le traitement du tableau du microphone est activé.</span><span class="sxs-lookup"><span data-stu-id="57a0e-116">Set this property if you are using the DSP in filter mode and microphone array processing is enabled.</span></span> <span data-ttu-id="57a0e-117">Si vous utilisez le DSP en mode Source, le DSP interroge automatiquement l’appareil pour obtenir les informations géométriques.</span><span class="sxs-lookup"><span data-stu-id="57a0e-117">If you are using the DSP in source mode, the DSP automatically queries the device for the geometry information.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a0e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57a0e-118">Requirements</span></span>



| <span data-ttu-id="57a0e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57a0e-119">Requirement</span></span> | <span data-ttu-id="57a0e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="57a0e-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57a0e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57a0e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57a0e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57a0e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="57a0e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57a0e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57a0e-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57a0e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57a0e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="57a0e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a0e-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="57a0e-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a0e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57a0e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a0e-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="57a0e-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="57a0e-129">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="57a0e-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
