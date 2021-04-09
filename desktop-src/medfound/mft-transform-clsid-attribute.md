---
description: Contient l’identificateur de classe (CLSID) d’une transformation de Media Foundation (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: Attribut MFT_TRANSFORM_CLSID_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951485"
---
# <a name="mft_transform_clsid_attribute-attribute"></a><span data-ttu-id="901b0-103">Attribut de l' \_ \_ attribut CLSID de transformation MFT \_</span><span class="sxs-lookup"><span data-stu-id="901b0-103">MFT\_TRANSFORM\_CLSID\_Attribute attribute</span></span>

<span data-ttu-id="901b0-104">Contient l’identificateur de classe (CLSID) d’une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="901b0-104">Contains the class identifier (CLSID) of a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="901b0-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="901b0-105">Data type</span></span>

<span data-ttu-id="901b0-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="901b0-106">**GUID**</span></span>

## <a name="getset"></a><span data-ttu-id="901b0-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="901b0-107">Get/set</span></span>

<span data-ttu-id="901b0-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="901b0-108">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="901b0-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="901b0-109">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="901b0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="901b0-110">Remarks</span></span>

<span data-ttu-id="901b0-111">Cet attribut est défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="901b0-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="901b0-112">Cet attribut est utilisé en interne par l’objet d’activation lorsqu’il crée la table MFT.</span><span class="sxs-lookup"><span data-stu-id="901b0-112">This attribute is used internally by the activation object when it creates the MFT.</span></span> <span data-ttu-id="901b0-113">Les applications ne doivent pas utiliser ce CLSID directement pour créer la table MFT, car il se peut que l’objet d’activation doive initialiser la table MFT.</span><span class="sxs-lookup"><span data-stu-id="901b0-113">Applications should not use this CLSID directly to create the MFT, because the activation object might need to initialize the MFT.</span></span> <span data-ttu-id="901b0-114">Par conséquent, pour créer une instance de la MFT, appelez [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sur l’objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="901b0-114">Therefore, to create an instance of the MFT, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the activation object.</span></span>

<span data-ttu-id="901b0-115">Notez que la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) se comporte différemment de la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) à cet égard.</span><span class="sxs-lookup"><span data-stu-id="901b0-115">Note that the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function behaves differently than the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function in this respect.</span></span> <span data-ttu-id="901b0-116">La fonction **MFTEnum** retourne des CLSID, que l’application transmet à la fonction **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="901b0-116">The **MFTEnum** function returns CLSIDs, which the application passes to the **CoCreateInstance** function.</span></span> <span data-ttu-id="901b0-117">La fonction **MFTEnumEx** retourne des objets d’activation plutôt que des CLSID.</span><span class="sxs-lookup"><span data-stu-id="901b0-117">The **MFTEnumEx** function returns activation objects rather than CLSIDs.</span></span>

<span data-ttu-id="901b0-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="901b0-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="901b0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="901b0-119">Requirements</span></span>



| <span data-ttu-id="901b0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="901b0-120">Requirement</span></span> | <span data-ttu-id="901b0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="901b0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="901b0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="901b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="901b0-123">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="901b0-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="901b0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="901b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="901b0-125">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="901b0-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="901b0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="901b0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="901b0-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="901b0-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="901b0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="901b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="901b0-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="901b0-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="901b0-130">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="901b0-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




