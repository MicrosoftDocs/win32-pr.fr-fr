---
description: Indique que les informations de longueur NALU sont envoyées en tant qu’objet BLOB avec chaque exemple H. 264 compressé.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: Attribut MF_NALU_LENGTH_SET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522211"
---
# <a name="mf_nalu_length_set-attribute"></a><span data-ttu-id="f560f-103">\_ \_ Attribut Set de longueur Nalu MF \_</span><span class="sxs-lookup"><span data-stu-id="f560f-103">MF\_NALU\_LENGTH\_SET attribute</span></span>

<span data-ttu-id="f560f-104">Indique que les informations de longueur NALU sont envoyées en tant qu' **objet BLOB** avec chaque exemple H. 264 compressé.</span><span class="sxs-lookup"><span data-stu-id="f560f-104">Indicates that NALU length information will be sent as a **BLOB** with each compressed H.264 sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="f560f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f560f-105">Data type</span></span>

<span data-ttu-id="f560f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f560f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f560f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f560f-107">Remarks</span></span>

<span data-ttu-id="f560f-108">Définissez cet attribut sur le type de média d’entrée de MEDIASUBTYPE \_ H264 –.</span><span class="sxs-lookup"><span data-stu-id="f560f-108">Set this attribute on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="f560f-109">Définissez \_ \_ la longueur de Nalu MF \_ définie sur le type de média d’entrée du décodeur H. 264, indiquant que chaque exemple d’entrée aura une longueur de Nalu disponible et que chaque exemple d’entrée contient une image principale complète.</span><span class="sxs-lookup"><span data-stu-id="f560f-109">Set MF\_NALU\_LENGTH\_SET on input media type of H.264 decoder, indicating each input sample will have a NALU length available and each input sample contains one complete primary picture.</span></span>

<span data-ttu-id="f560f-110">L' **objet BLOB** contenant les informations de longueur Nalu peut être récupéré à partir de l’attribut d' [ \_ \_ \_ informations de longueur Nalu MF](mf-nalu-length-information.md) sur l’exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f560f-110">The **BLOB** containing the NALU length information can be retrieved from [MF\_NALU\_LENGTH\_INFORMATION](mf-nalu-length-information.md) attribute on the input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="f560f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f560f-111">Requirements</span></span>



| <span data-ttu-id="f560f-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f560f-112">Requirement</span></span> | <span data-ttu-id="f560f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f560f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f560f-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f560f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f560f-115">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f560f-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f560f-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f560f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f560f-117">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="f560f-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f560f-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f560f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f560f-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f560f-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f560f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f560f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f560f-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f560f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f560f-122">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="f560f-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




