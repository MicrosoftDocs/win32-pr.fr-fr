---
description: Spécifie quand une transformation est vidée.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: Attribut MF_TOPONODE_FLUSH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea241227d70d967f6f41ccd994176e9ddbbacbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529698"
---
# <a name="mf_toponode_flush-attribute"></a><span data-ttu-id="db59a-103">\_Attribut de \_ vidage TOPONODE MF</span><span class="sxs-lookup"><span data-stu-id="db59a-103">MF\_TOPONODE\_FLUSH attribute</span></span>

<span data-ttu-id="db59a-104">Spécifie quand une transformation est vidée.</span><span class="sxs-lookup"><span data-stu-id="db59a-104">Specifies when a transform is flushed.</span></span>

## <a name="data-type"></a><span data-ttu-id="db59a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="db59a-105">Data type</span></span>

<span data-ttu-id="db59a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="db59a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="db59a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="db59a-107">Remarks</span></span>

<span data-ttu-id="db59a-108">Cet attribut s’applique aux nœuds de transformation (**\_ nœud de \_ transformation \_ de topologie MF**).</span><span class="sxs-lookup"><span data-stu-id="db59a-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="db59a-109">La valeur de l’attribut est un membre de l’énumération du [**\_ mode de \_ vidage \_ MF TOPONODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) .</span><span class="sxs-lookup"><span data-stu-id="db59a-109">The value of the attribute is a member of the [**MF\_TOPONODE\_FLUSH\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) enumeration.</span></span> <span data-ttu-id="db59a-110">Si cet attribut n’est pas défini, la valeur par défaut est **MF \_ TOPONODE \_ flush \_ Always**.</span><span class="sxs-lookup"><span data-stu-id="db59a-110">If this attribute is not set, the default value is **MF\_TOPONODE\_FLUSH\_ALWAYS**.</span></span>

<span data-ttu-id="db59a-111">Le vidage est effectué en appelant [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) sur la transformation à l’aide du message de vidage de la [**\_ commande du message \_ \_ MFT**](mft-message-command-flush.md) .</span><span class="sxs-lookup"><span data-stu-id="db59a-111">Flushing is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_FLUSH**](mft-message-command-flush.md) message.</span></span> <span data-ttu-id="db59a-112">Pour plus d’informations, consultez énumération des [**\_ \_ types de messages MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .</span><span class="sxs-lookup"><span data-stu-id="db59a-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="db59a-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="db59a-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="db59a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db59a-114">Requirements</span></span>



| <span data-ttu-id="db59a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db59a-115">Requirement</span></span> | <span data-ttu-id="db59a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="db59a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db59a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db59a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="db59a-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db59a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db59a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db59a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="db59a-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db59a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="db59a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="db59a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="db59a-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db59a-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db59a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db59a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db59a-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db59a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="db59a-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="db59a-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="db59a-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="db59a-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="db59a-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="db59a-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="db59a-128">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="db59a-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




