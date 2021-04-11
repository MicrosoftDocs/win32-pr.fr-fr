---
description: Spécifie la durée d’un flux d’octets, en unités de 100 nanosecondes.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: Attribut MF_BYTESTREAM_DURATION (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df264416b8a805e6d239cfcc457f4a6db2a8e4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318810"
---
# <a name="mf_bytestream_duration-attribute"></a><span data-ttu-id="13a77-103">\_Attribut de \_ durée BYTESTREAM MF</span><span class="sxs-lookup"><span data-stu-id="13a77-103">MF\_BYTESTREAM\_DURATION attribute</span></span>

<span data-ttu-id="13a77-104">Spécifie la durée d’un flux d’octets, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="13a77-104">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="13a77-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="13a77-105">Data type</span></span>

<span data-ttu-id="13a77-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="13a77-106">**UINT64**</span></span>

<span data-ttu-id="13a77-107">Traiter en tant que valeur **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="13a77-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13a77-108">Notes</span><span class="sxs-lookup"><span data-stu-id="13a77-108">Remarks</span></span>

<span data-ttu-id="13a77-109">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="13a77-109">This attribute is optional.</span></span> <span data-ttu-id="13a77-110">Si l’objet qui crée le flux d’octets peut déterminer la durée, il peut définir cet attribut.</span><span class="sxs-lookup"><span data-stu-id="13a77-110">If the object that creates the byte stream can determine the duration, it can set this attribute.</span></span> <span data-ttu-id="13a77-111">(Par exemple, dans un flux de réseau, la durée peut faire partie de la description de session.)</span><span class="sxs-lookup"><span data-stu-id="13a77-111">(For example, in a network stream, the duration might be part of the session description.)</span></span>

<span data-ttu-id="13a77-112">Pour obtenir la valeur de l’attribut, appelez **QueryInterface** sur le flux d’octets pour obtenir un pointeur vers l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="13a77-112">To get the attribute value, call **QueryInterface** on the byte stream to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="13a77-113">Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="13a77-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="13a77-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="13a77-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a77-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13a77-115">Requirements</span></span>



| <span data-ttu-id="13a77-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13a77-116">Requirement</span></span> | <span data-ttu-id="13a77-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="13a77-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a77-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13a77-118">Minimum supported client</span></span><br/> | <span data-ttu-id="13a77-119">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="13a77-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="13a77-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13a77-120">Minimum supported server</span></span><br/> | <span data-ttu-id="13a77-121">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="13a77-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="13a77-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="13a77-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a77-123"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13a77-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a77-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13a77-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a77-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="13a77-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="13a77-126">Attributs de flux d’octets</span><span class="sxs-lookup"><span data-stu-id="13a77-126">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="13a77-127">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="13a77-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="13a77-128">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="13a77-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="13a77-129">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="13a77-129">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




