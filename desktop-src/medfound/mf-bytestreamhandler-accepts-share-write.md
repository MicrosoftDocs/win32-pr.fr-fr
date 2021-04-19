---
description: Spécifie si un gestionnaire de flux d’octets peut utiliser un flux d’octets ouvert pour l’écriture par un autre thread.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: Attribut MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527377"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a><span data-ttu-id="913f7-103">MF \_ BYTESTREAMHANDLER \_ accepte \_ l' \_ attribut d’écriture de partage</span><span class="sxs-lookup"><span data-stu-id="913f7-103">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute</span></span>

<span data-ttu-id="913f7-104">Spécifie si un gestionnaire de flux d’octets peut utiliser un flux d’octets ouvert pour l’écriture par un autre thread.</span><span class="sxs-lookup"><span data-stu-id="913f7-104">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread.</span></span>

## <a name="data-type"></a><span data-ttu-id="913f7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="913f7-105">Data type</span></span>

<span data-ttu-id="913f7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="913f7-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="913f7-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="913f7-107">Get/set</span></span>

<span data-ttu-id="913f7-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="913f7-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="913f7-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="913f7-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="913f7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="913f7-110">Remarks</span></span>

<span data-ttu-id="913f7-111">Les gestionnaires de flux d’octets peuvent prendre en charge cet attribut.</span><span class="sxs-lookup"><span data-stu-id="913f7-111">Byte-stream handlers can support this attribute.</span></span> <span data-ttu-id="913f7-112">Pour obtenir ou définir l’attribut, interrogez d’abord le gestionnaire de flux d’octets de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="913f7-112">To get or set the attribute, first query the byte-stream handler for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="913f7-113">Appelez ensuite [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) ou [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span><span class="sxs-lookup"><span data-stu-id="913f7-113">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) or [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span></span>

<span data-ttu-id="913f7-114">Si cet attribut a la **valeur true**, cela signifie que le gestionnaire de flux d’octets peut lire à partir d’un flux, tandis qu’un autre thread écrit dans le même flux.</span><span class="sxs-lookup"><span data-stu-id="913f7-114">If this attribute is **TRUE**, it means that the byte-stream handler can read from a stream while another thread writes to the same stream.</span></span> <span data-ttu-id="913f7-115">Lorsqu’un flux est ouvert en écriture par un autre thread, la méthode [**IMFByteStream :: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) retourne l’indicateur d' **\_ \_ écriture de partage MFBYTESTREAM** .</span><span class="sxs-lookup"><span data-stu-id="913f7-115">When a stream is opened for writing by another thread, the [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) method returns the **MFBYTESTREAM\_SHARE\_WRITE** flag.</span></span>

<span data-ttu-id="913f7-116">Cet attribut affecte la résolution de la source.</span><span class="sxs-lookup"><span data-stu-id="913f7-116">This attribute affects source resolution.</span></span> <span data-ttu-id="913f7-117">Si l’indicateur **MFBYTESTREAM \_ share \_ Write** est défini pour un flux d’octets, le programme de [résolution source](source-resolver.md) ne passe pas ce flux à un gestionnaire de flux d’octets, à moins que le gestionnaire MF \_ BYTESTREAMHANDLER \_ accepte l' \_ \_ attribut share Write défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="913f7-117">If a byte stream has the **MFBYTESTREAM\_SHARE\_WRITE** flag set, the [Source Resolver](source-resolver.md) will not pass that stream to a byte-stream handler unless the handler has the MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute set to **TRUE**.</span></span>

<span data-ttu-id="913f7-118">L’indicateur **MFBYTESTREAM \_ share \_ Write** indique que la longueur du flux peut changer pendant que le gestionnaire la lit.</span><span class="sxs-lookup"><span data-stu-id="913f7-118">The **MFBYTESTREAM\_SHARE\_WRITE** flag is a hint that the length of the stream might change while the handler is reading from it.</span></span>

<span data-ttu-id="913f7-119">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="913f7-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="913f7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="913f7-120">Requirements</span></span>



| <span data-ttu-id="913f7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="913f7-121">Requirement</span></span> | <span data-ttu-id="913f7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="913f7-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="913f7-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="913f7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="913f7-124">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="913f7-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="913f7-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="913f7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="913f7-126">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="913f7-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="913f7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="913f7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="913f7-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="913f7-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="913f7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="913f7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="913f7-130">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="913f7-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="913f7-131">Gestionnaires de schémas et gestionnaires de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="913f7-131">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




