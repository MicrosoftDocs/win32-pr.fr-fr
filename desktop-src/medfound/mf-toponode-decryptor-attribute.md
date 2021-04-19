---
description: Spécifie si un objet sous-jacent de nœuds topologie est un Decrypter.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: Attribut MF_TOPONODE_DECRYPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520751"
---
# <a name="mf_toponode_decryptor-attribute"></a><span data-ttu-id="9c614-103">\_Attribut de \_ déchiffreur MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="9c614-103">MF\_TOPONODE\_DECRYPTOR attribute</span></span>

<span data-ttu-id="9c614-104">Spécifie si l’objet sous-jacent d’un nœud topologie est un Decrypter.</span><span class="sxs-lookup"><span data-stu-id="9c614-104">Specifies whether a toplogy node's underlying object is a decrypter.</span></span>

## <a name="data-type"></a><span data-ttu-id="9c614-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="9c614-105">Data type</span></span>

<span data-ttu-id="9c614-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9c614-106">**UINT32**</span></span>

<span data-ttu-id="9c614-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="9c614-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c614-108">Notes</span><span class="sxs-lookup"><span data-stu-id="9c614-108">Remarks</span></span>

<span data-ttu-id="9c614-109">Cet attribut s’applique à tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="9c614-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="9c614-110">Si la valeur de cet attribut est différente de zéro, l’objet sous-jacent du nœud est un Decrypter.</span><span class="sxs-lookup"><span data-stu-id="9c614-110">If the value of this attribute is nonzero, the node's underlying object is a decrypter.</span></span>

<span data-ttu-id="9c614-111">En général, les applications n’utilisent pas cet attribut directement.</span><span class="sxs-lookup"><span data-stu-id="9c614-111">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="9c614-112">La session multimédia définit cet attribut lors de la création d’un nœud pour un Decrypter, obtenu à partir de la méthode [**IMFInputTrustAuthority :: GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) .</span><span class="sxs-lookup"><span data-stu-id="9c614-112">The Media Session sets this attribute when it creates a node for a decrypter, obtained from the [**IMFInputTrustAuthority::GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) method.</span></span>

<span data-ttu-id="9c614-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9c614-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c614-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c614-114">Requirements</span></span>



| <span data-ttu-id="9c614-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c614-115">Requirement</span></span> | <span data-ttu-id="9c614-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c614-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c614-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c614-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c614-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c614-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9c614-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c614-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c614-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c614-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c614-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c614-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c614-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c614-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c614-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c614-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c614-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c614-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9c614-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9c614-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9c614-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9c614-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9c614-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="9c614-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="9c614-128">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="9c614-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




