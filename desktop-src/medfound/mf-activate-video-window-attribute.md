---
description: Handle vers la fenêtre de découpage vidéo.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: Attribut MF_ACTIVATE_VIDEO_WINDOW (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521825"
---
# <a name="mf_activate_video_window-attribute"></a><span data-ttu-id="7c77e-103">\_Attribut de \_ fenêtre vidéo d’activation MF \_</span><span class="sxs-lookup"><span data-stu-id="7c77e-103">MF\_ACTIVATE\_VIDEO\_WINDOW attribute</span></span>

<span data-ttu-id="7c77e-104">Handle vers la fenêtre de découpage vidéo.</span><span class="sxs-lookup"><span data-stu-id="7c77e-104">Handle to the video clipping window.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c77e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7c77e-105">Data type</span></span>

<span data-ttu-id="7c77e-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="7c77e-106">**UINT64**</span></span>

<span data-ttu-id="7c77e-107">Traiter en tant que **\_ pointeur DWORD** (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="7c77e-107">Treat as **DWORD\_PTR** (**HWND**).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c77e-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7c77e-108">Remarks</span></span>

<span data-ttu-id="7c77e-109">Cet attribut s’applique à l’objet d’activation pour le convertisseur vidéo amélioré (EVR).</span><span class="sxs-lookup"><span data-stu-id="7c77e-109">This attribute applies to the activation object for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="7c77e-110">La valeur est définie automatiquement quand vous appelez [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer l’objet d’activation EVR.</span><span class="sxs-lookup"><span data-stu-id="7c77e-110">The value is set automatically when you call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the EVR activation object.</span></span>

<span data-ttu-id="7c77e-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7c77e-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c77e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c77e-112">Requirements</span></span>



| <span data-ttu-id="7c77e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c77e-113">Requirement</span></span> | <span data-ttu-id="7c77e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c77e-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c77e-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c77e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7c77e-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c77e-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7c77e-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c77e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7c77e-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c77e-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7c77e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c77e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c77e-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c77e-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c77e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c77e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c77e-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c77e-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c77e-123">Attributs de convertisseur vidéo améliorés</span><span class="sxs-lookup"><span data-stu-id="7c77e-123">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c77e-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="7c77e-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="7c77e-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="7c77e-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="7c77e-126">Objets d’activation</span><span class="sxs-lookup"><span data-stu-id="7c77e-126">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




