---
description: Spécifie le CLSID d’un plug-in de traitement de message pour un périphérique de capture vidéo.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: Attribut MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527747"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a><span data-ttu-id="5acac-103">\_ \_ \_ Attribut CLSID du plug-in d’extension DEVICESTREAM MF \_</span><span class="sxs-lookup"><span data-stu-id="5acac-103">MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute</span></span>

<span data-ttu-id="5acac-104">Spécifie le CLSID d’un plug-in de traitement de message pour un périphérique de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="5acac-104">Specifies the CLSID of a post-processing plug-in for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="5acac-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5acac-105">Data type</span></span>

<span data-ttu-id="5acac-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="5acac-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="5acac-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5acac-107">Remarks</span></span>

<span data-ttu-id="5acac-108">Un plug-in de traitement de billet est un MFT qui traite l’image vidéo après sa capture.</span><span class="sxs-lookup"><span data-stu-id="5acac-108">A post-processing plug-in is an MFT that processes the video image after it is captured.</span></span> <span data-ttu-id="5acac-109">Le fournisseur de matériel peut inclure un plug-in de retraitement dans le cadre du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="5acac-109">The hardware vendor can include a post-processing plug-in as part of the installation package.</span></span> <span data-ttu-id="5acac-110">Si c’est le cas, la source de capture vidéo affecte \_ \_ à l' \_ attribut CLSID du plug-in d’extension DEVICESTREAM MF \_ le CLSID du plug-in.</span><span class="sxs-lookup"><span data-stu-id="5acac-110">If so, the video capture source sets the MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute to the CLSID of the plug-in.</span></span>

<span data-ttu-id="5acac-111">Pour accéder à cet attribut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5acac-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="5acac-112">Interrogez la source du média pour l’interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="5acac-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="5acac-113">Appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) pour obtenir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour le flux.</span><span class="sxs-lookup"><span data-stu-id="5acac-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="5acac-114">Appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) pour accéder à l’attribut.</span><span class="sxs-lookup"><span data-stu-id="5acac-114">Call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) to get the attribute.</span></span>

<span data-ttu-id="5acac-115">Pour créer le plug-in, appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="5acac-115">To create the plug-in, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="requirements"></a><span data-ttu-id="5acac-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5acac-116">Requirements</span></span>



| <span data-ttu-id="5acac-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5acac-117">Requirement</span></span> | <span data-ttu-id="5acac-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5acac-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5acac-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5acac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5acac-120">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5acac-120">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5acac-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5acac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5acac-122">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5acac-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5acac-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5acac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5acac-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5acac-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5acac-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5acac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5acac-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5acac-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
