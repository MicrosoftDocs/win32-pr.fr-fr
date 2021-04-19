---
description: La valeur de la deuxième partie du &\# 0034 ; CS (User-Agent) &\# 0034 ; champ que la source réseau utilise pour la journalisation.
ms.assetid: c662a6d6-5e0b-4c28-841d-5774d4103d4b
title: MFNETSOURCE_PLAYERUSERAGENT, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f4d06eaea566e22e1239ed04594f2f592c7cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543464"
---
# <a name="mfnetsource_playeruseragent-property"></a><span data-ttu-id="fea80-103">MFNETSOURCE \_ propriété PLAYERUSERAGENT</span><span class="sxs-lookup"><span data-stu-id="fea80-103">MFNETSOURCE\_PLAYERUSERAGENT property</span></span>

<span data-ttu-id="fea80-104">Valeur de la deuxième partie du champ « cs (User-Agent) » que la source réseau utilise pour la journalisation.</span><span class="sxs-lookup"><span data-stu-id="fea80-104">The value of the second portion of the "cs(User-Agent)" field that the network source uses for logging.</span></span> <span data-ttu-id="fea80-105">Les applications peuvent définir cette propriété sur n’importe quelle valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="fea80-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="fea80-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="fea80-106">Data type</span></span>

<span data-ttu-id="fea80-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="fea80-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="fea80-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="fea80-108">PROPVARIANT member</span></span>

<span data-ttu-id="fea80-109">Chaîne de caractères larges (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="fea80-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="fea80-110">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="fea80-110">VT\_LPWSTR</span></span>

<span data-ttu-id="fea80-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="fea80-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="fea80-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fea80-112">Remarks</span></span>

<span data-ttu-id="fea80-113">La constante **MFNETSOURCE \_ PLAYERUSERAGENT** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="fea80-113">The constant **MFNETSOURCE\_PLAYERUSERAGENT** defines the GUID for this property key.</span></span> <span data-ttu-id="fea80-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="fea80-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="fea80-115">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="fea80-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="fea80-116">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="fea80-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="fea80-117">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="fea80-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fea80-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fea80-118">Requirements</span></span>



| <span data-ttu-id="fea80-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fea80-119">Requirement</span></span> | <span data-ttu-id="fea80-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea80-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fea80-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fea80-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fea80-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fea80-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fea80-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fea80-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fea80-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fea80-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fea80-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fea80-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea80-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fea80-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fea80-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fea80-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea80-128">Journalisation du client</span><span class="sxs-lookup"><span data-stu-id="fea80-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="fea80-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fea80-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="fea80-130">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fea80-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="fea80-131">**MFNETSOURCE \_ BROWSERUSERAGENT**</span><span class="sxs-lookup"><span data-stu-id="fea80-131">**MFNETSOURCE\_BROWSERUSERAGENT**</span></span>](mfnetsource-browseruseragent-property.md)
</dt> </dl>

 

 




