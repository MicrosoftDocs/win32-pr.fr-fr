---
description: Contient un pointeur vers le Gestionnaire de périphériques DXGI pour le writer du récepteur.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Attribut MF_SINK_WRITER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544317"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a><span data-ttu-id="d7ab4-103">\_Attribut du \_ \_ Gestionnaire D3D \_ de l’enregistreur du récepteur MF</span><span class="sxs-lookup"><span data-stu-id="d7ab4-103">MF\_SINK\_WRITER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="d7ab4-104">Contient un pointeur vers le Gestionnaire de périphériques DXGI pour le [writer du récepteur](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="d7ab4-104">Contains a pointer to the DXGI Device Manager for the [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="d7ab4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d7ab4-105">Data type</span></span>

<span data-ttu-id="d7ab4-106">**IMFDXGIDeviceManager \** _ stocké en tant que _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="d7ab4-106">**IMFDXGIDeviceManager\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ab4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d7ab4-107">Remarks</span></span>

<span data-ttu-id="d7ab4-108">La valeur de cet attribut est un pointeur vers l’interface [_ *IMFDXGIDeviceManager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="d7ab4-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="d7ab4-109">Utilisez cet attribut pour fournir un appareil Direct3D pour tous les encodeurs vidéo ou récepteurs multimédias chargés par le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="d7ab4-109">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the Sink Writer.</span></span>

<span data-ttu-id="d7ab4-110">Utilisez cet attribut avec les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7ab4-110">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="d7ab4-111">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="d7ab4-111">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="d7ab4-112">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="d7ab4-112">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="d7ab4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7ab4-113">Requirements</span></span>



| <span data-ttu-id="d7ab4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7ab4-114">Requirement</span></span> | <span data-ttu-id="d7ab4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7ab4-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ab4-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ab4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ab4-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d7ab4-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d7ab4-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ab4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ab4-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="d7ab4-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d7ab4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7ab4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7ab4-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ab4-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ab4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7ab4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ab4-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7ab4-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7ab4-124">Enregistreur du récepteur</span><span class="sxs-lookup"><span data-stu-id="d7ab4-124">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 




