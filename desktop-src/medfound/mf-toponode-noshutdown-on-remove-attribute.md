---
description: Spécifie comment la session multimédia arrête un objet dans la topologie.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: Attribut MF_TOPONODE_NOSHUTDOWN_ON_REMOVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545801"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a><span data-ttu-id="8a247-103">\_TOPONODE \_ de mise à l’arrêt MF sur la \_ Suppression de l' \_ attribut</span><span class="sxs-lookup"><span data-stu-id="8a247-103">MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE attribute</span></span>

<span data-ttu-id="8a247-104">Spécifie comment la session multimédia arrête un objet dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="8a247-104">Specifies how the Media Session shuts down an object in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="8a247-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8a247-105">Data type</span></span>

<span data-ttu-id="8a247-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8a247-106">**UINT32**</span></span>

<span data-ttu-id="8a247-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="8a247-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a247-108">Notes</span><span class="sxs-lookup"><span data-stu-id="8a247-108">Remarks</span></span>

<span data-ttu-id="8a247-109">Cet attribut s’applique aux types de nœuds topologie suivants :</span><span class="sxs-lookup"><span data-stu-id="8a247-109">This attribute applies to the following types of toplogy node:</span></span>

-   <span data-ttu-id="8a247-110">Nœuds de sortie</span><span class="sxs-lookup"><span data-stu-id="8a247-110">Output nodes</span></span>
-   <span data-ttu-id="8a247-111">Tout nœud de transformation qui contient une transformation de Media Foundation *asynchrone* (MFT).</span><span class="sxs-lookup"><span data-stu-id="8a247-111">Any transform node that contains an *asynchronous* Media Foundation transform (MFT).</span></span>

<span data-ttu-id="8a247-112">L’attribut peut avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a247-112">The attribute can have the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8a247-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a247-113">Value</span></span></th>
<th><span data-ttu-id="8a247-114">Description</span><span class="sxs-lookup"><span data-stu-id="8a247-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a247-115"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="8a247-115"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="8a247-116">Lorsque la session multimédia bascule vers une nouvelle topologie ou efface la topologie actuelle, elle n’arrête pas l’objet qui appartient à ce nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="8a247-116">When the Media Session switches to a new topology or clears the current topology, it does not shut down the object that belongs to this topology node.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a247-117"><strong>FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="8a247-117"><strong>FALSE</strong></span></span></td>
<td><span data-ttu-id="8a247-118">Lorsque la session multimédia bascule vers une nouvelle topologie ou efface la topologie actuelle, elle arrête l’objet de nœud, comme suit :</span><span class="sxs-lookup"><span data-stu-id="8a247-118">When the Media Session switches to a new topology or clears the current topology, it shuts down the node object, as follows:</span></span>
<ul>
<li><span data-ttu-id="8a247-119">Nœuds de sortie : la session appelle <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink :: Shutdown</strong></a> sur le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="8a247-119">Output nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink::Shutdown</strong></a> on the media sink.</span></span></li>
<li><span data-ttu-id="8a247-120">Nœuds de transformation : la session appelle <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown :: Shutdown</strong></a> sur la MFT.</span><span class="sxs-lookup"><span data-stu-id="8a247-120">Transform nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown::Shutdown</strong></a> on the MFT.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8a247-121">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="8a247-121">The default value is **TRUE**.</span></span>

<span data-ttu-id="8a247-122">Si votre application met en file d’attente plusieurs topologies, il est judicieux de définir cet attribut sur **false**.</span><span class="sxs-lookup"><span data-stu-id="8a247-122">If your application queues multiple topologies, it is a good idea to set this attribute to **FALSE**.</span></span> <span data-ttu-id="8a247-123">Sinon, les objets de la topologie peuvent ne pas être arrêtés correctement.</span><span class="sxs-lookup"><span data-stu-id="8a247-123">Otherwise, objects in the topology might not be shut down correctly.</span></span>

<span data-ttu-id="8a247-124">Cet attribut ne s’applique pas lorsque l’application arrête la session multimédia en appelant [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="8a247-124">This attribute does not apply when the application shuts down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="8a247-125">Lorsque la session multimédia s’arrête, elle arrête toujours les récepteurs multimédia et les MFTs asynchrones dans la topologie actuelle.</span><span class="sxs-lookup"><span data-stu-id="8a247-125">When the Media Session shuts down, it always shuts down the media sinks and asynchronous MFTs in the current topology.</span></span>

<span data-ttu-id="8a247-126">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8a247-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a247-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a247-127">Requirements</span></span>



| <span data-ttu-id="8a247-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a247-128">Requirement</span></span> | <span data-ttu-id="8a247-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a247-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a247-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a247-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8a247-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a247-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8a247-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a247-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8a247-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a247-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8a247-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a247-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a247-135"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a247-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a247-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a247-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a247-137">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8a247-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8a247-138">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="8a247-138">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="8a247-139">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="8a247-139">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="8a247-140">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8a247-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8a247-141">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8a247-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8a247-142">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="8a247-142">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




