---
description: Spécifie les coefficients de repli pour le décodage de l’audio multicanaux pour un nombre de canaux inférieur à celui contenu dans le flux encodé.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: MFPKEY_WMADEC_FOLDDOWN_MATRIX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524947"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a><span data-ttu-id="7deb6-103">MFPKEY \_ WMADEC \_ FOLDDOWN, propriété de la \_ matrice</span><span class="sxs-lookup"><span data-stu-id="7deb6-103">MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX Property</span></span>

<span data-ttu-id="7deb6-104">Spécifie les coefficients de repli pour le décodage de l’audio multicanaux pour un nombre de canaux inférieur à celui contenu dans le flux encodé.</span><span class="sxs-lookup"><span data-stu-id="7deb6-104">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7deb6-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7deb6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7deb6-106">\_wszWMACFoldDownXToYChannels g</span><span class="sxs-lookup"><span data-stu-id="7deb6-106">g\_wszWMACFoldDownXToYChannels</span></span>

<span data-ttu-id="7deb6-107">\_wszWMACFoldXToYChannelsZ g</span><span class="sxs-lookup"><span data-stu-id="7deb6-107">g\_wszWMACFoldXToYChannelsZ</span></span>

## <a name="data-type"></a><span data-ttu-id="7deb6-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="7deb6-108">Data Type</span></span>

<span data-ttu-id="7deb6-109">**Tableau VT de \_ groupe VT \| \_**</span><span class="sxs-lookup"><span data-stu-id="7deb6-109">**VT\_ARRAY \| VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="7deb6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7deb6-110">Remarks</span></span>

<span data-ttu-id="7deb6-111">Un décodeur audio peut agir en tant qu’objet de média DirectX (DMO) ou en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="7deb6-111">An audio decoder can act as a DirectX Media Object (DMO) or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="7deb6-112">Pour plus d’informations sur le moment où un décodeur agit comme DMO ou MFT, consultez les pages de référence des codecs individuels sous [objets codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="7deb6-112">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="7deb6-113">Quand vous utilisez un décodeur en tant qu’DMO, le décodeur peut effectuer un repli de canal vers le dessous, et vous pouvez énumérer les types de média de sortie repliés en appelant [**IMediaObject :: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span><span class="sxs-lookup"><span data-stu-id="7deb6-113">When you use a decoder as a DMO, the decoder can perform channel fold down, and you can enumerate folded down output media types by calling [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

<span data-ttu-id="7deb6-114">Lorsque vous utilisez un décodeur en tant que MFT, le décodeur par défaut n’effectue pas de repli et n’offre pas de types de média de sortie pliés.</span><span class="sxs-lookup"><span data-stu-id="7deb6-114">When you use a decoder as an MFT, the decoder by default will not perform any fold down, and will not offer folded down output media types.</span></span> <span data-ttu-id="7deb6-115">Un décodeur agissant en tant que MFT effectue un repli uniquement si les coefficients de repli personnalisé sont définis à l’aide de la propriété de **\_ \_ \_ matrice MFPKEY WMADEC FOLDDOWN** .</span><span class="sxs-lookup"><span data-stu-id="7deb6-115">A decoder acting as an MFT will perform fold down only if custom fold-down coefficients are set using the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property.</span></span>

<span data-ttu-id="7deb6-116">Si la propriété de la **\_ \_ \_ matrice MFPKEY WMADEC FOLDDOWN** n’est pas définie sur la MFT du décodeur audio et que vous souhaitez effectuer un repli, vous pouvez utiliser (en tant que MFT) le processeur de signal numérique de reéchantillonneur audio.</span><span class="sxs-lookup"><span data-stu-id="7deb6-116">If the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property is not set on the audio decoder MFT, and you want to perform a fold down, you can use (as an MFT) the Audio Resampler digital signal processor.</span></span>

<span data-ttu-id="7deb6-117">La valeur de cette propriété est une chaîne contenant des coefficients de repli dans une liste séparée par des virgules de valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="7deb6-117">The value for this property is a string containing fold-down coefficients in a comma-separated list of integer values.</span></span> <span data-ttu-id="7deb6-118">La liste doit contenir un nombre d’entiers pour chaque canal dans le contenu encodé égal au nombre de canaux dans le contenu décodé.</span><span class="sxs-lookup"><span data-stu-id="7deb6-118">The list must contain a number of integers for each channel in the encoded content equal to the number of channels in the decoded content.</span></span>

<span data-ttu-id="7deb6-119">Si le coefficient est égal à zéro, la valeur à utiliser dans la chaîne doit être « -2147483648 »; dans le cas contraire, la valeur est calculée à l’aide de l’équation : 20 \* 65536 \* log10 (x).</span><span class="sxs-lookup"><span data-stu-id="7deb6-119">If the coefficient is zero, the value to be used in the string must be "-2147483648";otherwise the value is computed using the equation: 20 \* 65536 \* log10(x).</span></span>

<span data-ttu-id="7deb6-120">Les coefficients sont répertoriés dans l’ordre de masque de canal, comme défini par les constantes de masque de canal incluses dans le fichier d’en-tête mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="7deb6-120">Coefficients are listed in channel mask order, as defined by the channel mask constants that are included in the mmreg.h header file.</span></span> <span data-ttu-id="7deb6-121">Par conséquent, les deux premières valeurs dans un pli de canal 6-à-2 représentent les portions du canal de sortie de gauche et le canal de sortie de droite qui sont constitués du canal de gauche central dans le flux de 6 canaux.</span><span class="sxs-lookup"><span data-stu-id="7deb6-121">Therefore, the first two values in a 6-to-2 channel fold-down represent the portions of the left output channel and the right output channel that are made up of the center left channel in the 6 channel stream.</span></span>

<span data-ttu-id="7deb6-122">Vous devez définir cette propriété uniquement si les valeurs de repli fournies par l’auteur sont conservées avec le contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="7deb6-122">You should set this property only if author-supplied fold-down values are persisted with the encoded content.</span></span> <span data-ttu-id="7deb6-123">Dans le cas contraire, laissez le décodeur effectuer ses propres calculs.</span><span class="sxs-lookup"><span data-stu-id="7deb6-123">Otherwise, let the decoder make its own calculations.</span></span>

<span data-ttu-id="7deb6-124">Le codec Windows Media Audio 10 Professional prend actuellement en charge le repli sur deux canaux uniquement.</span><span class="sxs-lookup"><span data-stu-id="7deb6-124">The Windows Media Audio 10 Professional codec currently only supports fold-down to two channels.</span></span>

<span data-ttu-id="7deb6-125">Si la propriété [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) est définie sur **DSSPEAKER \_ surround**, le codec ignore les coefficients de repli et de repli fournis par l’auteur jusqu’à un signal à 2 canaux qui peut être traité par le décodeur de matrice du récepteur.</span><span class="sxs-lookup"><span data-stu-id="7deb6-125">If the [MFPKEY\_WMADEC\_SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) property is set to **DSSPEAKER\_SURROUND**, the codec will ignore author-supplied fold-down coefficients and fold down to a 2-channel signal that can be processed by the matrix decoder of the receiver.</span></span> <span data-ttu-id="7deb6-126">Cela permet à l’équipement surround d’offrir quatre canaux.</span><span class="sxs-lookup"><span data-stu-id="7deb6-126">This enables surround equipment to deliver four channels.</span></span> <span data-ttu-id="7deb6-127">Ce mode est pris en charge uniquement si la source est 5,1.</span><span class="sxs-lookup"><span data-stu-id="7deb6-127">This mode is supported only if the source is 5.1.</span></span> <span data-ttu-id="7deb6-128">Le codec peut uniquement plier 8 canaux à 2 canaux.</span><span class="sxs-lookup"><span data-stu-id="7deb6-128">The codec can only fold 8 channels to 2 channels.</span></span>

## <a name="requirements"></a><span data-ttu-id="7deb6-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7deb6-129">Requirements</span></span>



| <span data-ttu-id="7deb6-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7deb6-130">Requirement</span></span> | <span data-ttu-id="7deb6-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7deb6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7deb6-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7deb6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7deb6-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7deb6-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7deb6-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7deb6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7deb6-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7deb6-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7deb6-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="7deb6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7deb6-137"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7deb6-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7deb6-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7deb6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7deb6-139">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7deb6-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
