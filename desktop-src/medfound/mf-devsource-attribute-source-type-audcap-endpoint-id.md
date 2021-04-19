---
description: Spécifie l’ID de point de terminaison pour un périphérique de capture audio.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532210"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a><span data-ttu-id="353d8-103">Attribut \_ d' \_ ID de \_ point de \_ \_ \_ terminaison \_ AUDCAP de type de l’attribut DEVSOURCE MF</span><span class="sxs-lookup"><span data-stu-id="353d8-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="353d8-104">Spécifie l’ID de point de terminaison pour un périphérique de capture audio.</span><span class="sxs-lookup"><span data-stu-id="353d8-104">Specifies the endpoint ID for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="353d8-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="353d8-105">Data type</span></span>

<span data-ttu-id="353d8-106">**WCHAR\***</span><span class="sxs-lookup"><span data-stu-id="353d8-106">**WCHAR\***</span></span>

## <a name="getset"></a><span data-ttu-id="353d8-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="353d8-107">Get/set</span></span>

<span data-ttu-id="353d8-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="353d8-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="353d8-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="353d8-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="353d8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="353d8-110">Remarks</span></span>

<span data-ttu-id="353d8-111">La valeur de l’attribut est un ID de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="353d8-111">The value of the attribute is an endpoint ID.</span></span> <span data-ttu-id="353d8-112">Cet attribut est utilisé avec les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="353d8-112">This attribute is used with the following functions:</span></span>

-   <span data-ttu-id="353d8-113">Il peut être utilisé comme entrée pour les fonctions [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) et [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="353d8-113">It can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="353d8-114">Dans ce contexte, l’attribut spécifie le périphérique de capture audio pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="353d8-114">In this context, the attribute specifies the audio capture device for the function.</span></span> <span data-ttu-id="353d8-115">Vous pouvez obtenir l’ID de point de terminaison d’un appareil donné en appelant la méthode [**IMMDevice :: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) .</span><span class="sxs-lookup"><span data-stu-id="353d8-115">You can get the endpoint ID for a given device by calling the [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method.</span></span> <span data-ttu-id="353d8-116">Pour plus d’informations, consultez la documentation de l’API audio principale.</span><span class="sxs-lookup"><span data-stu-id="353d8-116">See the Core Audio API documentation for more information.</span></span>
-   <span data-ttu-id="353d8-117">Lorsque la fonction [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) énumère les périphériques audio, les objets d’activation retournés contiennent cet attribut.</span><span class="sxs-lookup"><span data-stu-id="353d8-117">When the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function enumerates audio devices, the returned activation objects contain this attribute.</span></span> <span data-ttu-id="353d8-118">L’attribut est utilisé en interne par l’objet d’activation lorsqu’il crée la source du média.</span><span class="sxs-lookup"><span data-stu-id="353d8-118">The attribute is used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="353d8-119">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="353d8-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="353d8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="353d8-120">Requirements</span></span>



| <span data-ttu-id="353d8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="353d8-121">Requirement</span></span> | <span data-ttu-id="353d8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="353d8-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="353d8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="353d8-123">Header</span></span><br/> | <dl> <span data-ttu-id="353d8-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="353d8-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="353d8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="353d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="353d8-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="353d8-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="353d8-127">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="353d8-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="353d8-128">Capturer les attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="353d8-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
