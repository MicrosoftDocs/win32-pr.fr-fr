---
description: Spécifie si une Media Foundation transformation (MFT) prend en charge les modifications de format dynamiques.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: Attribut MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529149"
---
# <a name="mft_support_dynamic_format_change-attribute"></a><span data-ttu-id="0eca7-103">\_Attribut de \_ \_ modification du format dynamique \_ de la MFT</span><span class="sxs-lookup"><span data-stu-id="0eca7-103">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE attribute</span></span>

<span data-ttu-id="0eca7-104">Spécifie si une Media Foundation transformation (MFT) prend en charge les modifications de format dynamiques.</span><span class="sxs-lookup"><span data-stu-id="0eca7-104">Specifies whether a Media Foundation transform (MFT) supports dynamic format changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="0eca7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0eca7-105">Data type</span></span>

<span data-ttu-id="0eca7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0eca7-106">**UINT32**</span></span>

<span data-ttu-id="0eca7-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="0eca7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eca7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0eca7-108">Remarks</span></span>

<span data-ttu-id="0eca7-109">Cet attribut peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0eca7-109">This attribute can have the following values.</span></span>



| <span data-ttu-id="0eca7-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="0eca7-110">Value</span></span>     | <span data-ttu-id="0eca7-111">Description</span><span class="sxs-lookup"><span data-stu-id="0eca7-111">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="0eca7-112">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="0eca7-112">**TRUE**</span></span>  | <span data-ttu-id="0eca7-113">Le client peut modifier le format d’entrée pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="0eca7-113">The client can change the input format during streaming.</span></span>               |
| <span data-ttu-id="0eca7-114">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="0eca7-114">**FALSE**</span></span> | <span data-ttu-id="0eca7-115">La table MFT doit être vidée pour que le client puisse modifier le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0eca7-115">The MFT must be drained before the client can change the input format.</span></span> |



 

<span data-ttu-id="0eca7-116">Pour obtenir cet attribut, appelez d’abord [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour obtenir le magasin d’attributs global pour la table MFT.</span><span class="sxs-lookup"><span data-stu-id="0eca7-116">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store for the MFT.</span></span> <span data-ttu-id="0eca7-117">Appelez ensuite [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) pour récupérer la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="0eca7-117">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span>

<span data-ttu-id="0eca7-118">Si [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) échoue ou si l’attribut n’est pas présent, la valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="0eca7-118">If [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) fails or the attribute is not present, the default value if **FALSE**.</span></span>

<span data-ttu-id="0eca7-119">Un [MFTS asynchrone](asynchronous-mfts.md) doit retourner la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="0eca7-119">[Asynchronous MFTs](asynchronous-mfts.md) must return the value **TRUE**.</span></span>

<span data-ttu-id="0eca7-120">Pour plus d’informations, consultez [gestion des modifications de flux](handling-stream-changes.md).</span><span class="sxs-lookup"><span data-stu-id="0eca7-120">For more information, see [Handling Stream Changes](handling-stream-changes.md).</span></span>

<span data-ttu-id="0eca7-121">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0eca7-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eca7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0eca7-122">Requirements</span></span>



| <span data-ttu-id="0eca7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0eca7-123">Requirement</span></span> | <span data-ttu-id="0eca7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0eca7-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0eca7-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eca7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0eca7-126">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="0eca7-126">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0eca7-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eca7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0eca7-128">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="0eca7-128">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0eca7-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0eca7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eca7-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eca7-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eca7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0eca7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eca7-132">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0eca7-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0eca7-133">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="0eca7-133">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="0eca7-134">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="0eca7-134">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="0eca7-135">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0eca7-135">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0eca7-136">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0eca7-136">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0eca7-137">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="0eca7-137">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




