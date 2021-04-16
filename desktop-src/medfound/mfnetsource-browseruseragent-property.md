---
description: La valeur de la première partie du &\# 0034 ; CS (User-Agent) &\# 0034 ; champ que la source réseau utilise pour la journalisation.
ms.assetid: b6c33cc8-ff43-4a19-a333-51a7f9b265a9
title: MFNETSOURCE_BROWSERUSERAGENT, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cbb4dcd5558c59da20e75209529c16fc0c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527387"
---
# <a name="mfnetsource_browseruseragent-property"></a><span data-ttu-id="a26e5-103">MFNETSOURCE \_ propriété BROWSERUSERAGENT</span><span class="sxs-lookup"><span data-stu-id="a26e5-103">MFNETSOURCE\_BROWSERUSERAGENT property</span></span>

<span data-ttu-id="a26e5-104">Valeur de la première partie du champ « cs (User-Agent) » que la source réseau utilise pour la journalisation.</span><span class="sxs-lookup"><span data-stu-id="a26e5-104">The value of the first portion of the "cs(User-Agent)" field that the network source uses for logging.</span></span> <span data-ttu-id="a26e5-105">Les applications peuvent définir cette propriété sur n’importe quelle valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a26e5-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="a26e5-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="a26e5-106">Data type</span></span>

<span data-ttu-id="a26e5-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a26e5-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a26e5-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a26e5-108">PROPVARIANT member</span></span>

<span data-ttu-id="a26e5-109">Chaîne de caractères larges (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="a26e5-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="a26e5-110">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="a26e5-110">VT\_LPWSTR</span></span>

<span data-ttu-id="a26e5-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="a26e5-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a26e5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a26e5-112">Remarks</span></span>

<span data-ttu-id="a26e5-113">La constante **MFNETSOURCE \_ BROWSERUSERAGENT** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="a26e5-113">The constant **MFNETSOURCE\_BROWSERUSERAGENT** defines the GUID for this property key.</span></span> <span data-ttu-id="a26e5-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a26e5-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a26e5-115">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="a26e5-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="a26e5-116">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="a26e5-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a26e5-117">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a26e5-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a26e5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a26e5-118">Requirements</span></span>



| <span data-ttu-id="a26e5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a26e5-119">Requirement</span></span> | <span data-ttu-id="a26e5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a26e5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a26e5-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a26e5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a26e5-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a26e5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a26e5-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a26e5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a26e5-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a26e5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a26e5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a26e5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a26e5-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a26e5-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a26e5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a26e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a26e5-128">Journalisation du client</span><span class="sxs-lookup"><span data-stu-id="a26e5-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="a26e5-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a26e5-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a26e5-130">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a26e5-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a26e5-131">**MFNETSOURCE \_ PLAYERUSERAGENT**</span><span class="sxs-lookup"><span data-stu-id="a26e5-131">**MFNETSOURCE\_PLAYERUSERAGENT**</span></span>](mfnetsource-playeruseragent-property.md)
</dt> </dl>

 

 




