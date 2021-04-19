---
description: Définit un visuel Microsoft DirectComposition comme région de lecture pour le moteur multimédia.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: Attribut MF_MEDIA_ENGINE_PLAYBACK_VISUAL (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538956"
---
# <a name="mf_media_engine_playback_visual-attribute"></a><span data-ttu-id="2a497-103">\_ \_ \_ Attribut visuel lecture du moteur multimédia MF \_</span><span class="sxs-lookup"><span data-stu-id="2a497-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_VISUAL attribute</span></span>

<span data-ttu-id="2a497-104">Définit un visuel Microsoft DirectComposition comme région de lecture pour le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="2a497-104">Sets a Microsoft DirectComposition visual as the playback region for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="2a497-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2a497-105">Data type</span></span>

<span data-ttu-id="2a497-106">**IDCompositionVisual \* *_ stocké en tant que _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="2a497-106">**IDCompositionVisual\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="2a497-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="2a497-107">Get/set</span></span>

<span data-ttu-id="2a497-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="2a497-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="2a497-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="2a497-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="2a497-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2a497-110">Remarks</span></span>

<span data-ttu-id="2a497-111">Pour plus d’informations sur DirectComposition, consultez [DirectComposition](../directcomp/directcomposition-portal.md) et [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span><span class="sxs-lookup"><span data-stu-id="2a497-111">For more information on DirectComposition, see [DirectComposition](../directcomp/directcomposition-portal.md) and [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span></span>

<span data-ttu-id="2a497-112">Cet attribut est utilisé avec la méthode [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) pour initialiser le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="2a497-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a497-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a497-113">Requirements</span></span>



| <span data-ttu-id="2a497-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a497-114">Requirement</span></span> | <span data-ttu-id="2a497-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a497-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a497-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a497-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2a497-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a497-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="2a497-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a497-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2a497-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a497-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="2a497-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a497-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a497-121"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a497-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a497-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a497-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a497-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a497-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
