---
description: Spécifie quand une transformation est vidée.
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: Attribut MF_TOPONODE_DRAIN (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534371"
---
# <a name="mf_toponode_drain-attribute"></a><span data-ttu-id="5277f-103">\_ \_ Attribut drain TOPONODE MF</span><span class="sxs-lookup"><span data-stu-id="5277f-103">MF\_TOPONODE\_DRAIN attribute</span></span>

<span data-ttu-id="5277f-104">Spécifie quand une transformation est vidée.</span><span class="sxs-lookup"><span data-stu-id="5277f-104">Specifies when a transform is drained.</span></span>

## <a name="data-type"></a><span data-ttu-id="5277f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5277f-105">Data type</span></span>

<span data-ttu-id="5277f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5277f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5277f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5277f-107">Remarks</span></span>

<span data-ttu-id="5277f-108">Cet attribut s’applique aux nœuds de transformation (**\_ nœud de \_ transformation \_ de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="5277f-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="5277f-109">La valeur de l’attribut est un membre de l’énumération du [**\_ mode de \_ drainage \_ MF TOPONODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) .</span><span class="sxs-lookup"><span data-stu-id="5277f-109">The value of the attribute is a member of the [**MF\_TOPONODE\_DRAIN\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) enumeration.</span></span> <span data-ttu-id="5277f-110">Si cet attribut n’est pas défini, la valeur par défaut est **MF \_ TOPONODE \_ drain \_ default**.</span><span class="sxs-lookup"><span data-stu-id="5277f-110">If this attribute is not set, the default value is **MF\_TOPONODE\_DRAIN\_DEFAULT**.</span></span>

<span data-ttu-id="5277f-111">La vidange est effectuée en appelant [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) sur la transformation à l’aide du message de [**\_ drainage de \_ commande \_ de message MFT**](mft-message-command-drain.md) .</span><span class="sxs-lookup"><span data-stu-id="5277f-111">Draining is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_DRAIN**](mft-message-command-drain.md) message.</span></span> <span data-ttu-id="5277f-112">Pour plus d’informations, consultez énumération des [**\_ \_ types de messages MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .</span><span class="sxs-lookup"><span data-stu-id="5277f-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="5277f-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5277f-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5277f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5277f-114">Requirements</span></span>



| <span data-ttu-id="5277f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5277f-115">Requirement</span></span> | <span data-ttu-id="5277f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5277f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5277f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5277f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5277f-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5277f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5277f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5277f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5277f-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5277f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5277f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5277f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5277f-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5277f-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5277f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5277f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5277f-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5277f-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5277f-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5277f-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5277f-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5277f-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5277f-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="5277f-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="5277f-128">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="5277f-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




