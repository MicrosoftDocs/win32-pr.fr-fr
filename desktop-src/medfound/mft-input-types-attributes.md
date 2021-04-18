---
description: Contient les types d’entrée inscrits pour une transformation de Media Foundation (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: Attribut MFT_INPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c42a051c124cdb96e57ea239c02ebaa47f22e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527916"
---
# <a name="mft_input_types_attributes-attribute"></a><span data-ttu-id="8d3b8-103">\_Attribut des \_ attributs des types d’entrée MFT \_</span><span class="sxs-lookup"><span data-stu-id="8d3b8-103">MFT\_INPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="8d3b8-104">Contient les types d’entrée inscrits pour une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="8d3b8-104">Contains the registered input types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="8d3b8-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8d3b8-105">Data type</span></span>

<span data-ttu-id="8d3b8-106">**MFT \_ Enregistrer \_ les \_ \[ informations \] de type** stockées en tant qu' **octets \[ \]**</span><span class="sxs-lookup"><span data-stu-id="8d3b8-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="8d3b8-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="8d3b8-107">Get/set</span></span>

<span data-ttu-id="8d3b8-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="8d3b8-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="8d3b8-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="8d3b8-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="8d3b8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8d3b8-110">Remarks</span></span>

<span data-ttu-id="8d3b8-111">Cet attribut est défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="8d3b8-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="8d3b8-112">Cet attribut contient un tableau de structures d' [**\_ informations de \_ type \_ de Registre MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) qui décrivent un ou plusieurs formats d’entrée pris en charge par la table MFT.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-112">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more input formats supported by the MFT.</span></span> <span data-ttu-id="8d3b8-113">Ces valeurs sont extraites du Registre et sont destinées à l’application.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-113">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="8d3b8-114">La table MFT peut prendre en charge des formats supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-114">The MFT might support additional formats.</span></span> <span data-ttu-id="8d3b8-115">Pour définir le format d’entrée réel, vous devez créer la table MFT et appeler [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="8d3b8-115">To set the actual input format, you must create the MFT and call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="8d3b8-116">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8d3b8-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d3b8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d3b8-117">Requirements</span></span>



| <span data-ttu-id="8d3b8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d3b8-118">Requirement</span></span> | <span data-ttu-id="8d3b8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d3b8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d3b8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d3b8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d3b8-121">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8d3b8-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="8d3b8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d3b8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d3b8-123">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8d3b8-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8d3b8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d3b8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d3b8-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d3b8-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d3b8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d3b8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d3b8-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8d3b8-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8d3b8-128">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="8d3b8-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




