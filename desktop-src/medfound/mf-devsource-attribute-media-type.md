---
description: Spécifie le format de sortie d’un appareil.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: Attribut MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106529530"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a><span data-ttu-id="74114-103">\_Attribut de \_ \_ type de média d’attribut DEVSOURCE MF \_</span><span class="sxs-lookup"><span data-stu-id="74114-103">MF\_DEVSOURCE\_ATTRIBUTE\_MEDIA\_TYPE attribute</span></span>

<span data-ttu-id="74114-104">Spécifie le format de sortie d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="74114-104">Specifies the output format of a device.</span></span>

## <a name="data-type"></a><span data-ttu-id="74114-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="74114-105">Data type</span></span>

<span data-ttu-id="74114-106">**[**MFT \_ Enregistrer \_ les \_ informations de type**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** stockées en tant qu' **octets \[ \]**</span><span class="sxs-lookup"><span data-stu-id="74114-106">**[**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="74114-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="74114-107">Get/set</span></span>

<span data-ttu-id="74114-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="74114-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="74114-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="74114-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="74114-110">Notes</span><span class="sxs-lookup"><span data-stu-id="74114-110">Remarks</span></span>

<span data-ttu-id="74114-111">Cet attribut contient une paire de GUID : un type principal et un sous-type.</span><span class="sxs-lookup"><span data-stu-id="74114-111">This attribute contains a pair of GUIDs: a major type and a subtype.</span></span> <span data-ttu-id="74114-112">Ces GUID décrivent le format de sortie par défaut de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="74114-112">These GUIDs describe the default output format of the device.</span></span> <span data-ttu-id="74114-113">L’appareil peut prendre en charge des formats de sortie supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="74114-113">The device might support additional output formats.</span></span>

<span data-ttu-id="74114-114">Par exemple, si un appareil de capture vidéo produit une vidéo RGB-32, la valeur de cet attribut est `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .</span><span class="sxs-lookup"><span data-stu-id="74114-114">For example, if a video capture device outputs RGB-32 video, the value of this attribute is `{ MFMediaType_Video, MFVideoFormat_RGB32 }`.</span></span>

<span data-ttu-id="74114-115">Cet attribut est une indication de l’application.</span><span class="sxs-lookup"><span data-stu-id="74114-115">This attribute is a hint to the application.</span></span> <span data-ttu-id="74114-116">Pour obtenir le format de sortie exact, créez la source du média pour l’appareil et récupérez le descripteur de présentation de la source du média.</span><span class="sxs-lookup"><span data-stu-id="74114-116">To get the exact output format, create the media source for the device and get the media source's presentation descriptor.</span></span>

<span data-ttu-id="74114-117">Cet attribut est défini sur les objets d’activation retournés par les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="74114-117">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="74114-118">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="74114-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="74114-119">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="74114-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="74114-120">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="74114-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="74114-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74114-121">Requirements</span></span>



| <span data-ttu-id="74114-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74114-122">Requirement</span></span> | <span data-ttu-id="74114-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="74114-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="74114-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74114-124">Minimum supported client</span></span><br/> | <span data-ttu-id="74114-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74114-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="74114-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74114-126">Minimum supported server</span></span><br/> | <span data-ttu-id="74114-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74114-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="74114-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="74114-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="74114-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74114-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74114-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74114-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74114-131">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="74114-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="74114-132">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="74114-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="74114-133">Capturer les attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="74114-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




