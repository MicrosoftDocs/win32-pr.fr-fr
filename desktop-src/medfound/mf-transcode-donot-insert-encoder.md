---
description: Spécifie si un encodeur doit être inclus dans la topologie de transcodage.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: Attribut MF_TRANSCODE_DONOT_INSERT_ENCODER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514236"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a><span data-ttu-id="03c77-103">MF \_ transcodage \_ ne \_ \_ attribut d’encodeur d’insertion</span><span class="sxs-lookup"><span data-stu-id="03c77-103">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER attribute</span></span>

<span data-ttu-id="03c77-104">Spécifie si un encodeur doit être inclus dans la topologie de transcodage.</span><span class="sxs-lookup"><span data-stu-id="03c77-104">Specifies whether an encoder must be included in the transcode topology.</span></span>

<span data-ttu-id="03c77-105">La fonction [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) vérifie cet attribut pendant la génération de la topologie.</span><span class="sxs-lookup"><span data-stu-id="03c77-105">The [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function checks this attribute during topology building.</span></span> <span data-ttu-id="03c77-106">Si cet attribut n’est pas défini, un encodeur est inséré dans la topologie de transcodage.</span><span class="sxs-lookup"><span data-stu-id="03c77-106">If this attribute is not set, an encoder is inserted in the transcode topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="03c77-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="03c77-107">Data type</span></span>

<span data-ttu-id="03c77-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="03c77-108">**UINT32**</span></span>



| <span data-ttu-id="03c77-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="03c77-109">Value</span></span>                                                                        | <span data-ttu-id="03c77-110">Signification</span><span class="sxs-lookup"><span data-stu-id="03c77-110">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03c77-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="03c77-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="03c77-112">Un encodeur est inséré dans la topologie de transcodage.</span><span class="sxs-lookup"><span data-stu-id="03c77-112">An encoder is inserted in the transcode topology.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="03c77-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="03c77-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="03c77-114">Un encodeur n’est pas inclus dans la topologie de transcodage.</span><span class="sxs-lookup"><span data-stu-id="03c77-114">An encoder is not included in the transcode topology.</span></span> <span data-ttu-id="03c77-115">Le nœud source est connecté au nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="03c77-115">The source node is connected to the output node.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="03c77-116">Notes</span><span class="sxs-lookup"><span data-stu-id="03c77-116">Remarks</span></span>

<span data-ttu-id="03c77-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="03c77-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="03c77-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03c77-118">Requirements</span></span>



| <span data-ttu-id="03c77-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03c77-119">Requirement</span></span> | <span data-ttu-id="03c77-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="03c77-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03c77-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03c77-121">Minimum supported client</span></span><br/> | <span data-ttu-id="03c77-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03c77-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="03c77-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03c77-123">Minimum supported server</span></span><br/> | <span data-ttu-id="03c77-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03c77-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="03c77-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="03c77-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="03c77-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="03c77-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c77-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03c77-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c77-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03c77-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="03c77-129">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03c77-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




