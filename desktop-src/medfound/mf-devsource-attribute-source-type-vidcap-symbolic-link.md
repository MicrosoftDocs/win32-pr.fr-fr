---
description: Contient le lien symbolique pour un pilote de capture vidéo.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48e1c854ee070713462676482cc04690c2bdde2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114606"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a><span data-ttu-id="66e3c-103">Attribut \_ de \_ \_ \_ \_ \_ lien symbolique VIDCAP du type de source \_ de l’attribut MF DEVSOURCE</span><span class="sxs-lookup"><span data-stu-id="66e3c-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute</span></span>

<span data-ttu-id="66e3c-104">Contient le lien symbolique pour un pilote de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="66e3c-104">Contains the symbolic link for a video capture driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="66e3c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="66e3c-105">Data type</span></span>

<span data-ttu-id="66e3c-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="66e3c-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="66e3c-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="66e3c-107">Get/set</span></span>

<span data-ttu-id="66e3c-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="66e3c-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="66e3c-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="66e3c-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="66e3c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="66e3c-110">Remarks</span></span>

<span data-ttu-id="66e3c-111">Utilisez cet attribut comme entrée de la fonction [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="66e3c-111">Use this attribute as input to the [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="66e3c-112">En outre, cet attribut est défini sur les objets d’activation retournés par les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="66e3c-112">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="66e3c-113">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="66e3c-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="66e3c-114">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="66e3c-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="66e3c-115">Le lien symbolique doit être considéré comme une chaîne opaque.</span><span class="sxs-lookup"><span data-stu-id="66e3c-115">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="66e3c-116">Le nom complet lisible pour un appareil est contenu dans l’attribut de [ \_ \_ \_ \_ nom convivial de l’attribut MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) .</span><span class="sxs-lookup"><span data-stu-id="66e3c-116">The human-readable display name for a device is contained in the [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute.</span></span>

<span data-ttu-id="66e3c-117">L’attribut \_ \_ \_ de lien symbolique VIDCAP du type de source de l’attribut MF DEVSOURCE \_ \_ \_ \_ peut être transmis en tant que valeur de l’argument DevicePath de la fonction [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) .</span><span class="sxs-lookup"><span data-stu-id="66e3c-117">The MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute can be passed in as the value of the DevicePath argument of the [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) function.</span></span>

<span data-ttu-id="66e3c-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="66e3c-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e3c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66e3c-119">Requirements</span></span>



| <span data-ttu-id="66e3c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66e3c-120">Requirement</span></span> | <span data-ttu-id="66e3c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="66e3c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66e3c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66e3c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="66e3c-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66e3c-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="66e3c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66e3c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="66e3c-125">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66e3c-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="66e3c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="66e3c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="66e3c-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66e3c-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e3c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66e3c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e3c-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66e3c-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66e3c-130">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="66e3c-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="66e3c-131">Capturer les attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="66e3c-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
