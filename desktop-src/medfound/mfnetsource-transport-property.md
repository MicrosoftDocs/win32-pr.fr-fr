---
description: Spécifie le protocole de transport utilisé par la source réseau.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: MFNETSOURCE_TRANSPORT, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd41653f2b5ea0686527af4d6ee8c8b9962005aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863157"
---
# <a name="mfnetsource_transport-property"></a><span data-ttu-id="f38a1-103">\_Propriété de transport MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="f38a1-103">MFNETSOURCE\_TRANSPORT property</span></span>

<span data-ttu-id="f38a1-104">Spécifie le protocole de transport utilisé par la source réseau.</span><span class="sxs-lookup"><span data-stu-id="f38a1-104">Specifies the transport protocol used by the network source.</span></span> <span data-ttu-id="f38a1-105">La valeur de cette propriété est un membre de l’énumération du [**\_ \_ type de transport MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .</span><span class="sxs-lookup"><span data-stu-id="f38a1-105">The value of this property is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>



<span data-ttu-id="f38a1-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="f38a1-106">Data type</span></span>

<span data-ttu-id="f38a1-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f38a1-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f38a1-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f38a1-108">PROPVARIANT member</span></span>

<span data-ttu-id="f38a1-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="f38a1-109">**LONG**</span></span>

<span data-ttu-id="f38a1-110">VT \_</span><span class="sxs-lookup"><span data-stu-id="f38a1-110">VT\_I4</span></span>

<span data-ttu-id="f38a1-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="f38a1-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f38a1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f38a1-112">Remarks</span></span>

<span data-ttu-id="f38a1-113">La constante **MFNETSOURCE \_ transport** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="f38a1-113">The constant **MFNETSOURCE\_TRANSPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="f38a1-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f38a1-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="f38a1-115">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f38a1-115">This property is read-only.</span></span> <span data-ttu-id="f38a1-116">Pour récupérer cette propriété, interrogez la source réseau de l’interface **IPropertyStore** et appelez **IPropertyStore :: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="f38a1-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f38a1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f38a1-117">Requirements</span></span>



| <span data-ttu-id="f38a1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f38a1-118">Requirement</span></span> | <span data-ttu-id="f38a1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f38a1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f38a1-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f38a1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f38a1-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f38a1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f38a1-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f38a1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f38a1-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f38a1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f38a1-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f38a1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f38a1-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f38a1-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f38a1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f38a1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38a1-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f38a1-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f38a1-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f38a1-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f38a1-129">Protocoles pris en charge</span><span class="sxs-lookup"><span data-stu-id="f38a1-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




