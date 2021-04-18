---
description: Spécifie si le décodeur audio doit fournir une sortie haute résolution.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: MFPKEY_WMADEC_HIRESOUTPUT, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519629"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a><span data-ttu-id="d129c-103">MFPKEY \_ WMADEC \_ HIRESOUTPUT, propriété</span><span class="sxs-lookup"><span data-stu-id="d129c-103">MFPKEY\_WMADEC\_HIRESOUTPUT Property</span></span>

<span data-ttu-id="d129c-104">Spécifie si le décodeur audio doit fournir une sortie haute résolution.</span><span class="sxs-lookup"><span data-stu-id="d129c-104">Specifies whether the audio decoder should deliver high-resolution output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d129c-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d129c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d129c-106">\_wszWMACHiResOutput g</span><span class="sxs-lookup"><span data-stu-id="d129c-106">g\_wszWMACHiResOutput</span></span>

## <a name="data-type"></a><span data-ttu-id="d129c-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="d129c-107">Data Type</span></span>

<span data-ttu-id="d129c-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d129c-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="d129c-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="d129c-109">Default Value</span></span>

<span data-ttu-id="d129c-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="d129c-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="d129c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d129c-111">Remarks</span></span>

<span data-ttu-id="d129c-112">Affectez à cette propriété la \_ valeur variant true pour décoder le contenu audio multicanaux ou 24 bits, ou l’audio avec un taux d’échantillonnage supérieur à 48 000 Hz.</span><span class="sxs-lookup"><span data-stu-id="d129c-112">Set this property to VARIANT\_TRUE to decode multichannel or 24-bit audio content, or audio with a sample rate greater than 48,000 Hz.</span></span> <span data-ttu-id="d129c-113">Si le contenu est encodé en haute résolution, mais que cette propriété a \_ la valeur false, les comportements suivants s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="d129c-113">If the content is encoded in high resolution, but this property is VARIANT\_FALSE, the following behaviors apply:</span></span>

-   <span data-ttu-id="d129c-114">La sortie DMO sera limitée à 16 bits, 48-KHz stéréo.</span><span class="sxs-lookup"><span data-stu-id="d129c-114">The DMO output will be limited to 16-bit, 48-KHz stereo.</span></span>
-   <span data-ttu-id="d129c-115">La table MFT énumère les modes de sortie qui sont limités à 16 bits et n’implique pas de modifications du nombre de canaux ou du taux d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="d129c-115">The MFT will enumerate output modes that are limited to 16 bits and do not involve changes in channel count or sampling rate.</span></span>

<span data-ttu-id="d129c-116">Les propriétés du son haute résolution sont transmises dans une structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) , et non [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d129c-116">The properties of high-resolution audio are passed in a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure, not [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span></span>

<span data-ttu-id="d129c-117">La sortie haute résolution est disponible uniquement si le décodeur s’exécute sous Windows XP ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d129c-117">High-resolution output is available only if the decoder is running on Windows XP or later.</span></span> <span data-ttu-id="d129c-118">Vous pouvez définir cette propriété indépendamment du système d’exploitation sur lequel votre application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d129c-118">You can set this property regardless of the operating system on which your application is running.</span></span> <span data-ttu-id="d129c-119">Dans les versions de Windows antérieures à Windows XP, le décodeur ignore ce paramètre et remet la sortie standard.</span><span class="sxs-lookup"><span data-stu-id="d129c-119">On versions of Windows earlier than Windows XP, the decoder will ignore this setting and deliver standard output.</span></span>

<span data-ttu-id="d129c-120">De nombreux lecteurs (y compris le lecteur Windows Media série 9 et versions ultérieures) définissent cette valeur pour tout le contenu.</span><span class="sxs-lookup"><span data-stu-id="d129c-120">Many players (including Windows Media Player 9 Series and later) set this value for all content.</span></span>

## <a name="requirements"></a><span data-ttu-id="d129c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d129c-121">Requirements</span></span>



| <span data-ttu-id="d129c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d129c-122">Requirement</span></span> | <span data-ttu-id="d129c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d129c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d129c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d129c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d129c-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d129c-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d129c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d129c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d129c-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d129c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d129c-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d129c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d129c-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d129c-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d129c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d129c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d129c-131">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d129c-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
