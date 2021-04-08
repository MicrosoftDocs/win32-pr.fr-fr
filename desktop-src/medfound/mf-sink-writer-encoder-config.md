---
description: Contient un pointeur vers une banque de propriétés avec des propriétés d’encodage.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: Attribut MF_SINK_WRITER_ENCODER_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757401"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a><span data-ttu-id="d6637-103">Attribut de configuration de l' \_ \_ \_ encodeur du récepteur MF \_</span><span class="sxs-lookup"><span data-stu-id="d6637-103">MF\_SINK\_WRITER\_ENCODER\_CONFIG attribute</span></span>

<span data-ttu-id="d6637-104">Contient un pointeur vers une banque de propriétés avec des propriétés d’encodage.</span><span class="sxs-lookup"><span data-stu-id="d6637-104">Contains a pointer to a property store with encoding properties.</span></span>

## <a name="data-type"></a><span data-ttu-id="d6637-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d6637-105">Data type</span></span>

<span data-ttu-id="d6637-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="d6637-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="d6637-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d6637-107">Remarks</span></span>

<span data-ttu-id="d6637-108">La valeur de cet attribut est un pointeur [_ *IPropertyStore* \*](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="d6637-108">The value of this attribute is an [_ *IPropertyStore*\*](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer.</span></span>

<span data-ttu-id="d6637-109">Cet attribut permet à une application de définir des propriétés d’encodage lors de l’utilisation du [writer du récepteur](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="d6637-109">This attribute enables an application to set encoding properties when using the [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="d6637-110">Pour définir cet attribut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6637-110">To set this attribute, perform the following steps:</span></span>

1.  <span data-ttu-id="d6637-111">Appelez [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) pour créer une banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d6637-111">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a new property store.</span></span>
2.  <span data-ttu-id="d6637-112">Définissez les propriétés de l’encodeur dans la Banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d6637-112">Set encoder properties on the property store.</span></span> <span data-ttu-id="d6637-113">Les propriétés disponibles dépendent de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="d6637-113">The available properties depends on the encoder.</span></span> <span data-ttu-id="d6637-114">Pour plus d’informations, consultez la page [objets codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="d6637-114">For more information, see [Codec Objects](codecobjects.md).</span></span>
3.  <span data-ttu-id="d6637-115">Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un nouveau magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="d6637-115">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
4.  <span data-ttu-id="d6637-116">Appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) pour définir le pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) sur le magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="d6637-116">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer on the attribute store.</span></span>
5.  <span data-ttu-id="d6637-117">Créez une nouvelle instance de l’enregistreur du récepteur.</span><span class="sxs-lookup"><span data-stu-id="d6637-117">Create a new instance of the Sink Writer.</span></span> <span data-ttu-id="d6637-118">Transmettez le pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) à la fonction de création.</span><span class="sxs-lookup"><span data-stu-id="d6637-118">Pass the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer to the creation function.</span></span> <span data-ttu-id="d6637-119">Pour plus d’informations, consultez [attributs du writer du récepteur](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d6637-119">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

<span data-ttu-id="d6637-120">L’enregistreur du récepteur définit les propriétés sur l’encodeur avant de définir les types de média.</span><span class="sxs-lookup"><span data-stu-id="d6637-120">The Sink Writer sets the properties on the encoder before setting the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6637-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6637-121">Requirements</span></span>



| <span data-ttu-id="d6637-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6637-122">Requirement</span></span> | <span data-ttu-id="d6637-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6637-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6637-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6637-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d6637-125">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6637-125">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d6637-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6637-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d6637-127">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6637-127">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d6637-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6637-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6637-129"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6637-129"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6637-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6637-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6637-131">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6637-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d6637-132">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="d6637-132">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="d6637-133">Attributs du writer du récepteur</span><span class="sxs-lookup"><span data-stu-id="d6637-133">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 
