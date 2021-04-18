---
description: Spécifie la bande passante de lien pour la source réseau, en bits par seconde.
ms.assetid: 1b71dce1-8744-4114-9629-2a9d0afb7c43
title: MFNETSOURCE_CONNECTIONBANDWIDTH, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b852b3eb8dbfe5d3abc85e2223e868c5be708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527382"
---
# <a name="mfnetsource_connectionbandwidth-property"></a><span data-ttu-id="958cd-103">MFNETSOURCE \_ propriété CONNECTIONBANDWIDTH</span><span class="sxs-lookup"><span data-stu-id="958cd-103">MFNETSOURCE\_CONNECTIONBANDWIDTH property</span></span>

<span data-ttu-id="958cd-104">Spécifie la bande passante de lien pour la source réseau, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="958cd-104">Specifies the link bandwidth for the network source, in bits per second.</span></span>



<span data-ttu-id="958cd-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="958cd-105">Data type</span></span>

<span data-ttu-id="958cd-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="958cd-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="958cd-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="958cd-107">PROPVARIANT member</span></span>

<span data-ttu-id="958cd-108">**DWORD** (stocké en tant que **long**)</span><span class="sxs-lookup"><span data-stu-id="958cd-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="958cd-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="958cd-109">VT\_I4</span></span>

<span data-ttu-id="958cd-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="958cd-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="958cd-111">Notes</span><span class="sxs-lookup"><span data-stu-id="958cd-111">Remarks</span></span>

<span data-ttu-id="958cd-112">La constante **MFNETSOURCE \_ CONNECTIONBANDWIDTH** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="958cd-112">The constant **MFNETSOURCE\_CONNECTIONBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="958cd-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="958cd-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="958cd-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="958cd-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="958cd-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="958cd-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="958cd-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="958cd-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="958cd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="958cd-117">Requirements</span></span>



| <span data-ttu-id="958cd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="958cd-118">Requirement</span></span> | <span data-ttu-id="958cd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="958cd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="958cd-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="958cd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="958cd-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="958cd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="958cd-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="958cd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="958cd-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="958cd-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="958cd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="958cd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="958cd-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="958cd-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="958cd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="958cd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="958cd-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="958cd-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="958cd-128">Fonctionnalités de la source réseau</span><span class="sxs-lookup"><span data-stu-id="958cd-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="958cd-129">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="958cd-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




