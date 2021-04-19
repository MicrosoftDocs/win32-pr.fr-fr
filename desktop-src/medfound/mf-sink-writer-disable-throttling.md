---
description: Spécifie si l’enregistreur du récepteur limite le taux des données entrantes.
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: Attribut MF_SINK_WRITER_DISABLE_THROTTLING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529425"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a><span data-ttu-id="8e4c4-103">\_Attribut de \_ \_ limitation de désactivation de l’enregistreur de récepteur MF \_</span><span class="sxs-lookup"><span data-stu-id="8e4c4-103">MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute</span></span>

<span data-ttu-id="8e4c4-104">Spécifie si l’enregistreur du récepteur limite le taux des données entrantes.</span><span class="sxs-lookup"><span data-stu-id="8e4c4-104">Specifies whether the sink writer limits the rate of incoming data.</span></span>

## <a name="data-type"></a><span data-ttu-id="8e4c4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8e4c4-105">Data type</span></span>

<span data-ttu-id="8e4c4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8e4c4-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="8e4c4-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="8e4c4-107">Get/set</span></span>

<span data-ttu-id="8e4c4-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8e4c4-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8e4c4-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="8e4c4-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4c4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8e4c4-110">Remarks</span></span>

<span data-ttu-id="8e4c4-111">Par défaut, la méthode [**IMFSinkWriter :: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) du writer de récepteur limite le débit de données en bloquant le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="8e4c4-111">By default, the sink writer's [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method limits the data rate by blocking the calling thread.</span></span> <span data-ttu-id="8e4c4-112">Cela empêche l’application de diffuser des exemples trop rapidement.</span><span class="sxs-lookup"><span data-stu-id="8e4c4-112">This prevents the application from delivering samples too quickly.</span></span> <span data-ttu-id="8e4c4-113">Pour désactiver ce comportement, affectez \_ à l' \_ \_ attribut de limitation de désactivation de l’enregistreur de récepteur MF la \_ **valeur true** lorsque vous créez le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="8e4c4-113">To disable this behavior, set the MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute to **TRUE** when you create the sink writer.</span></span>

<span data-ttu-id="8e4c4-114">Utilisez cet attribut avec les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e4c4-114">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="8e4c4-115">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="8e4c4-115">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="8e4c4-116">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="8e4c4-116">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="8e4c4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e4c4-117">Requirements</span></span>



| <span data-ttu-id="8e4c4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e4c4-118">Requirement</span></span> | <span data-ttu-id="8e4c4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e4c4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e4c4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e4c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8e4c4-121">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8e4c4-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="8e4c4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e4c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8e4c4-123">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8e4c4-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8e4c4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e4c4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e4c4-125"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e4c4-125"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e4c4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e4c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e4c4-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8e4c4-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8e4c4-128">Attributs du writer du récepteur</span><span class="sxs-lookup"><span data-stu-id="8e4c4-128">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




