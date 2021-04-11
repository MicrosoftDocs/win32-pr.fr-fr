---
description: Spécifie un objet d’activation qui crée un présentateur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).
ms.assetid: 65d88832-0969-4d85-bee2-fd0aa68e9f3b
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75855c18faba8568547f9efcfb19e04574c4885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318818"
---
# <a name="mf_activate_custom_video_presenter_activate-attribute"></a><span data-ttu-id="e2ad2-103">\_Activer l' \_ attribut \_ d' \_ activation de PRÉSENTateur vidéo personnalisé \_ MF</span><span class="sxs-lookup"><span data-stu-id="e2ad2-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_ACTIVATE attribute</span></span>

<span data-ttu-id="e2ad2-104">Spécifie un objet d’activation qui crée un présentateur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).</span><span class="sxs-lookup"><span data-stu-id="e2ad2-104">Specifies an activation object that creates a custom video presenter for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="e2ad2-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e2ad2-105">Data type</span></span>

<span data-ttu-id="e2ad2-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="e2ad2-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="e2ad2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e2ad2-107">Remarks</span></span>

<span data-ttu-id="e2ad2-108">Si vous créez le EVR via un objet d’activation, vous pouvez utiliser cet attribut pour définir un présentateur vidéo personnalisé sur EVR.</span><span class="sxs-lookup"><span data-stu-id="e2ad2-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video presenter on the EVR.</span></span> <span data-ttu-id="e2ad2-109">Utilisez cet attribut comme suit :</span><span class="sxs-lookup"><span data-stu-id="e2ad2-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="e2ad2-110">Appelez la fonction [_ *MFCreateVideoRendererActivate* \*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer un objet d’activation pour EVR.</span><span class="sxs-lookup"><span data-stu-id="e2ad2-110">Call the [_ *MFCreateVideoRendererActivate*\*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="e2ad2-111">La fonction retourne un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="e2ad2-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="e2ad2-112">Définissez cet attribut sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) en appelant [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="e2ad2-112">Set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span> <span data-ttu-id="e2ad2-113">La valeur de l’attribut est un pointeur vers un objet d’activation implémenté par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e2ad2-113">The value of the attribute is a pointer to an activation object implemented by the caller.</span></span> <span data-ttu-id="e2ad2-114">L’objet d’activation de l’appelant doit exposer l’interface **IMFActivate** .</span><span class="sxs-lookup"><span data-stu-id="e2ad2-114">The caller's activation object must expose the **IMFActivate** interface.</span></span>

<span data-ttu-id="e2ad2-115">Si vous définissez cet attribut, EVR appelle [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pour créer le présentateur vidéo personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e2ad2-115">If you set this attribute, the EVR calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the custom video presenter.</span></span> <span data-ttu-id="e2ad2-116">Le présentateur vidéo doit exposer l’interface [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) .</span><span class="sxs-lookup"><span data-stu-id="e2ad2-116">The video presenter must expose the [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface.</span></span>

<span data-ttu-id="e2ad2-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e2ad2-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ad2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2ad2-118">Requirements</span></span>



| <span data-ttu-id="e2ad2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2ad2-119">Requirement</span></span> | <span data-ttu-id="e2ad2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2ad2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ad2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2ad2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e2ad2-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2ad2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e2ad2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2ad2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e2ad2-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2ad2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e2ad2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2ad2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2ad2-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ad2-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2ad2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2ad2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ad2-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2ad2-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2ad2-129">Attributs de convertisseur vidéo améliorés</span><span class="sxs-lookup"><span data-stu-id="e2ad2-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2ad2-130">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="e2ad2-130">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="e2ad2-131">**IMFAttributes :: Setunknown,**</span><span class="sxs-lookup"><span data-stu-id="e2ad2-131">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="e2ad2-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="e2ad2-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="e2ad2-133">Objets d’activation</span><span class="sxs-lookup"><span data-stu-id="e2ad2-133">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="e2ad2-134">Comment écrire un présentateur EVR</span><span class="sxs-lookup"><span data-stu-id="e2ad2-134">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




