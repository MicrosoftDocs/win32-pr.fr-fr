---
description: Spécifie la configuration de l’orateur sur l’ordinateur client.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: MFPKEY_WMADEC_SPKRCFG, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528569"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a><span data-ttu-id="80655-103">MFPKEY \_ WMADEC \_ SPKRCFG, propriété</span><span class="sxs-lookup"><span data-stu-id="80655-103">MFPKEY\_WMADEC\_SPKRCFG Property</span></span>

<span data-ttu-id="80655-104">Spécifie la configuration de l’orateur sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="80655-104">Specifies the speaker configuration on the client computer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="80655-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="80655-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="80655-106">\_wszWMACSpeakerConfig g</span><span class="sxs-lookup"><span data-stu-id="80655-106">g\_wszWMACSpeakerConfig</span></span>

## <a name="data-type"></a><span data-ttu-id="80655-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="80655-107">Data Type</span></span>

<span data-ttu-id="80655-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="80655-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="80655-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="80655-109">Default Value</span></span>

<span data-ttu-id="80655-110">Aucune configuration d’orateur spécifique n’est utilisée.</span><span class="sxs-lookup"><span data-stu-id="80655-110">No specific speaker configuration is assumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="80655-111">Notes</span><span class="sxs-lookup"><span data-stu-id="80655-111">Remarks</span></span>

<span data-ttu-id="80655-112">Vous devez définir cette valeur sur l’une des constantes ou valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="80655-112">You should set this value to one of the constants or values in the following table.</span></span> <span data-ttu-id="80655-113">Les constantes sont définies dans Microsoft DirectSound et sont répertoriées ici pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="80655-113">The constants are defined in Microsoft DirectSound, and are listed here for convenience.</span></span> <span data-ttu-id="80655-114">Pour résoudre ces noms de constantes pour votre compilateur, vous devez inclure dsound. h.</span><span class="sxs-lookup"><span data-stu-id="80655-114">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="80655-115">Constante</span><span class="sxs-lookup"><span data-stu-id="80655-115">Constant</span></span>             | <span data-ttu-id="80655-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="80655-116">Value</span></span>      | <span data-ttu-id="80655-117">Description</span><span class="sxs-lookup"><span data-stu-id="80655-117">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="80655-118">DSSPEAKER \_ DIRECTOUT</span><span class="sxs-lookup"><span data-stu-id="80655-118">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="80655-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80655-119">0x00000000</span></span> | <span data-ttu-id="80655-120">L’audio est transmis directement, sans être configuré pour les intervenants.</span><span class="sxs-lookup"><span data-stu-id="80655-120">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="80655-121">\_casque DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="80655-121">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="80655-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="80655-122">0x00000001</span></span> | <span data-ttu-id="80655-123">L’ordinateur client est équipé d’un casque.</span><span class="sxs-lookup"><span data-stu-id="80655-123">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="80655-124">\_mono DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="80655-124">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="80655-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="80655-125">0x00000002</span></span> | <span data-ttu-id="80655-126">L’ordinateur client est équipé d’un orateur monoaural.</span><span class="sxs-lookup"><span data-stu-id="80655-126">The client computer is equipped with a monoaural speaker.</span></span>                    |
| <span data-ttu-id="80655-127">DSSPEAKER \_ Quad</span><span class="sxs-lookup"><span data-stu-id="80655-127">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="80655-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="80655-128">0x00000003</span></span> | <span data-ttu-id="80655-129">L’ordinateur client est équipé de haut-parleurs Quadraphonic.</span><span class="sxs-lookup"><span data-stu-id="80655-129">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="80655-130">\_stéréo DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="80655-130">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="80655-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="80655-131">0x00000004</span></span> | <span data-ttu-id="80655-132">L’ordinateur client est équipé de haut-parleurs stéréo.</span><span class="sxs-lookup"><span data-stu-id="80655-132">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="80655-133">DSSPEAKER \_ surround</span><span class="sxs-lookup"><span data-stu-id="80655-133">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="80655-134">0x00000005</span><span class="sxs-lookup"><span data-stu-id="80655-134">0x00000005</span></span> | <span data-ttu-id="80655-135">L’ordinateur client est équipé de haut-parleurs Surround audio à quatre canaux.</span><span class="sxs-lookup"><span data-stu-id="80655-135">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="80655-136">DSSPEAKER \_ 5POINT1</span><span class="sxs-lookup"><span data-stu-id="80655-136">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="80655-137">0x00000006</span><span class="sxs-lookup"><span data-stu-id="80655-137">0x00000006</span></span> | <span data-ttu-id="80655-138">L’ordinateur client est équipé de cinq enceintes et d’un caisson de basses.</span><span class="sxs-lookup"><span data-stu-id="80655-138">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="80655-139">DSSPEAKER \_ 7POINT1</span><span class="sxs-lookup"><span data-stu-id="80655-139">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="80655-140">0x00000007</span><span class="sxs-lookup"><span data-stu-id="80655-140">0x00000007</span></span> | <span data-ttu-id="80655-141">L’ordinateur client est équipé de sept haut-parleurs et d’un caisson de basses.</span><span class="sxs-lookup"><span data-stu-id="80655-141">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="80655-142">La valeur définie pour cette propriété détermine les formats de sortie énumérés par le codec pour l’audio multicanal.</span><span class="sxs-lookup"><span data-stu-id="80655-142">The value set for this property determines the output formats enumerated by the codec for multichannel audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="80655-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80655-143">Requirements</span></span>



| <span data-ttu-id="80655-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80655-144">Requirement</span></span> | <span data-ttu-id="80655-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="80655-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80655-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80655-146">Minimum supported client</span></span><br/> | <span data-ttu-id="80655-147">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80655-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="80655-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80655-148">Minimum supported server</span></span><br/> | <span data-ttu-id="80655-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80655-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="80655-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="80655-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="80655-151"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="80655-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80655-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80655-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80655-153">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80655-153">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




