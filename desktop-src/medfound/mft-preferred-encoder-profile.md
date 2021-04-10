---
description: Contient les propriétés de configuration d’un encodeur.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: Attribut MFT_PREFERRED_ENCODER_PROFILE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfdc85ead0fe813215b3edaea14833400df5445d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951486"
---
# <a name="mft_preferred_encoder_profile-attribute"></a><span data-ttu-id="75453-103">\_Attribut de \_ profil d’encodeur préféré MFT \_</span><span class="sxs-lookup"><span data-stu-id="75453-103">MFT\_PREFERRED\_ENCODER\_PROFILE attribute</span></span>

<span data-ttu-id="75453-104">Contient les propriétés de configuration d’un encodeur.</span><span class="sxs-lookup"><span data-stu-id="75453-104">Contains configuration properties for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="75453-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="75453-105">Data type</span></span>

<span data-ttu-id="75453-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ stocké en tant que _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="75453-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="75453-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="75453-107">Get/set</span></span>

<span data-ttu-id="75453-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="75453-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="75453-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="75453-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="75453-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="75453-110">Applies to</span></span>

[<span data-ttu-id="75453-111">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="75453-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="75453-112">Notes</span><span class="sxs-lookup"><span data-stu-id="75453-112">Remarks</span></span>

<span data-ttu-id="75453-113">Cet attribut peut être défini sur l’objet d’activation renvoyé par la fonction [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) .</span><span class="sxs-lookup"><span data-stu-id="75453-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="75453-114">L’attribut s’applique uniquement lorsque l’objet d’activation est configuré pour créer un encodeur.</span><span class="sxs-lookup"><span data-stu-id="75453-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="75453-115">La valeur de l’attribut est un pointeur vers un magasin d’attributs, qui contient lui-même des propriétés à définir sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="75453-115">The value of the attribute is a pointer to an attribute store, which itself contains properties to set on the encoder.</span></span>

<span data-ttu-id="75453-116">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="75453-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="75453-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75453-117">Requirements</span></span>



| <span data-ttu-id="75453-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75453-118">Requirement</span></span> | <span data-ttu-id="75453-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="75453-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="75453-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75453-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75453-121">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="75453-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="75453-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75453-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75453-123">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="75453-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="75453-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="75453-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75453-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="75453-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75453-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75453-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75453-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="75453-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="75453-128">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="75453-128">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="75453-129">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="75453-129">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




