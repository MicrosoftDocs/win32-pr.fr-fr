---
description: Spécifie la bande passante de paire de paquets et la bande passante d’exécution détectée par la source réseau.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: MFNETSOURCE_PPBANDWIDTH, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519596"
---
# <a name="mfnetsource_ppbandwidth-property"></a><span data-ttu-id="712b1-103">MFNETSOURCE \_ propriété PPBANDWIDTH</span><span class="sxs-lookup"><span data-stu-id="712b1-103">MFNETSOURCE\_PPBANDWIDTH property</span></span>

<span data-ttu-id="712b1-104">Spécifie la bande passante de paire de paquets et la bande passante d’exécution détectée par la source réseau.</span><span class="sxs-lookup"><span data-stu-id="712b1-104">Specifies the packet-pair bandwidth and run-time bandwidth detected by the network source.</span></span> <span data-ttu-id="712b1-105">La valeur de la propriété est un tableau de deux valeurs :</span><span class="sxs-lookup"><span data-stu-id="712b1-105">The property value is a array of two values:</span></span>

-   <span data-ttu-id="712b1-106">Bande passante de paires de paquets, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="712b1-106">Packet-pair bandwidth, in bits per second.</span></span>
-   <span data-ttu-id="712b1-107">Bande passante d’exécution, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="712b1-107">Run-time bandwidth, in bits per second.</span></span>



<span data-ttu-id="712b1-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="712b1-108">Data type</span></span>

<span data-ttu-id="712b1-109">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="712b1-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="712b1-110">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="712b1-110">PROPVARIANT member</span></span>

<span data-ttu-id="712b1-111">Tableau de valeurs **ULong** (**CAUL**)</span><span class="sxs-lookup"><span data-stu-id="712b1-111">Array of **ULONG** values (**CAUL**)</span></span>

<span data-ttu-id="712b1-112">VT \_ Vector \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="712b1-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="712b1-113">**caul**</span><span class="sxs-lookup"><span data-stu-id="712b1-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="712b1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="712b1-114">Remarks</span></span>

<span data-ttu-id="712b1-115">La constante **MFNETSOURCE \_ PPBANDWIDTH** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="712b1-115">The constant **MFNETSOURCE\_PPBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="712b1-116">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="712b1-116">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="712b1-117">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="712b1-117">This property is read-only.</span></span> <span data-ttu-id="712b1-118">Pour récupérer cette propriété, interrogez la source réseau de l’interface **IPropertyStore** et appelez **IPropertyStore :: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="712b1-118">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="712b1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="712b1-119">Requirements</span></span>



| <span data-ttu-id="712b1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="712b1-120">Requirement</span></span> | <span data-ttu-id="712b1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="712b1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="712b1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="712b1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="712b1-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="712b1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="712b1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="712b1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="712b1-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="712b1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="712b1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="712b1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="712b1-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="712b1-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="712b1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="712b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="712b1-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="712b1-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="712b1-130">Fonctionnalités de la source réseau</span><span class="sxs-lookup"><span data-stu-id="712b1-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="712b1-131">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="712b1-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




