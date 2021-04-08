---
description: Spécifie le format de sortie préféré pour un encodeur.
ms.assetid: 36a09696-3fe7-41a0-93f1-712220f88b04
title: Attribut MFT_PREFERRED_OUTPUTTYPE_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13cd079bee65f5324987d9b38dca845ec5b85f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863957"
---
# <a name="mft_preferred_outputtype_attribute-attribute"></a><span data-ttu-id="8f8df-103">Attribut de l' \_ \_ attribut OUTPUTTYPE préféré de MFT \_</span><span class="sxs-lookup"><span data-stu-id="8f8df-103">MFT\_PREFERRED\_OUTPUTTYPE\_Attribute attribute</span></span>

<span data-ttu-id="8f8df-104">Spécifie le format de sortie préféré pour un encodeur.</span><span class="sxs-lookup"><span data-stu-id="8f8df-104">Specifies the preferred output format for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="8f8df-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8f8df-105">Data type</span></span>

<span data-ttu-id="8f8df-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ stocké en tant que _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="8f8df-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="8f8df-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="8f8df-107">Get/set</span></span>

<span data-ttu-id="8f8df-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="8f8df-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="8f8df-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="8f8df-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8f8df-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="8f8df-110">Applies to</span></span>

[<span data-ttu-id="8f8df-111">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="8f8df-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="8f8df-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8f8df-112">Remarks</span></span>

<span data-ttu-id="8f8df-113">Cet attribut peut être défini sur l’objet d’activation renvoyé par la fonction [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) .</span><span class="sxs-lookup"><span data-stu-id="8f8df-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="8f8df-114">L’attribut s’applique uniquement lorsque l’objet d’activation est configuré pour créer un encodeur.</span><span class="sxs-lookup"><span data-stu-id="8f8df-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="8f8df-115">La valeur de l’attribut est un type de média.</span><span class="sxs-lookup"><span data-stu-id="8f8df-115">The value of the attribute is a media type.</span></span> <span data-ttu-id="8f8df-116">L’objet d’activation définit ce type de sortie sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="8f8df-116">The activation object sets this output type on the encoder.</span></span>

<span data-ttu-id="8f8df-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8f8df-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f8df-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f8df-118">Requirements</span></span>



| <span data-ttu-id="8f8df-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f8df-119">Requirement</span></span> | <span data-ttu-id="8f8df-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f8df-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f8df-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f8df-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8f8df-122">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8f8df-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="8f8df-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f8df-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8f8df-124">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8f8df-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8f8df-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f8df-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f8df-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f8df-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f8df-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f8df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f8df-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8f8df-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8f8df-129">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="8f8df-129">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="8f8df-130">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="8f8df-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




