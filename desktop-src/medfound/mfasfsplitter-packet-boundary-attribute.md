---
description: Spécifie si une mémoire tampon contient le début d’un paquet ASF (Advanced Systems Format).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: Attribut MFASFSPLITTER_PACKET_BOUNDARY (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521420"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a><span data-ttu-id="02f57-103">MFASFSPLITTER \_ attribut de limite de paquet \_</span><span class="sxs-lookup"><span data-stu-id="02f57-103">MFASFSPLITTER\_PACKET\_BOUNDARY attribute</span></span>

<span data-ttu-id="02f57-104">Spécifie si une mémoire tampon contient le début d’un paquet ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="02f57-104">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="02f57-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="02f57-105">Data type</span></span>

<span data-ttu-id="02f57-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="02f57-106">**UINT32**</span></span>

<span data-ttu-id="02f57-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="02f57-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02f57-108">Notes</span><span class="sxs-lookup"><span data-stu-id="02f57-108">Remarks</span></span>

<span data-ttu-id="02f57-109">Si une mémoire tampon de média expose l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) via **QueryInterface** et que la valeur de cet attribut est différente de zéro, le séparateur ASF traite la mémoire tampon comme le début d’un nouveau paquet.</span><span class="sxs-lookup"><span data-stu-id="02f57-109">If a media buffer exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface through **QueryInterface**, and the value of this attribute is nonzero, the ASF splitter treats the buffer as the start of a new packet.</span></span>

<span data-ttu-id="02f57-110">Cet attribut s’applique si vous utilisez le séparateur ASF pour analyser les données ASF.</span><span class="sxs-lookup"><span data-stu-id="02f57-110">This attribute applies if you are using the ASF splitter to parse ASF data.</span></span> <span data-ttu-id="02f57-111">Si vos données ASF ont des longueurs de paquets variables, vous devez définir cet attribut sur les mémoires tampons de média que vous transmettez à la méthode [**IMFASFSplitter ::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="02f57-111">If your ASF data has variable packet lengths, you must set this attribute on the media buffers that you pass to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="02f57-112">Affectez la **valeur true** à l’attribut si la mémoire tampon contient le début d’un nouveau paquet.</span><span class="sxs-lookup"><span data-stu-id="02f57-112">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="02f57-113">Si la mémoire tampon contient une continuation du paquet précédent, affectez la valeur **false** à l’attribut.</span><span class="sxs-lookup"><span data-stu-id="02f57-113">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="02f57-114">Les mémoires tampons ne peuvent pas couvrir plusieurs paquets.</span><span class="sxs-lookup"><span data-stu-id="02f57-114">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="02f57-115">Pour les données ASF avec des tailles de paquets fixes, cet attribut n’est pas obligatoire et une mémoire tampon peut s’étendre sur plusieurs paquets.</span><span class="sxs-lookup"><span data-stu-id="02f57-115">For ASF data with fixed packet sizes, this attribute is not required, and a buffer can can span multiple packets.</span></span>

<span data-ttu-id="02f57-116">Notez que les implémentations standard du [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) fournies par Media Foundation n’exposent pas [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="02f57-116">Note that the standard implementations of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) provided by Media Foundation do not expose [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="02f57-117">Pour utiliser cet attribut, vous devez fournir votre propre implémentation de **IMFMediaBuffer**; par exemple, en encapsulant les mémoires tampons retournées par [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span><span class="sxs-lookup"><span data-stu-id="02f57-117">To use this attribute, you must provide your own implementation of **IMFMediaBuffer**; for example, by wrapping the buffers returned by [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span></span>

## <a name="requirements"></a><span data-ttu-id="02f57-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02f57-118">Requirements</span></span>



| <span data-ttu-id="02f57-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02f57-119">Requirement</span></span> | <span data-ttu-id="02f57-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="02f57-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02f57-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02f57-121">Minimum supported client</span></span><br/> | <span data-ttu-id="02f57-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02f57-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="02f57-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02f57-123">Minimum supported server</span></span><br/> | <span data-ttu-id="02f57-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02f57-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="02f57-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="02f57-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="02f57-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="02f57-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02f57-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02f57-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f57-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="02f57-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="02f57-129">Attributs ASF</span><span class="sxs-lookup"><span data-stu-id="02f57-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="02f57-130">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="02f57-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="02f57-131">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="02f57-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="02f57-132">**IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="02f57-132">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




