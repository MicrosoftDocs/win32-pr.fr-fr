---
description: Spécifie un objet d’activation qui crée un mélangeur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6268f3630b013235f3d365e0b8ab0578c9dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114611"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a><span data-ttu-id="26fe6-103">Activer \_ l' \_ \_ attribut d' \_ activation du MÉLANGEur vidéo personnalisé \_ MF</span><span class="sxs-lookup"><span data-stu-id="26fe6-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_ACTIVATE attribute</span></span>

<span data-ttu-id="26fe6-104">Spécifie un objet d’activation qui crée un mélangeur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).</span><span class="sxs-lookup"><span data-stu-id="26fe6-104">Specifies an activation object that creates a custom video mixer for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="26fe6-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="26fe6-105">Data type</span></span>

<span data-ttu-id="26fe6-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="26fe6-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="26fe6-107">Notes</span><span class="sxs-lookup"><span data-stu-id="26fe6-107">Remarks</span></span>

<span data-ttu-id="26fe6-108">Si vous créez le EVR via un objet d’activation, vous pouvez utiliser cet attribut pour définir une console de mixage vidéo personnalisée sur EVR.</span><span class="sxs-lookup"><span data-stu-id="26fe6-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video mixer on the EVR.</span></span> <span data-ttu-id="26fe6-109">Utilisez cet attribut comme suit :</span><span class="sxs-lookup"><span data-stu-id="26fe6-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="26fe6-110">Appelez la fonction [_ *MFCreateVideoRendererActivate* \*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer un objet d’activation pour EVR.</span><span class="sxs-lookup"><span data-stu-id="26fe6-110">Call the [_ *MFCreateVideoRendererActivate*\*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="26fe6-111">La fonction retourne un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="26fe6-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="26fe6-112">Définissez cet attribut sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) en appelant [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="26fe6-112">Set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span> <span data-ttu-id="26fe6-113">La valeur de l’attribut est un pointeur vers un objet d’activation implémenté par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="26fe6-113">The value of the attribute is a pointer to an activation object implemented by the caller.</span></span> <span data-ttu-id="26fe6-114">L’objet d’activation de l’appelant doit exposer l’interface **IMFActivate** .</span><span class="sxs-lookup"><span data-stu-id="26fe6-114">The caller's activation object must expose the **IMFActivate** interface.</span></span>

<span data-ttu-id="26fe6-115">Si vous définissez cet attribut, EVR appelle [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pour créer le mélangeur vidéo personnalisé.</span><span class="sxs-lookup"><span data-stu-id="26fe6-115">If you set this attribute, the EVR calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the custom video mixer.</span></span> <span data-ttu-id="26fe6-116">Le mixer vidéo doit exposer l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="26fe6-116">The video mixer must expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span>

<span data-ttu-id="26fe6-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="26fe6-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="26fe6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26fe6-118">Requirements</span></span>



| <span data-ttu-id="26fe6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26fe6-119">Requirement</span></span> | <span data-ttu-id="26fe6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="26fe6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26fe6-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26fe6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26fe6-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26fe6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="26fe6-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26fe6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26fe6-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26fe6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="26fe6-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="26fe6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="26fe6-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26fe6-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26fe6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26fe6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26fe6-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26fe6-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="26fe6-129">Attributs de convertisseur vidéo améliorés</span><span class="sxs-lookup"><span data-stu-id="26fe6-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="26fe6-130">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="26fe6-130">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="26fe6-131">**IMFAttributes :: Setunknown,**</span><span class="sxs-lookup"><span data-stu-id="26fe6-131">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="26fe6-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="26fe6-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="26fe6-133">Objets d’activation</span><span class="sxs-lookup"><span data-stu-id="26fe6-133">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




