---
description: Spécifie si une table de Media Foundation matérielle (MFT, Hardware-Based transformation) est connectée à une autre table MFT matérielle.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: Attribut MFT_CONNECTED_TO_HW_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520431"
---
# <a name="mft_connected_to_hw_stream-attribute"></a><span data-ttu-id="cb4b0-103">MFT \_ connecté \_ à \_ l' \_ attribut de flux de matériel</span><span class="sxs-lookup"><span data-stu-id="cb4b0-103">MFT\_CONNECTED\_TO\_HW\_STREAM attribute</span></span>

<span data-ttu-id="cb4b0-104">Spécifie si une table de Media Foundation matérielle (MFT, Hardware-Based transformation) est connectée à une autre table MFT matérielle.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-104">Specifies whether a hardware-based Media Foundation transform (MFT) is connected to another hardware-based MFT.</span></span>

## <a name="data-type"></a><span data-ttu-id="cb4b0-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="cb4b0-105">Data type</span></span>

<span data-ttu-id="cb4b0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cb4b0-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="cb4b0-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="cb4b0-107">Get/set</span></span>

<span data-ttu-id="cb4b0-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="cb4b0-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="cb4b0-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="cb4b0-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb4b0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="cb4b0-110">Remarks</span></span>

<span data-ttu-id="cb4b0-111">En général, les applications n’utilisent pas cet attribut.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="cb4b0-112">Cet attribut est utilisé avec les MFTs basés sur le matériel.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-112">This attribute is used with hardware-based MFTs.</span></span> <span data-ttu-id="cb4b0-113">Lorsque deux MFTs matériels sont connectés dans une topologie, le chargeur de topologie affecte la **valeur true** à cet attribut sur les objets suivants :</span><span class="sxs-lookup"><span data-stu-id="cb4b0-113">When two hardware MFTs are connected within a topology, the topology loader sets this attribute to **TRUE** on the following objects:</span></span>

-   <span data-ttu-id="cb4b0-114">Flux de sortie de la table MFT en amont</span><span class="sxs-lookup"><span data-stu-id="cb4b0-114">The output stream of the upstream MFT</span></span>
-   <span data-ttu-id="cb4b0-115">Flux d’entrée de la table MFT en aval</span><span class="sxs-lookup"><span data-stu-id="cb4b0-115">The input stream of the downstream MFT</span></span>

<span data-ttu-id="cb4b0-116">Pour obtenir le magasin d’attributs du flux de sortie, le chargeur de topologie appelle [**IMFTransform :: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) sur la table MFT en amont.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-116">To get the attribute store for the output stream, the topology loader calls [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) on the upstream MFT.</span></span> <span data-ttu-id="cb4b0-117">Pour obtenir le magasin d’attributs pour le flux d’entrée, le chargeur de topologie appelle [**IMFTransform :: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) sur la table MFT en aval.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-117">To get the attribute store for the input stream, the topology loader calls [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) on the downstream MFT.</span></span>

<span data-ttu-id="cb4b0-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4b0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb4b0-119">Requirements</span></span>



| <span data-ttu-id="cb4b0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb4b0-120">Requirement</span></span> | <span data-ttu-id="cb4b0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb4b0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4b0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb4b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4b0-123">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cb4b0-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="cb4b0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb4b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4b0-125">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cb4b0-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cb4b0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb4b0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb4b0-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb4b0-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb4b0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb4b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb4b0-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb4b0-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb4b0-130">Matériel MFTs</span><span class="sxs-lookup"><span data-stu-id="cb4b0-130">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="cb4b0-131">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="cb4b0-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




