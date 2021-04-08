---
description: Spécifie comment créer un mélangeur personnalisé pour le convertisseur vidéo amélioré (EVR).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757869"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a><span data-ttu-id="ab16b-103">\_Attribut d' \_ \_ indicateur de \_ mélangeur vidéo personnalisé MF activé \_</span><span class="sxs-lookup"><span data-stu-id="ab16b-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_FLAGS attribute</span></span>

<span data-ttu-id="ab16b-104">Spécifie comment créer un mélangeur personnalisé pour le convertisseur vidéo amélioré (EVR).</span><span class="sxs-lookup"><span data-stu-id="ab16b-104">Specifies how to create a custom mixer for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="ab16b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ab16b-105">Data type</span></span>

<span data-ttu-id="ab16b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ab16b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ab16b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ab16b-107">Remarks</span></span>

<span data-ttu-id="ab16b-108">Vous pouvez définir cet attribut sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) obtenu à partir de la fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="ab16b-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="ab16b-109">La valeur de cet attribut est **une opération or au niveau du bit** des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ab16b-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="ab16b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab16b-110">Value</span></span>                                      | <span data-ttu-id="ab16b-111">Description</span><span class="sxs-lookup"><span data-stu-id="ab16b-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab16b-112">**\_ALLOWFAIL de \_ \_ mixage personnalisé \_ MF MF**</span><span class="sxs-lookup"><span data-stu-id="ab16b-112">**MF\_ACTIVATE\_CUSTOM\_MIXER\_ALLOWFAIL**</span></span> | <span data-ttu-id="ab16b-113">Si la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ne parvient pas à créer le mélangeur personnalisé de l’application, elle utilise à la place le mélangeur EVR par défaut.</span><span class="sxs-lookup"><span data-stu-id="ab16b-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom mixer, it uses the default EVR mixer instead.</span></span> <span data-ttu-id="ab16b-114">Par défaut, si l’objet [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) échoue lors de la tentative de création du mélangeur personnalisé, la méthode **ActivateObject** échoue.</span><span class="sxs-lookup"><span data-stu-id="ab16b-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom mixer, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="ab16b-115">Les applications peuvent utiliser l’attribut [**\_ \_ \_ \_ \_ CLSID du mélangeur vidéo personnalisé MF activer**](mf-activate-custom-video-mixer-clsid-attribute.md) pour spécifier un mélangeur personnalisé pour le EVR.</span><span class="sxs-lookup"><span data-stu-id="ab16b-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) attribute to specify a custom mixer for the EVR.</span></span>

<span data-ttu-id="ab16b-116">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ab16b-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab16b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab16b-117">Requirements</span></span>



| <span data-ttu-id="ab16b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab16b-118">Requirement</span></span> | <span data-ttu-id="ab16b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab16b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab16b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab16b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab16b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab16b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ab16b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab16b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab16b-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab16b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ab16b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab16b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab16b-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab16b-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab16b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab16b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab16b-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab16b-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ab16b-128">Attributs de convertisseur vidéo améliorés</span><span class="sxs-lookup"><span data-stu-id="ab16b-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ab16b-129">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ab16b-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ab16b-130">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ab16b-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ab16b-131">Objets d’activation</span><span class="sxs-lookup"><span data-stu-id="ab16b-131">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




