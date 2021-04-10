---
description: Spécifie si le décodeur doit effectuer Lt-Rt pli vers le dessous.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: MFPKEY_WMADEC_LTRTOUTPUT, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114426"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a><span data-ttu-id="199f8-103">MFPKEY \_ WMADEC \_ LTRTOUTPUT, propriété</span><span class="sxs-lookup"><span data-stu-id="199f8-103">MFPKEY\_WMADEC\_LTRTOUTPUT Property</span></span>

<span data-ttu-id="199f8-104">Spécifie si le décodeur doit effectuer Lt-Rt pli vers le dessous.</span><span class="sxs-lookup"><span data-stu-id="199f8-104">Specifies whether the decoder should perform Lt-Rt fold down.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="199f8-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="199f8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="199f8-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="199f8-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="199f8-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="199f8-107">Data Type</span></span>

<span data-ttu-id="199f8-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="199f8-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="199f8-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="199f8-109">Default Value</span></span>

<span data-ttu-id="199f8-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="199f8-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="199f8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="199f8-111">Remarks</span></span>

<span data-ttu-id="199f8-112">Si cette propriété a la valeur VARIANT \_ false et que la sortie est stéréo, le décodeur audio utilise le repli de canal simple.</span><span class="sxs-lookup"><span data-stu-id="199f8-112">If this property has a value of VARIANT\_FALSE and the output is stereo, the audio decoder uses simple channel fold down.</span></span> <span data-ttu-id="199f8-113">Si cette propriété a la valeur VARIANT \_ true, le décodeur audio effectue une repliage Lt-Rt (matrice) vers le bout de la chaîne stéréo, puis tout décodeur Dolby Surround peut être utilisé pour décoder le surround à matrice.</span><span class="sxs-lookup"><span data-stu-id="199f8-113">If this property has a value of VARIANT\_TRUE, the audio decoder performs Lt-Rt (matrixed) fold down to stereo, and then any Dolby Surround decoder can be used to decode the matrixed surround .</span></span> <span data-ttu-id="199f8-114">Par exemple, le décodeur audio peut effectuer Lt-Rt repli sur le contenu 5,1 ou 7,1.</span><span class="sxs-lookup"><span data-stu-id="199f8-114">For example, the audio decoder could perform Lt-Rt fold down on 5.1 or 7.1 content.</span></span>

<span data-ttu-id="199f8-115">Cette propriété est prise en charge uniquement lorsque le décodeur agit comme un objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="199f8-115">This property is supported only when the decoder is acting as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="199f8-116">Aucun pli d’un type quelconque n’est pris en charge lorsque le décodeur agit comme une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="199f8-116">No fold down of any kind is supported when the decoder is acting as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="199f8-117">Sur Windows Vista, si vous obtenez une interface **IPropertyStore** sur un décodeur audio, le décodeur agit comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="199f8-117">On Windows Vista, if you obtain an **IPropertyStore** interface on an audio decoder, the decoder acts as an MFT.</span></span> <span data-ttu-id="199f8-118">Par conséquent, cette propriété ne peut pas être utilisée sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="199f8-118">Consequently, this property cannot be used on Windows Vista.</span></span> <span data-ttu-id="199f8-119">Pour plus d’informations sur le moment où un décodeur agit comme DMO ou MFT, consultez les pages de référence des codecs individuels sous [objets codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="199f8-119">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="199f8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="199f8-120">Requirements</span></span>



| <span data-ttu-id="199f8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="199f8-121">Requirement</span></span> | <span data-ttu-id="199f8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="199f8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="199f8-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="199f8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="199f8-124">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="199f8-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="199f8-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="199f8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="199f8-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="199f8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="199f8-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="199f8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="199f8-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="199f8-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="199f8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="199f8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="199f8-130">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="199f8-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
