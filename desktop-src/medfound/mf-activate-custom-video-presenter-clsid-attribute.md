---
description: CLSID d’un présentateur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0eb913a56671d5d2ac8d27c785e1cc1fbfc51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516916"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a><span data-ttu-id="c2ca1-103">\_ \_ \_ \_ Attribut CLSID du présentateur vidéo personnalisé MF activé \_</span><span class="sxs-lookup"><span data-stu-id="c2ca1-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID attribute</span></span>

<span data-ttu-id="c2ca1-104">CLSID d’un présentateur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).</span><span class="sxs-lookup"><span data-stu-id="c2ca1-104">CLSID of a custom video presenter for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="c2ca1-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="c2ca1-105">Data type</span></span>

<span data-ttu-id="c2ca1-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="c2ca1-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="c2ca1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c2ca1-107">Remarks</span></span>

<span data-ttu-id="c2ca1-108">Si vous créez le EVR via un objet d’activation, vous pouvez utiliser cet attribut pour définir un présentateur vidéo personnalisé sur EVR.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video presenter on the EVR.</span></span> <span data-ttu-id="c2ca1-109">Utilisez cet attribut comme suit :</span><span class="sxs-lookup"><span data-stu-id="c2ca1-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="c2ca1-110">Appelez la fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer un objet d’activation pour EVR.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="c2ca1-111">La fonction retourne un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="c2ca1-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="c2ca1-112">Définissez ce du sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) en appelant [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="c2ca1-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="c2ca1-113">La valeur de l’attribut est le CLSID du présentateur vidéo personnalisé de l’application.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-113">The value of the attribute is the CLSID of the application's custom video presenter.</span></span>

<span data-ttu-id="c2ca1-114">Si cet attribut est défini, EVR appelle **CoCreateInstance** avec le CLSID spécifié pour créer le présentateur vidéo personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video presenter.</span></span> <span data-ttu-id="c2ca1-115">Le présentateur vidéo doit exposer l’interface [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) .</span><span class="sxs-lookup"><span data-stu-id="c2ca1-115">The video presenter must expose the [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface.</span></span> <span data-ttu-id="c2ca1-116">Le présentateur est créé en tant que serveur COM in-process.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-116">The presenter is created as an in-process COM server.</span></span>

<span data-ttu-id="c2ca1-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c2ca1-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2ca1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2ca1-118">Requirements</span></span>



| <span data-ttu-id="c2ca1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2ca1-119">Requirement</span></span> | <span data-ttu-id="c2ca1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2ca1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ca1-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2ca1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ca1-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2ca1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c2ca1-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2ca1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ca1-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2ca1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c2ca1-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2ca1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2ca1-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2ca1-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2ca1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2ca1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ca1-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c2ca1-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2ca1-129">Attributs de convertisseur vidéo améliorés</span><span class="sxs-lookup"><span data-stu-id="c2ca1-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2ca1-130">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="c2ca1-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="c2ca1-131">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="c2ca1-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="c2ca1-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="c2ca1-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="c2ca1-133">Objets d’activation</span><span class="sxs-lookup"><span data-stu-id="c2ca1-133">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="c2ca1-134">Comment écrire un présentateur EVR</span><span class="sxs-lookup"><span data-stu-id="c2ca1-134">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




