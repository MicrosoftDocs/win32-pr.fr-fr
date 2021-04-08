---
description: Durée maximale de la diffusion en continu accélérée, en millisecondes, lorsque la source réseau utilise le transport UDP.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035189"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a><span data-ttu-id="06291-103">MFNETSOURCE \_ propriété MAXUDPACCELERATEDSTREAMINGDURATION</span><span class="sxs-lookup"><span data-stu-id="06291-103">MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="06291-104">Durée maximale de la diffusion en continu accélérée, en millisecondes, lorsque la source réseau utilise le transport UDP.</span><span class="sxs-lookup"><span data-stu-id="06291-104">Maximum duration of accelerated streaming, in milliseconds, when the network source uses UDP transport.</span></span>



<span data-ttu-id="06291-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="06291-105">Data type</span></span>

<span data-ttu-id="06291-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="06291-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="06291-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="06291-107">PROPVARIANT member</span></span>

<span data-ttu-id="06291-108">**DWORD** (stocké en tant que **long**)</span><span class="sxs-lookup"><span data-stu-id="06291-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="06291-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="06291-109">VT\_I4</span></span>

<span data-ttu-id="06291-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="06291-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="06291-111">Notes</span><span class="sxs-lookup"><span data-stu-id="06291-111">Remarks</span></span>

<span data-ttu-id="06291-112">La constante **MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="06291-112">The constant **MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="06291-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="06291-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="06291-114">Pour le transport UDP, cette propriété remplace la propriété [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) si la valeur de cette propriété est inférieure.</span><span class="sxs-lookup"><span data-stu-id="06291-114">For UDP transport, this property overrides the [**MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) property if the value of this property is lower.</span></span>

<span data-ttu-id="06291-115">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="06291-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="06291-116">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="06291-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="06291-117">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="06291-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="06291-118">La valeur par défaut de cette propriété est 8 000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="06291-118">The default value of this property is 8,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="06291-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06291-119">Requirements</span></span>



| <span data-ttu-id="06291-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06291-120">Requirement</span></span> | <span data-ttu-id="06291-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="06291-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06291-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06291-122">Minimum supported client</span></span><br/> | <span data-ttu-id="06291-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06291-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="06291-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06291-124">Minimum supported server</span></span><br/> | <span data-ttu-id="06291-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06291-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="06291-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="06291-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="06291-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="06291-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06291-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06291-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06291-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06291-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="06291-130">Fonctionnalités de la source réseau</span><span class="sxs-lookup"><span data-stu-id="06291-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="06291-131">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06291-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




