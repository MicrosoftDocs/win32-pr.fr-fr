---
description: Spécifie comment créer un présentateur personnalisé pour le convertisseur vidéo amélioré (EVR).
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3681edaed39b63b0f7c13313039f1c6e72311a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034831"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a><span data-ttu-id="ae3dc-103">\_ \_ \_ \_ Attribut indicateurs de présentateur vidéo personnalisé MF activé \_</span><span class="sxs-lookup"><span data-stu-id="ae3dc-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_FLAGS attribute</span></span>

<span data-ttu-id="ae3dc-104">Spécifie comment créer un présentateur personnalisé pour le convertisseur vidéo amélioré (EVR).</span><span class="sxs-lookup"><span data-stu-id="ae3dc-104">Specifies how to create a custom presenter for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="ae3dc-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ae3dc-105">Data type</span></span>

<span data-ttu-id="ae3dc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ae3dc-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ae3dc-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ae3dc-107">Remarks</span></span>

<span data-ttu-id="ae3dc-108">Vous pouvez définir cet attribut sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) obtenu à partir de la fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="ae3dc-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="ae3dc-109">La valeur de cet attribut est **une opération or au niveau du bit** des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ae3dc-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="ae3dc-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae3dc-110">Value</span></span>                                          | <span data-ttu-id="ae3dc-111">Description</span><span class="sxs-lookup"><span data-stu-id="ae3dc-111">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae3dc-112">**MF \_ activer \_ le \_ présentateur personnalisé \_ ALLOWFAIL**</span><span class="sxs-lookup"><span data-stu-id="ae3dc-112">**MF\_ACTIVATE\_CUSTOM\_PRESENTER\_ALLOWFAIL**</span></span> | <span data-ttu-id="ae3dc-113">Si la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ne parvient pas à créer le présentateur personnalisé de l’application, il utilise à la place le présentateur EVR par défaut.</span><span class="sxs-lookup"><span data-stu-id="ae3dc-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom presenter, it uses the default EVR presenter instead.</span></span> <span data-ttu-id="ae3dc-114">Par défaut, si l’objet [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) échoue lorsqu’il tente de créer le présentateur personnalisé, la méthode **ActivateObject** échoue.</span><span class="sxs-lookup"><span data-stu-id="ae3dc-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom presenter, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="ae3dc-115">Les applications peuvent utiliser l’attribut de [**\_ CLSID d’activation de \_ \_ vidéo \_ \_ personnalisée MF**](mf-activate-custom-video-presenter-clsid-attribute.md) pour spécifier un présentateur personnalisé pour le EVR.</span><span class="sxs-lookup"><span data-stu-id="ae3dc-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md) attribute to specify a custom presenter for the EVR.</span></span>

<span data-ttu-id="ae3dc-116">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ae3dc-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae3dc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae3dc-117">Requirements</span></span>



| <span data-ttu-id="ae3dc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae3dc-118">Requirement</span></span> | <span data-ttu-id="ae3dc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae3dc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae3dc-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae3dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae3dc-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae3dc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ae3dc-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae3dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae3dc-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae3dc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ae3dc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae3dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae3dc-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae3dc-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae3dc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae3dc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae3dc-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae3dc-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae3dc-128">Attributs de convertisseur vidéo améliorés</span><span class="sxs-lookup"><span data-stu-id="ae3dc-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae3dc-129">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ae3dc-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ae3dc-130">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ae3dc-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ae3dc-131">Objets d’activation</span><span class="sxs-lookup"><span data-stu-id="ae3dc-131">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="ae3dc-132">Comment écrire un présentateur EVR</span><span class="sxs-lookup"><span data-stu-id="ae3dc-132">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




