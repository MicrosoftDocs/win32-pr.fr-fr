---
description: Contient un pointeur vers l’interface de rappel des applications pour le writer du récepteur.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: Attribut MF_SINK_WRITER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759568"
---
# <a name="mf_sink_writer_async_callback-attribute"></a><span data-ttu-id="0e707-103">\_Attribut de \_ \_ rappel asynchrone du writer de récepteur MF \_</span><span class="sxs-lookup"><span data-stu-id="0e707-103">MF\_SINK\_WRITER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="0e707-104">Contient un pointeur vers l’interface de rappel de l’application pour le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="0e707-104">Contains a pointer to the application's callback interface for the sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e707-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0e707-105">Data type</span></span>

<span data-ttu-id="0e707-106">**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) IMFSinkWriterCallback \** _ stocké en tant que _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="0e707-106">**[**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="0e707-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="0e707-107">Get/set</span></span>

<span data-ttu-id="0e707-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="0e707-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="0e707-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="0e707-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e707-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0e707-110">Remarks</span></span>

<span data-ttu-id="0e707-111">La valeur de cet attribut est un pointeur vers l’interface [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) de l’application.</span><span class="sxs-lookup"><span data-stu-id="0e707-111">The value of this attribute is a pointer to the application's [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) interface.</span></span>

<span data-ttu-id="0e707-112">Utilisez cet attribut avec les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e707-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="0e707-113">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="0e707-113">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="0e707-114">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="0e707-114">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="0e707-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e707-115">Requirements</span></span>



| <span data-ttu-id="0e707-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e707-116">Requirement</span></span> | <span data-ttu-id="0e707-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e707-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e707-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e707-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0e707-119">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0e707-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0e707-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e707-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0e707-121">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0e707-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0e707-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e707-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e707-123"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e707-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e707-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e707-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e707-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e707-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e707-126">Attributs du writer du récepteur</span><span class="sxs-lookup"><span data-stu-id="0e707-126">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




