---
description: Spécifie le protocole de contrôle utilisé par la source réseau.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: MFNETSOURCE_PROTOCOL, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188eeb1f6669544291f4dca95db8a4a45a50d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525978"
---
# <a name="mfnetsource_protocol-property"></a><span data-ttu-id="53399-103">\_Propriété de protocole MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="53399-103">MFNETSOURCE\_PROTOCOL property</span></span>

<span data-ttu-id="53399-104">Spécifie le protocole de contrôle utilisé par la source réseau.</span><span class="sxs-lookup"><span data-stu-id="53399-104">Specifies the control protocol used by the network source.</span></span> <span data-ttu-id="53399-105">La valeur de cette propriété est un membre de l’énumération du [**\_ \_ type de protocole MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="53399-105">The value of this property is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>



<span data-ttu-id="53399-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="53399-106">Data type</span></span>

<span data-ttu-id="53399-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="53399-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="53399-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="53399-108">PROPVARIANT member</span></span>

<span data-ttu-id="53399-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="53399-109">**LONG**</span></span>

<span data-ttu-id="53399-110">VT \_</span><span class="sxs-lookup"><span data-stu-id="53399-110">VT\_I4</span></span>

<span data-ttu-id="53399-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="53399-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="53399-112">Notes</span><span class="sxs-lookup"><span data-stu-id="53399-112">Remarks</span></span>

<span data-ttu-id="53399-113">Le **\_ protocole MFNETSOURCE** constant définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="53399-113">The constant **MFNETSOURCE\_PROTOCOL** defines the GUID for this property key.</span></span> <span data-ttu-id="53399-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="53399-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="53399-115">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="53399-115">This property is read-only.</span></span> <span data-ttu-id="53399-116">Pour récupérer cette propriété, interrogez la source réseau de l’interface **IPropertyStore** et appelez **IPropertyStore :: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="53399-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="53399-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53399-117">Requirements</span></span>



| <span data-ttu-id="53399-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53399-118">Requirement</span></span> | <span data-ttu-id="53399-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="53399-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53399-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53399-120">Minimum supported client</span></span><br/> | <span data-ttu-id="53399-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53399-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="53399-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53399-122">Minimum supported server</span></span><br/> | <span data-ttu-id="53399-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53399-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="53399-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="53399-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="53399-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53399-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53399-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53399-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53399-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="53399-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="53399-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="53399-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="53399-129">Protocoles pris en charge</span><span class="sxs-lookup"><span data-stu-id="53399-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




