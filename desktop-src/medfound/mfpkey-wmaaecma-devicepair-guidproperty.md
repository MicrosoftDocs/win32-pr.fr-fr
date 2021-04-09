---
description: Identifie la combinaison de périphériques audio actuellement utilisée par l’application avec le DSP de capture vocale.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: MFPKEY_WMAAECMA_DEVICEPAIR_GUID, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a586d7d31f29b20eb7ca39320d5fa57b9943715a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114430"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a><span data-ttu-id="75212-103">MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID, propriété</span><span class="sxs-lookup"><span data-stu-id="75212-103">MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID Property</span></span>

<span data-ttu-id="75212-104">Identifie la combinaison de périphériques audio actuellement utilisée par l’application avec le DSP de capture vocale.</span><span class="sxs-lookup"><span data-stu-id="75212-104">Identifies the combination of audio devices that the application is currently using with the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="75212-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="75212-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="75212-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="75212-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="75212-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="75212-107">Data Type</span></span>

<span data-ttu-id="75212-108">\_CLSID VT</span><span class="sxs-lookup"><span data-stu-id="75212-108">VT\_CLSID</span></span>

## <a name="applies-to"></a><span data-ttu-id="75212-109">S'applique à</span><span class="sxs-lookup"><span data-stu-id="75212-109">Applies To</span></span>

-   [<span data-ttu-id="75212-110">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="75212-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="75212-111">Notes</span><span class="sxs-lookup"><span data-stu-id="75212-111">Remarks</span></span>

<span data-ttu-id="75212-112">Définissez cette propriété si vous utilisez le DSP en mode filtre et que la valeur de la propriété [MFPKEY \_ WMAAECMA \_ Retrieve \_ TS \_ Statistic](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) est \_ true.</span><span class="sxs-lookup"><span data-stu-id="75212-112">Set this property if you are using the DSP in filter mode and the value of the [MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE.</span></span>

<span data-ttu-id="75212-113">Lorsque la propriété [**MFPKEY \_ WMAAECMA Retrieve des \_ \_ \_ statistiques TS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) est \_ définie sur true, le DSP collecte des statistiques sur les horodatages à partir des périphériques audio et stocke ces informations dans le registre.</span><span class="sxs-lookup"><span data-stu-id="75212-113">When the [**MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE, the DSP collects statistics about the time stamps from the audio devices and stores this information in the registry.</span></span> <span data-ttu-id="75212-114">Ces statistiques peuvent changer pour chaque combinaison de périphérique de capture audio et de périphérique de rendu audio.</span><span class="sxs-lookup"><span data-stu-id="75212-114">These statistics can change for each combination of audio capture device and audio rendering device.</span></span> <span data-ttu-id="75212-115">Par conséquent, l’application doit assigner un GUID pour identifier la combinaison particulière d’appareils en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="75212-115">Therefore, the application must assign a GUID to identify the particular combination of devices in use.</span></span> <span data-ttu-id="75212-116">L’application doit effectuer le suivi de ce GUID pour pouvoir attribuer le même GUID chaque fois qu’il utilise la même paire de périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="75212-116">The application should keep track of this GUID, so that it can assign the same GUID whenever it uses the same pair of audio devices.</span></span>

<span data-ttu-id="75212-117">Si vous utilisez le DSP en mode Source, vous n’avez pas besoin de définir cette propriété.</span><span class="sxs-lookup"><span data-stu-id="75212-117">If you are using the DSP in source mode, you do not need to set this property.</span></span> <span data-ttu-id="75212-118">Le DSP génère automatiquement un GUID basé sur la valeur de la propriété d’index de l' [ \_ \_ appareil \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-device-indexesproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="75212-118">The DSP automatically generates a GUID based on the value of the [MFPKEY\_WMAAECMA\_DEVICE\_INDEXES](mfpkey-wmaaecma-device-indexesproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="75212-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75212-119">Requirements</span></span>



| <span data-ttu-id="75212-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75212-120">Requirement</span></span> | <span data-ttu-id="75212-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="75212-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75212-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75212-122">Minimum supported client</span></span><br/> | <span data-ttu-id="75212-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75212-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="75212-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75212-124">Minimum supported server</span></span><br/> | <span data-ttu-id="75212-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75212-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="75212-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="75212-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="75212-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="75212-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75212-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75212-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75212-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="75212-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="75212-130">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="75212-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
