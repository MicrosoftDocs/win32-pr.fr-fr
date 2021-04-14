---
description: Contient un pointeur vers l’interface IMFMediaEngineExtension.
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: Attribut MF_MEDIA_ENGINE_EXTENSION (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104393863"
---
# <a name="mf_media_engine_extension-attribute"></a><span data-ttu-id="60b31-103">\_Attribut d' \_ extension du moteur multimédia MF \_</span><span class="sxs-lookup"><span data-stu-id="60b31-103">MF\_MEDIA\_ENGINE\_EXTENSION attribute</span></span>

<span data-ttu-id="60b31-104">Contient un pointeur vers l’interface [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .</span><span class="sxs-lookup"><span data-stu-id="60b31-104">Contains a pointer to the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="60b31-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="60b31-105">Data type</span></span>

<span data-ttu-id="60b31-106">**IMFMediaEngineExtension \* *_ stocké en tant que _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="60b31-106">**IMFMediaEngineExtension\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="60b31-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="60b31-107">Get/set</span></span>

<span data-ttu-id="60b31-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="60b31-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="60b31-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="60b31-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="60b31-110">Notes</span><span class="sxs-lookup"><span data-stu-id="60b31-110">Remarks</span></span>

<span data-ttu-id="60b31-111">Cet attribut est utilisé avec la méthode [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) pour initialiser le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="60b31-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="60b31-112">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="60b31-112">This attribute is optional.</span></span> <span data-ttu-id="60b31-113">Utilisez-le pour fournir un objet qui implémente l’interface [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .</span><span class="sxs-lookup"><span data-stu-id="60b31-113">Use it to provide an object that implements the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span> <span data-ttu-id="60b31-114">Cette interface permet à l’application de charger des ressources multimédias personnalisées.</span><span class="sxs-lookup"><span data-stu-id="60b31-114">This interface enables the application to load custom media resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b31-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60b31-115">Requirements</span></span>



| <span data-ttu-id="60b31-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60b31-116">Requirement</span></span> | <span data-ttu-id="60b31-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="60b31-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b31-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60b31-118">Minimum supported client</span></span><br/> | <span data-ttu-id="60b31-119">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="60b31-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="60b31-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60b31-120">Minimum supported server</span></span><br/> | <span data-ttu-id="60b31-121">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="60b31-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="60b31-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="60b31-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="60b31-123"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="60b31-123"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b31-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60b31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b31-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60b31-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




