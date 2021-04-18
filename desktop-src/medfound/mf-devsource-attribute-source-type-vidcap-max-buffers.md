---
description: Spécifie le nombre maximal de trames que la source de capture vidéo va mettre en mémoire tampon.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519344"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a><span data-ttu-id="7ef7e-103">\_Attribut MF DEVSOURCE \_ type de \_ source \_ \_ VIDCAP \_ Max \_ buffers</span><span class="sxs-lookup"><span data-stu-id="7ef7e-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_MAX\_BUFFERS attribute</span></span>

<span data-ttu-id="7ef7e-104">Spécifie le nombre maximal de trames que la source de capture vidéo va mettre en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7ef7e-104">Specifies the maximum number of frames that the video capture source will buffer.</span></span>

## <a name="data-type"></a><span data-ttu-id="7ef7e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7ef7e-105">Data type</span></span>

<span data-ttu-id="7ef7e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7ef7e-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7ef7e-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="7ef7e-107">Get/set</span></span>

<span data-ttu-id="7ef7e-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7ef7e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7ef7e-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7ef7e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ef7e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7ef7e-110">Remarks</span></span>

<span data-ttu-id="7ef7e-111">Par défaut, la source de capture vidéo met en mémoire tampon un maximum d’une image à la fois.</span><span class="sxs-lookup"><span data-stu-id="7ef7e-111">By default, the video capture source buffers a maximum of one frame at a time.</span></span> <span data-ttu-id="7ef7e-112">Vous pouvez augmenter la limite de la mémoire tampon en définissant cet attribut.</span><span class="sxs-lookup"><span data-stu-id="7ef7e-112">You can increase the buffer limit by setting this attribute.</span></span>

<span data-ttu-id="7ef7e-113">La méthode correcte pour définir cet attribut dépend de la fonction utilisée pour créer la source du média :</span><span class="sxs-lookup"><span data-stu-id="7ef7e-113">The correct way to set this attribute depends on the function used to create the media source:</span></span>

-   <span data-ttu-id="7ef7e-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): définissez l’attribut par le biais du paramètre *pAttributes* de la fonction.</span><span class="sxs-lookup"><span data-stu-id="7ef7e-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="7ef7e-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): définissez l’attribut par le biais du paramètre *pAttributes* de la fonction.</span><span class="sxs-lookup"><span data-stu-id="7ef7e-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="7ef7e-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): définissez l’attribut sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retourné par la fonction.</span><span class="sxs-lookup"><span data-stu-id="7ef7e-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Set the attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned by the function.</span></span> <span data-ttu-id="7ef7e-117">Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="7ef7e-117">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="7ef7e-118">L’attribut s’applique uniquement aux périphériques de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="7ef7e-118">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="7ef7e-119">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7ef7e-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ef7e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ef7e-120">Requirements</span></span>



| <span data-ttu-id="7ef7e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ef7e-121">Requirement</span></span> | <span data-ttu-id="7ef7e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ef7e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef7e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ef7e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7ef7e-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ef7e-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7ef7e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ef7e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7ef7e-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ef7e-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7ef7e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ef7e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ef7e-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ef7e-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ef7e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ef7e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ef7e-130">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7ef7e-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7ef7e-131">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="7ef7e-131">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="7ef7e-132">Capturer les attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="7ef7e-132">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




