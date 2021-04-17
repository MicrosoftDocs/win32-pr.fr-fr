---
description: Spécifie si la session multimédia tente de modifier la topologie lorsque le format d’un flux de contenu change.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: Attribut MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484801"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a><span data-ttu-id="ad74b-103">\_Attribut modification dynamique de la topologie MF \_ \_ \_ non \_ autorisé</span><span class="sxs-lookup"><span data-stu-id="ad74b-103">MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute</span></span>

<span data-ttu-id="ad74b-104">Spécifie si la session multimédia tente de modifier la topologie lorsque le format d’un flux de contenu change.</span><span class="sxs-lookup"><span data-stu-id="ad74b-104">Specifies whether the Media Session attempts to modify the topology when the format of a stream changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad74b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ad74b-105">Data type</span></span>

<span data-ttu-id="ad74b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ad74b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ad74b-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="ad74b-107">Get/set</span></span>

<span data-ttu-id="ad74b-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ad74b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ad74b-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ad74b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ad74b-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="ad74b-110">Applies to</span></span>

[<span data-ttu-id="ad74b-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="ad74b-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="ad74b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ad74b-112">Remarks</span></span>

<span data-ttu-id="ad74b-113">Cet attribut contrôle la manière dont la session multimédia répond si le format d’un flux est modifié pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="ad74b-113">This attribute controls how the Media Session responds if the format of a stream changes during streaming.</span></span>

<span data-ttu-id="ad74b-114">Si le format change et que l' \_ attribut modification dynamique de la topologie MF \_ \_ \_ n' \_ est pas autorisé a la **valeur false**, la session multimédia peut insérer de nouveaux nœuds dans la topologie pour qu’ils correspondent au nouveau format.</span><span class="sxs-lookup"><span data-stu-id="ad74b-114">If the format changes and the MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute is **FALSE**, the Media Session might insert new nodes into the topology to match the new format.</span></span> <span data-ttu-id="ad74b-115">Par exemple, si la taille de la vidéo change, la session multimédia peut ajouter une transformation de Media Foundation (MFT) qui redimensionne la vidéo.</span><span class="sxs-lookup"><span data-stu-id="ad74b-115">For example, if the video size changes, the Media Session might add a Media Foundation transform (MFT) that resizes the video.</span></span> <span data-ttu-id="ad74b-116">Sinon, si l’attribut a la **valeur true**, la session multimédia ne modifiera pas la topologie.</span><span class="sxs-lookup"><span data-stu-id="ad74b-116">Otherwise, if the attribute is **TRUE**, the Media Session will not modify the topology.</span></span>

<span data-ttu-id="ad74b-117">La valeur par défaut de cet attribut est **false**.</span><span class="sxs-lookup"><span data-stu-id="ad74b-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="ad74b-118">La valeur recommandée est **false**.</span><span class="sxs-lookup"><span data-stu-id="ad74b-118">The recommended value is **FALSE**.</span></span>

<span data-ttu-id="ad74b-119">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ad74b-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad74b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad74b-120">Requirements</span></span>



| <span data-ttu-id="ad74b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad74b-121">Requirement</span></span> | <span data-ttu-id="ad74b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad74b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad74b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad74b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ad74b-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad74b-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ad74b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad74b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ad74b-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad74b-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ad74b-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad74b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad74b-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad74b-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad74b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad74b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad74b-130">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad74b-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad74b-131">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="ad74b-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




