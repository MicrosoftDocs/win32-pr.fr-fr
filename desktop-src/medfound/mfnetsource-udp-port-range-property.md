---
description: Plage de ports UDP valides que la source réseau peut utiliser pour recevoir du contenu de diffusion en continu.
ms.assetid: 97fe2d11-70f7-4baa-b49f-513d90146591
title: MFNETSOURCE_UDP_PORT_RANGE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04db8c450bd20adc8c03ec3b964b543f1500aa51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518542"
---
# <a name="mfnetsource_udp_port_range-property"></a><span data-ttu-id="944f5-103">Propriété de la \_ \_ plage de ports UDP MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="944f5-103">MFNETSOURCE\_UDP\_PORT\_RANGE property</span></span>

<span data-ttu-id="944f5-104">Plage de ports UDP valides que la source réseau peut utiliser pour recevoir du contenu de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="944f5-104">The range of valid UDP ports that the network source can use to receive streaming content.</span></span> <span data-ttu-id="944f5-105">La valeur de cette propriété est une chaîne au format " *m*–*n* ", où *m* et *n* sont les numéros de port.</span><span class="sxs-lookup"><span data-stu-id="944f5-105">The value of this property is a string with the form " *m*–*n* " where *m* and *n* are port numbers.</span></span>



<span data-ttu-id="944f5-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="944f5-106">Data type</span></span>

<span data-ttu-id="944f5-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="944f5-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="944f5-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="944f5-108">PROPVARIANT member</span></span>

<span data-ttu-id="944f5-109">Chaîne de caractères larges (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="944f5-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="944f5-110">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="944f5-110">VT\_LPWSTR</span></span>

<span data-ttu-id="944f5-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="944f5-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="944f5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="944f5-112">Remarks</span></span>

<span data-ttu-id="944f5-113">La **plage de \_ \_ ports UDP \_ constante MFNETSOURCE** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="944f5-113">The constant **MFNETSOURCE\_UDP\_PORT\_RANGE** defines the GUID for this property key.</span></span> <span data-ttu-id="944f5-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="944f5-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="944f5-115">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="944f5-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="944f5-116">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="944f5-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="944f5-117">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="944f5-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="944f5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="944f5-118">Requirements</span></span>



| <span data-ttu-id="944f5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="944f5-119">Requirement</span></span> | <span data-ttu-id="944f5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="944f5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="944f5-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="944f5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="944f5-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="944f5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="944f5-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="944f5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="944f5-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="944f5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="944f5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="944f5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="944f5-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="944f5-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="944f5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="944f5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="944f5-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="944f5-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="944f5-129">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="944f5-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




