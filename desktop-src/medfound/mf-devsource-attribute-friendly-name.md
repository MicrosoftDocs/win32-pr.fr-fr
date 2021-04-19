---
description: Spécifie le nom complet d’un appareil.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: Attribut MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab0d2bb3c0e75d547e1249a83261b7c804743ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527196"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a><span data-ttu-id="cf4e2-103">\_Attribut de \_ \_ nom convivial \_ de l’attribut DEVSOURCE MF</span><span class="sxs-lookup"><span data-stu-id="cf4e2-103">MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME attribute</span></span>

<span data-ttu-id="cf4e2-104">Spécifie le nom complet d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="cf4e2-104">Specifies the display name for a device.</span></span> <span data-ttu-id="cf4e2-105">Le *nom d’affichage* est une chaîne explicite, pouvant être affichée dans une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf4e2-105">The *display name* is a human-readable string, suitable for display in a user interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="cf4e2-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="cf4e2-106">Data type</span></span>

<span data-ttu-id="cf4e2-107">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="cf4e2-107">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="cf4e2-108">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="cf4e2-108">Get/set</span></span>

<span data-ttu-id="cf4e2-109">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="cf4e2-109">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="cf4e2-110">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="cf4e2-110">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf4e2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cf4e2-111">Remarks</span></span>

<span data-ttu-id="cf4e2-112">Cet attribut est défini sur les objets d’activation retournés par les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf4e2-112">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="cf4e2-113">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="cf4e2-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="cf4e2-114">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="cf4e2-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="cf4e2-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cf4e2-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf4e2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf4e2-116">Requirements</span></span>



| <span data-ttu-id="cf4e2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf4e2-117">Requirement</span></span> | <span data-ttu-id="cf4e2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf4e2-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4e2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf4e2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf4e2-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf4e2-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cf4e2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf4e2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf4e2-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf4e2-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cf4e2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf4e2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf4e2-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf4e2-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf4e2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf4e2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf4e2-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cf4e2-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cf4e2-127">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="cf4e2-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="cf4e2-128">Capturer les attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="cf4e2-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




