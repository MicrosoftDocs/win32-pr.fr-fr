---
description: Spécifie si le fournisseur de captures vocales stocke les statistiques de datage dans le registre.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: MFPKEY_WMAAECMA_RETRIEVE_TS_STATS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533783"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a><span data-ttu-id="f15da-103">MFPKEY \_ WMAAECMA \_ récupérer \_ les \_ statistiques TS, propriété</span><span class="sxs-lookup"><span data-stu-id="f15da-103">MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS Property</span></span>

<span data-ttu-id="f15da-104">Spécifie si le fournisseur de captures vocales stocke les statistiques de datage dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f15da-104">Specifies whether the Voice Capture DSP stores time stamp statistics in the registry.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f15da-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f15da-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f15da-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f15da-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f15da-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="f15da-107">Data Type</span></span>

<span data-ttu-id="f15da-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="f15da-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="f15da-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f15da-109">Default Value</span></span>

<span data-ttu-id="f15da-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="f15da-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="f15da-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="f15da-111">Applies To</span></span>

-   [<span data-ttu-id="f15da-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="f15da-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="f15da-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f15da-113">Remarks</span></span>

<span data-ttu-id="f15da-114">Les algorithmes d’annulation de l’écho acoustique (AEC) dépendent des horodatages précis des flux audio.</span><span class="sxs-lookup"><span data-stu-id="f15da-114">Acoustic echo cancellation (AEC) algorithms depend on accurate time stamps on the audio streams.</span></span> <span data-ttu-id="f15da-115">En réalité, les horodatages sont souvent imparfaits, et différents périphériques audio peuvent présenter des taux de variance et de dérive différents.</span><span class="sxs-lookup"><span data-stu-id="f15da-115">In reality, time stamps are often imperfect, and different audio devices can exhibit different rates of variance and drift.</span></span> <span data-ttu-id="f15da-116">Lorsque l’AEC est activé, le DSP collecte des statistiques sur les horodatages et utilise ces informations pour compenser les imprécisions.</span><span class="sxs-lookup"><span data-stu-id="f15da-116">When AEC is enabled, the DSP collects statistics about the time stamps and uses this information to compensate for inaccuracies.</span></span>

<span data-ttu-id="f15da-117">Si la valeur de cette propriété est \_ true, le DSP enregistre les statistiques qu’il collecte dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f15da-117">If the value of this property is VARIANT\_TRUE, the DSP saves the statistics that it collects in the registry.</span></span> <span data-ttu-id="f15da-118">La prochaine fois que le DSP effectue l’AEC à l’aide de la même paire de périphériques audio, il lit les informations statistiques du Registre, ce qui permet au DSP de s’exécuter plus efficacement.</span><span class="sxs-lookup"><span data-stu-id="f15da-118">The next time the DSP performs AEC using the same pair of audio devices, it reads the statistical information from the registry, which enables the DSP to perform more efficiently.</span></span>

<span data-ttu-id="f15da-119">Si vous affectez à cette propriété la valeur VARIANT \_ true et que vous utilisez le DSP en mode filtre, vous devez également définir la propriété [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="f15da-119">If you set the value of this property to VARIANT\_TRUE and you are using the DSP in filter mode, you should also set the [MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) property.</span></span> <span data-ttu-id="f15da-120">En mode Source, ce n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f15da-120">In source mode, this is not required.</span></span>

<span data-ttu-id="f15da-121">La valeur par défaut de cette propriété est \_ false false.</span><span class="sxs-lookup"><span data-stu-id="f15da-121">The default value of this property is VARIANT\_FALSE.</span></span> <span data-ttu-id="f15da-122">Le DSP utilise cette propriété uniquement lorsque le traitement AEC est activé.</span><span class="sxs-lookup"><span data-stu-id="f15da-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="f15da-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f15da-123">Requirements</span></span>



| <span data-ttu-id="f15da-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f15da-124">Requirement</span></span> | <span data-ttu-id="f15da-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f15da-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f15da-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f15da-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f15da-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f15da-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f15da-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f15da-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f15da-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f15da-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f15da-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f15da-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f15da-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f15da-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f15da-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f15da-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15da-133">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f15da-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f15da-134">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="f15da-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
