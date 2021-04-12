---
description: Spécifie comment le chargeur de topologie connecte ce nœud de topologie et si ce nœud est facultatif.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: Attribut MF_TOPONODE_CONNECT_METHOD (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210091"
---
# <a name="mf_toponode_connect_method-attribute"></a><span data-ttu-id="d1693-103">\_Attribut de \_ méthode de connexion MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="d1693-103">MF\_TOPONODE\_CONNECT\_METHOD attribute</span></span>

<span data-ttu-id="d1693-104">Spécifie comment le chargeur de topologie connecte ce nœud de topologie et si ce nœud est facultatif.</span><span class="sxs-lookup"><span data-stu-id="d1693-104">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>

## <a name="data-type"></a><span data-ttu-id="d1693-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d1693-105">Data type</span></span>

<span data-ttu-id="d1693-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d1693-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d1693-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d1693-107">Remarks</span></span>

<span data-ttu-id="d1693-108">Cet attribut s’applique à tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="d1693-108">This attribute applies to all node types.</span></span>

<span data-ttu-id="d1693-109">La valeur d’attribut est une **opération or au niveau du bit** des indicateurs de l’énumération de [**\_ \_ méthode MF Connect**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) .</span><span class="sxs-lookup"><span data-stu-id="d1693-109">The attribute value is a bitwise **OR** of flags from the [**MF\_CONNECT\_METHOD**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) enumeration.</span></span> <span data-ttu-id="d1693-110">Si cet attribut n’est pas défini, la valeur par défaut est **MF \_ Connect \_ autoriser le \_ décodeur**.</span><span class="sxs-lookup"><span data-stu-id="d1693-110">If this attribute is not set, the default value is **MF\_CONNECT\_ALLOW\_DECODER**.</span></span>

<span data-ttu-id="d1693-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d1693-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1693-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1693-112">Requirements</span></span>



| <span data-ttu-id="d1693-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1693-113">Requirement</span></span> | <span data-ttu-id="d1693-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1693-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1693-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1693-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d1693-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1693-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d1693-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1693-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d1693-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1693-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d1693-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1693-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1693-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1693-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1693-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1693-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1693-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1693-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1693-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d1693-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d1693-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d1693-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d1693-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="d1693-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="d1693-126">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="d1693-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




