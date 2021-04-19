---
description: Contient un pointeur vers l’interface de rappel pour le moteur multimédia.
ms.assetid: 5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D
title: Attribut MF_MEDIA_ENGINE_CALLBACK (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173e22f9d87f4a77f9ed4a1d1b405fc040bd32b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106532355"
---
# <a name="mf_media_engine_callback-attribute"></a><span data-ttu-id="e58ed-103">\_Attribut de \_ rappel du moteur multimédia MF \_</span><span class="sxs-lookup"><span data-stu-id="e58ed-103">MF\_MEDIA\_ENGINE\_CALLBACK attribute</span></span>

<span data-ttu-id="e58ed-104">Contient un pointeur vers l’interface de rappel pour le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="e58ed-104">Contains a pointer to the callback interface for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="e58ed-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e58ed-105">Data type</span></span>

<span data-ttu-id="e58ed-106">**IMFMediaEngineNotify \* *_ stocké en tant que _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="e58ed-106">**IMFMediaEngineNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="e58ed-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="e58ed-107">Get/set</span></span>

<span data-ttu-id="e58ed-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="e58ed-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="e58ed-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="e58ed-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="e58ed-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e58ed-110">Remarks</span></span>

<span data-ttu-id="e58ed-111">La valeur de cet attribut est un pointeur vers l’interface [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) , implémentée par l’application.</span><span class="sxs-lookup"><span data-stu-id="e58ed-111">The value of this attribute is a pointer to the [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) interface, implemented by the application.</span></span>

<span data-ttu-id="e58ed-112">Cet attribut est utilisé avec la méthode [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) pour initialiser le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="e58ed-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="e58ed-113">L’attribut est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e58ed-113">The attribute is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="e58ed-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e58ed-114">Requirements</span></span>



| <span data-ttu-id="e58ed-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e58ed-115">Requirement</span></span> | <span data-ttu-id="e58ed-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e58ed-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e58ed-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e58ed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e58ed-118">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e58ed-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="e58ed-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e58ed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e58ed-120">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="e58ed-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="e58ed-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e58ed-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e58ed-122"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="e58ed-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e58ed-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e58ed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e58ed-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e58ed-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e58ed-125">**IMFMediaEngineClassFactory :: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="e58ed-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> <dt>

[<span data-ttu-id="e58ed-126">**IMFMediaEngineNotify**</span><span class="sxs-lookup"><span data-stu-id="e58ed-126">**IMFMediaEngineNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)
</dt> </dl>

 

 




