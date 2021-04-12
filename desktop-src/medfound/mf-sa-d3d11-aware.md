---
description: Spécifie si une Media Foundation transformation (MFT) prend en charge Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: Attribut MF_SA_D3D11_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318646"
---
# <a name="mf_sa_d3d11_aware-attribute"></a><span data-ttu-id="43058-103">\_ \_ Attribut sensible sa d3d11 MF \_</span><span class="sxs-lookup"><span data-stu-id="43058-103">MF\_SA\_D3D11\_AWARE attribute</span></span>

<span data-ttu-id="43058-104">Spécifie si une Media Foundation transformation (MFT) prend en charge Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="43058-104">Specifies whether a Media Foundation transform (MFT) supports Microsoft Direct3D 11.</span></span>

## <a name="data-type"></a><span data-ttu-id="43058-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="43058-105">Data type</span></span>

<span data-ttu-id="43058-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43058-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="43058-107">Notes</span><span class="sxs-lookup"><span data-stu-id="43058-107">Remarks</span></span>

<span data-ttu-id="43058-108">Cet attribut s’applique uniquement à la vidéo MFTs.</span><span class="sxs-lookup"><span data-stu-id="43058-108">This attribute applies only to video MFTs.</span></span> <span data-ttu-id="43058-109">Pour interroger cet attribut, appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour obtenir le magasin d’attributs MFT.</span><span class="sxs-lookup"><span data-stu-id="43058-109">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT attribute store.</span></span> <span data-ttu-id="43058-110">Si la condition **GetAttributes** est établie, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="43058-110">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

-   <span data-ttu-id="43058-111">Si l’attribut est différent de zéro, le client peut attribuer à la MFT un pointeur vers l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) avant le démarrage de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="43058-111">If the attribute is nonzero, the client can give the MFT a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface before streaming starts.</span></span> <span data-ttu-id="43058-112">Pour ce faire, le client envoie le message du [**\_ \_ \_ \_ Gestionnaire D3D du jeu de messages MFT**](mft-message-set-d3d-manager.md) au MFT.</span><span class="sxs-lookup"><span data-stu-id="43058-112">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="43058-113">Le client n’est pas obligé d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="43058-113">The client is not required to send this message.</span></span>
-   <span data-ttu-id="43058-114">Si cet attribut est égal à zéro (**false**), la table MFT ne prend pas en charge Direct3D 11 et le client ne doit pas envoyer le message du [**\_ \_ \_ \_ Gestionnaire D3D de la définition de message MFT**](mft-message-set-d3d-manager.md) à la MFT.</span><span class="sxs-lookup"><span data-stu-id="43058-114">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 11, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="43058-115">La valeur par défaut de cet attribut est **false**.</span><span class="sxs-lookup"><span data-stu-id="43058-115">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="43058-116">Traiter cet attribut comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="43058-116">Treat this attribute as read-only.</span></span> <span data-ttu-id="43058-117">Ne modifiez pas la valeur ; la table MFT ignore toute modification apportée à la valeur.</span><span class="sxs-lookup"><span data-stu-id="43058-117">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="43058-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43058-118">Requirements</span></span>



| <span data-ttu-id="43058-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43058-119">Requirement</span></span> | <span data-ttu-id="43058-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="43058-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43058-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43058-121">Minimum supported client</span></span><br/> | <span data-ttu-id="43058-122">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="43058-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="43058-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43058-123">Minimum supported server</span></span><br/> | <span data-ttu-id="43058-124">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="43058-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="43058-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="43058-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="43058-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="43058-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43058-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43058-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43058-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="43058-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="43058-129">Prise en charge du décodage vidéo Direct3D 11 dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="43058-129">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




