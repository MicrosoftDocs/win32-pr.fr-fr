---
description: CLSID d’un mélangeur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318554"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a><span data-ttu-id="8f75a-103">\_ \_ \_ \_ Attribut CLSID du mélangeur vidéo personnalisé MF activé \_</span><span class="sxs-lookup"><span data-stu-id="8f75a-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID attribute</span></span>

<span data-ttu-id="8f75a-104">CLSID d’un mélangeur vidéo personnalisé pour le récepteur multimédia EVR (Enhanced Video Renderer).</span><span class="sxs-lookup"><span data-stu-id="8f75a-104">CLSID of a custom video mixer for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="8f75a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8f75a-105">Data type</span></span>

<span data-ttu-id="8f75a-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="8f75a-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="8f75a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8f75a-107">Remarks</span></span>

<span data-ttu-id="8f75a-108">Si vous créez le EVR via un objet d’activation, vous pouvez utiliser cet attribut pour définir une console de mixage vidéo personnalisée sur EVR.</span><span class="sxs-lookup"><span data-stu-id="8f75a-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video mixer on the EVR.</span></span> <span data-ttu-id="8f75a-109">Utilisez cet attribut comme suit :</span><span class="sxs-lookup"><span data-stu-id="8f75a-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="8f75a-110">Appelez la fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer un objet d’activation pour EVR.</span><span class="sxs-lookup"><span data-stu-id="8f75a-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="8f75a-111">La fonction retourne un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="8f75a-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="8f75a-112">Définissez ce du sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) en appelant [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="8f75a-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="8f75a-113">La valeur de l’attribut est le CLSID du mélangeur vidéo personnalisé de l’application.</span><span class="sxs-lookup"><span data-stu-id="8f75a-113">The value of the attribute is the CLSID of the application's custom video mixer.</span></span>

<span data-ttu-id="8f75a-114">Si cet attribut est défini, EVR appelle **CoCreateInstance** avec le CLSID spécifié pour créer le mélangeur vidéo personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8f75a-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video mixer.</span></span> <span data-ttu-id="8f75a-115">Le mixer vidéo doit exposer l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="8f75a-115">The video mixer must expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="8f75a-116">Le mélangeur est créé en tant que serveur COM in-process.</span><span class="sxs-lookup"><span data-stu-id="8f75a-116">The mixer is created as an in-process COM server.</span></span>

<span data-ttu-id="8f75a-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8f75a-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f75a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f75a-118">Requirements</span></span>



| <span data-ttu-id="8f75a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f75a-119">Requirement</span></span> | <span data-ttu-id="8f75a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f75a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f75a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f75a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8f75a-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f75a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8f75a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f75a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8f75a-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f75a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8f75a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f75a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f75a-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f75a-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f75a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f75a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f75a-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8f75a-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8f75a-129">Attributs de convertisseur vidéo améliorés</span><span class="sxs-lookup"><span data-stu-id="8f75a-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="8f75a-130">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="8f75a-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="8f75a-131">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="8f75a-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="8f75a-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="8f75a-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="8f75a-133">Objets d’activation</span><span class="sxs-lookup"><span data-stu-id="8f75a-133">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




