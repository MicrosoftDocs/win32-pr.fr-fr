---
description: Spécifie le profil de complexité du contenu encodé.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: MFPKEY_DECODERCOMPLEXITYPROFILE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864174"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a><span data-ttu-id="5a458-103">MFPKEY \_ propriété DECODERCOMPLEXITYPROFILE</span><span class="sxs-lookup"><span data-stu-id="5a458-103">MFPKEY\_DECODERCOMPLEXITYPROFILE Property</span></span>

<span data-ttu-id="5a458-104">Spécifie le profil de complexité du contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="5a458-104">Specifies the complexity profile of the encoded content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5a458-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5a458-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5a458-106">\_wszWMVCDecoderComplexityProfile g</span><span class="sxs-lookup"><span data-stu-id="5a458-106">g\_wszWMVCDecoderComplexityProfile</span></span>

## <a name="data-type"></a><span data-ttu-id="5a458-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="5a458-107">Data Type</span></span>

<span data-ttu-id="5a458-108">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="5a458-108">**VT\_BSTR**</span></span>

## <a name="remarks"></a><span data-ttu-id="5a458-109">Notes</span><span class="sxs-lookup"><span data-stu-id="5a458-109">Remarks</span></span>

<span data-ttu-id="5a458-110">Vous ne pouvez lire cette valeur qu’une fois l’encodage terminé.</span><span class="sxs-lookup"><span data-stu-id="5a458-110">You can read this value only after encoding is completed.</span></span>

<span data-ttu-id="5a458-111">Pour l’audio, cette propriété a l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5a458-111">For audio, this property has one of the following values.</span></span>



| <span data-ttu-id="5a458-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a458-112">Value</span></span> | <span data-ttu-id="5a458-113">Description</span><span class="sxs-lookup"><span data-stu-id="5a458-113">Description</span></span>                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a458-114">Ko</span><span class="sxs-lookup"><span data-stu-id="5a458-114">"L1"</span></span>  | <span data-ttu-id="5a458-115">Encodage standard avec un taux d’échantillonnage de 44,1 KHz et un taux binaire maximal de 161 Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="5a458-115">Standard encoding with a sampling rate of 44.1 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="5a458-116">NIV</span><span class="sxs-lookup"><span data-stu-id="5a458-116">"L2"</span></span>  | <span data-ttu-id="5a458-117">Encodage standard avec des taux d’échantillonnage allant jusqu’à 48 KHz et une vitesse de transmission maximale de 161 Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="5a458-117">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="5a458-118">Mémoire</span><span class="sxs-lookup"><span data-stu-id="5a458-118">"L3"</span></span>  | <span data-ttu-id="5a458-119">Encodage standard avec des taux d’échantillonnage allant jusqu’à 48 KHz et une vitesse de transmission maximale de 385 Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="5a458-119">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 385 Kbps.</span></span>         |
| <span data-ttu-id="5a458-120">"M0a"</span><span class="sxs-lookup"><span data-stu-id="5a458-120">"M0a"</span></span> | <span data-ttu-id="5a458-121">Encodage professionnel avec des taux d’échantillonnage allant jusqu’à 48 KHz et des vitesses de bit comprises entre 48 et 192 kbit/s.</span><span class="sxs-lookup"><span data-stu-id="5a458-121">Professional encoding with sampling rates up to 48 KHz and bit rates between 48 and 192 Kbps.</span></span>  |
| <span data-ttu-id="5a458-122">"M0b"</span><span class="sxs-lookup"><span data-stu-id="5a458-122">"M0b"</span></span> | <span data-ttu-id="5a458-123">Codage professionnel avec des taux d’échantillonnage allant jusqu’à 48 KHz et un débit maximal de 192 Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="5a458-123">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 192 Kbps.</span></span>      |
| <span data-ttu-id="5a458-124">M1</span><span class="sxs-lookup"><span data-stu-id="5a458-124">"M1"</span></span>  | <span data-ttu-id="5a458-125">Codage professionnel avec des taux d’échantillonnage allant jusqu’à 48 KHz et un débit maximal de 384 Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="5a458-125">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 384 Kbps.</span></span>      |
| <span data-ttu-id="5a458-126">Carré</span><span class="sxs-lookup"><span data-stu-id="5a458-126">"M2"</span></span>  | <span data-ttu-id="5a458-127">Codage professionnel avec des taux d’échantillonnage allant jusqu’à 96 KHz et un débit maximal de 768 Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="5a458-127">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 768 Kbps.</span></span>      |
| <span data-ttu-id="5a458-128">M3</span><span class="sxs-lookup"><span data-stu-id="5a458-128">"M3"</span></span>  | <span data-ttu-id="5a458-129">Encodage professionnel avec des taux d’échantillonnage allant jusqu’à 96 KHz et un débit maximal de 1,5 Mbits/s.</span><span class="sxs-lookup"><span data-stu-id="5a458-129">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 1.5 Mbps.</span></span>      |
| <span data-ttu-id="5a458-130">N1</span><span class="sxs-lookup"><span data-stu-id="5a458-130">"N1"</span></span>  | <span data-ttu-id="5a458-131">Encodage sans perte avec des taux d’échantillonnage allant jusqu’à 48 KHz et un maximum de 2 canaux.</span><span class="sxs-lookup"><span data-stu-id="5a458-131">Lossless encoding with sampling rates up to 48 KHz and a maximum of 2 channels.</span></span>                |
| <span data-ttu-id="5a458-132">N2</span><span class="sxs-lookup"><span data-stu-id="5a458-132">"N2"</span></span>  | <span data-ttu-id="5a458-133">Encodage sans perte avec des taux d’échantillonnage allant jusqu’à 96 KHz et un maximum de 6 canaux (5,1 Surround).</span><span class="sxs-lookup"><span data-stu-id="5a458-133">Lossless encoding with sampling rates up to 96 KHz and a maximum of 6 channels (5.1 surround).</span></span> |
| <span data-ttu-id="5a458-134">N3</span><span class="sxs-lookup"><span data-stu-id="5a458-134">"N3"</span></span>  | <span data-ttu-id="5a458-135">Encodage sans perte avec des taux d’échantillonnage allant jusqu’à 96 KHz et un maximum de 8 canaux (7,1 Surround).</span><span class="sxs-lookup"><span data-stu-id="5a458-135">Lossless encoding with sampling rates up to 96 KHz and a maximum of 8 channels (7.1 surround).</span></span> |



 

<span data-ttu-id="5a458-136">Pour la vidéo, cette propriété a l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a458-136">For video, this property has one of the following values:</span></span>



| <span data-ttu-id="5a458-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a458-137">Value</span></span> | <span data-ttu-id="5a458-138">Description</span><span class="sxs-lookup"><span data-stu-id="5a458-138">Description</span></span>                                                                       |
|-------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5a458-139">FOURNISSEURS</span><span class="sxs-lookup"><span data-stu-id="5a458-139">"AP"</span></span>  | <span data-ttu-id="5a458-140">Profil avancé (disponible uniquement sur le codec du profil avancé Windows Media Video 9)</span><span class="sxs-lookup"><span data-stu-id="5a458-140">advanced profile (available only on Windows Media Video 9 Advanced Profile codec)</span></span> |
| <span data-ttu-id="5a458-141">CP</span><span class="sxs-lookup"><span data-stu-id="5a458-141">"CP"</span></span>  | <span data-ttu-id="5a458-142">n’est plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a458-142">no longer supported</span></span>                                                               |
| <span data-ttu-id="5a458-143">CANAL</span><span class="sxs-lookup"><span data-stu-id="5a458-143">"MP"</span></span>  | <span data-ttu-id="5a458-144">Profil principal</span><span class="sxs-lookup"><span data-stu-id="5a458-144">main profile</span></span>                                                                      |
| <span data-ttu-id="5a458-145">SR</span><span class="sxs-lookup"><span data-stu-id="5a458-145">"SP"</span></span>  | <span data-ttu-id="5a458-146">Profil simple</span><span class="sxs-lookup"><span data-stu-id="5a458-146">simple profile</span></span>                                                                    |



 

<span data-ttu-id="5a458-147">Pour le contenu vidéo, vous pouvez demander un niveau de profil en définissant [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) avant de commencer l’encodage.</span><span class="sxs-lookup"><span data-stu-id="5a458-147">For video content, you can request a profile level by setting [MFPKEY\_DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) before you begin encoding.</span></span> <span data-ttu-id="5a458-148">Le codec tentera d’effectuer un encodage dans les paramètres du niveau de complexité demandé, mais les autres paramètres que vous configurerez seront prioritaires.</span><span class="sxs-lookup"><span data-stu-id="5a458-148">The codec will attempt to encode within the parameters of the requested complexity level, but the other settings that you configure will take precedence.</span></span> <span data-ttu-id="5a458-149">Vous devez toujours vérifier la valeur du profil de complexité réel après l’encodage au cas où votre demande n’a pas pu être honorée.</span><span class="sxs-lookup"><span data-stu-id="5a458-149">You should always check the actual complexity profile value after encoding in case your request could not be honored.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a458-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a458-150">Requirements</span></span>



| <span data-ttu-id="5a458-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a458-151">Requirement</span></span> | <span data-ttu-id="5a458-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a458-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a458-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a458-153">Minimum supported client</span></span><br/> | <span data-ttu-id="5a458-154">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a458-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5a458-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a458-155">Minimum supported server</span></span><br/> | <span data-ttu-id="5a458-156">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a458-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5a458-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a458-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a458-158"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a458-158"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a458-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a458-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a458-160">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a458-160">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




