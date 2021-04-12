---
description: Spécifie si le lecteur source arrête la source du média.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: Attribut MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321662"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a><span data-ttu-id="6e9db-103">\_Lecteur source \_ MF \_ Disconnect \_ MEDIASOURCE \_ sur l' \_ attribut Shutdown</span><span class="sxs-lookup"><span data-stu-id="6e9db-103">MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute</span></span>

<span data-ttu-id="6e9db-104">Spécifie si le [lecteur source](source-reader.md) arrête la source du média.</span><span class="sxs-lookup"><span data-stu-id="6e9db-104">Specifies whether the [Source Reader](source-reader.md) shuts down the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="6e9db-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="6e9db-105">Data type</span></span>

<span data-ttu-id="6e9db-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6e9db-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6e9db-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="6e9db-107">Get/set</span></span>

<span data-ttu-id="6e9db-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6e9db-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6e9db-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="6e9db-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e9db-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6e9db-110">Remarks</span></span>

<span data-ttu-id="6e9db-111">Cet attribut s’applique uniquement lorsque l’application crée le lecteur source à partir d’un objet source multimédia existant, en appelant [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) ou en appelant [**IMFReadWriteClassFactory :: CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span><span class="sxs-lookup"><span data-stu-id="6e9db-111">This attribute applies only when the application creates the source reader from an existing media source object, either by calling [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) or by calling [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span></span>

<span data-ttu-id="6e9db-112">Par défaut, lorsque l’application libère le lecteur source, le lecteur source arrête la source du média en appelant [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur la source du média.</span><span class="sxs-lookup"><span data-stu-id="6e9db-112">By default, when the application releases the source reader, the source reader shuts down the media source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span> <span data-ttu-id="6e9db-113">À ce stade, l’application ne peut plus utiliser la source du média.</span><span class="sxs-lookup"><span data-stu-id="6e9db-113">At that point, the application can no longer use the media source.</span></span>

<span data-ttu-id="6e9db-114">Toutefois, si le \_ lecteur source \_ MF \_ Disconnect \_ MEDIASOURCE \_ sur \_ l’attribut Shutdown a la **valeur true**, le lecteur source n’arrête pas la source du média.</span><span class="sxs-lookup"><span data-stu-id="6e9db-114">However, if the MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is **TRUE**, the source reader does not shut down the media source.</span></span> <span data-ttu-id="6e9db-115">Cela signifie que l’application peut toujours utiliser la source du média après que l’application a libéré le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="6e9db-115">That means the application can still use the media source after the application releases the source reader.</span></span> <span data-ttu-id="6e9db-116">Cela signifie également que l’application est responsable de l’appel de [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur la source du média.</span><span class="sxs-lookup"><span data-stu-id="6e9db-116">It also means the application is responsible for calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>

<span data-ttu-id="6e9db-117">Si l’application crée le lecteur source à partir d’une URL ou d’un flux d’octets, le lecteur source arrête toujours la source du média.</span><span class="sxs-lookup"><span data-stu-id="6e9db-117">If the application creates the source reader from a URL or from a byte stream, the source reader always shuts down the media source.</span></span> <span data-ttu-id="6e9db-118">Le \_ lecteur source \_ MF \_ Disconnect \_ MEDIASOURCE \_ sur l' \_ attribut Shutdown est ignoré dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="6e9db-118">The MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is ignored in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e9db-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e9db-119">Requirements</span></span>



| <span data-ttu-id="6e9db-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e9db-120">Requirement</span></span> | <span data-ttu-id="6e9db-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e9db-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9db-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e9db-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6e9db-123">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6e9db-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="6e9db-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e9db-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6e9db-125">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6e9db-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6e9db-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e9db-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e9db-127"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e9db-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e9db-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e9db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e9db-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6e9db-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6e9db-130">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="6e9db-130">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="6e9db-131">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="6e9db-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




