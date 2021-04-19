---
description: Nombre de fois que la source réseau a tenté de se reconnecter au réseau.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: MFNETSOURCE_AUTORECONNECTPROGRESS, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534369"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a><span data-ttu-id="59c3b-103">MFNETSOURCE \_ propriété AUTORECONNECTPROGRESS</span><span class="sxs-lookup"><span data-stu-id="59c3b-103">MFNETSOURCE\_AUTORECONNECTPROGRESS property</span></span>

<span data-ttu-id="59c3b-104">Nombre de fois que la source réseau a tenté de se reconnecter au réseau.</span><span class="sxs-lookup"><span data-stu-id="59c3b-104">The number of times the network source has attempted to reconnect to the network.</span></span>



<span data-ttu-id="59c3b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="59c3b-105">Data type</span></span>

<span data-ttu-id="59c3b-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="59c3b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="59c3b-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="59c3b-107">PROPVARIANT member</span></span>

<span data-ttu-id="59c3b-108">**DWORD** (stocké en tant que **long**)</span><span class="sxs-lookup"><span data-stu-id="59c3b-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="59c3b-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="59c3b-109">VT\_I4</span></span>

<span data-ttu-id="59c3b-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="59c3b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="59c3b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="59c3b-111">Remarks</span></span>

<span data-ttu-id="59c3b-112">La constante **MFNETSOURCE \_ AUTORECONNECTPROGRESS** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="59c3b-112">The constant **MFNETSOURCE\_AUTORECONNECTPROGRESS** defines the GUID for this property key.</span></span> <span data-ttu-id="59c3b-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="59c3b-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="59c3b-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="59c3b-114">This property is read-only.</span></span> <span data-ttu-id="59c3b-115">Pour récupérer cette propriété, interrogez la source réseau de l’interface **IPropertyStore** et appelez **IPropertyStore :: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="59c3b-115">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c3b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59c3b-116">Requirements</span></span>



| <span data-ttu-id="59c3b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59c3b-117">Requirement</span></span> | <span data-ttu-id="59c3b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c3b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59c3b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59c3b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="59c3b-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59c3b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59c3b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59c3b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="59c3b-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59c3b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="59c3b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="59c3b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c3b-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c3b-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c3b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c3b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c3b-126">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59c3b-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="59c3b-127">Fonctionnalités de la source réseau</span><span class="sxs-lookup"><span data-stu-id="59c3b-127">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="59c3b-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59c3b-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




