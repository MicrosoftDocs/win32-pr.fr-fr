---
description: Définit l’Gestionnaire de périphériques de l’infrastructure Microsoft DirectX Graphics (DXGI) sur le moteur multimédia.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: Attribut MF_MEDIA_ENGINE_DXGI_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523749"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a><span data-ttu-id="8c945-103">\_Attribut du \_ \_ Gestionnaire de dxgi du moteur multimédia MF \_</span><span class="sxs-lookup"><span data-stu-id="8c945-103">MF\_MEDIA\_ENGINE\_DXGI\_MANAGER attribute</span></span>

<span data-ttu-id="8c945-104">Définit l’Gestionnaire de périphériques de l’infrastructure Microsoft DirectX Graphics (DXGI) sur le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="8c945-104">Sets the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="8c945-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8c945-105">Data type</span></span>

<span data-ttu-id="8c945-106">**IMFDXGIDeviceManager \* *_ stocké en tant que _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="8c945-106">**IMFDXGIDeviceManager\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="8c945-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="8c945-107">Get/set</span></span>

<span data-ttu-id="8c945-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="8c945-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="8c945-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="8c945-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="8c945-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8c945-110">Remarks</span></span>

<span data-ttu-id="8c945-111">La valeur de cet attribut est un pointeur vers l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="8c945-111">The value of this attribute is a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="8c945-112">En mode serveur Frame, cet attribut permet au moteur multimédia d’utiliser l’accélération matérielle pour le décodage vidéo et le traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="8c945-112">In frame-server mode, this attribute enables the Media Engine to use hardware acceleration for video decoding and video processing.</span></span> <span data-ttu-id="8c945-113">Si l’attribut n’est pas défini, le moteur multimédia utilise le décodage et le traitement des logiciels.</span><span class="sxs-lookup"><span data-stu-id="8c945-113">If the attribute is not set, the Media Engine uses software decoding and processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c945-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c945-114">Requirements</span></span>



| <span data-ttu-id="8c945-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c945-115">Requirement</span></span> | <span data-ttu-id="8c945-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c945-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c945-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c945-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c945-118">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8c945-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="8c945-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c945-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c945-120">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="8c945-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="8c945-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c945-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c945-122"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c945-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c945-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c945-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c945-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8c945-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8c945-125">**IMFMediaEngineClassFactory :: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="8c945-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




