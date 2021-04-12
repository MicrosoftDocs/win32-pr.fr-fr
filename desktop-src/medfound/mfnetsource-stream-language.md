---
description: Stocke la chaîne envoyée dans l’en-tête Accept-Language.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: MFNETSOURCE_STREAM_LANGUAGE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200c49d4a14146277c66fbb3389cf1ba6ab13fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393255"
---
# <a name="mfnetsource_stream_language-property"></a><span data-ttu-id="ac0a3-103">MFNETSOURCE \_ , \_ propriété de langage de flux</span><span class="sxs-lookup"><span data-stu-id="ac0a3-103">MFNETSOURCE\_STREAM\_LANGUAGE property</span></span>

<span data-ttu-id="ac0a3-104">Stocke la chaîne envoyée dans l’en-tête Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-104">Stores the string sent in the Accept-Language header.</span></span>



<span data-ttu-id="ac0a3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ac0a3-105">Data type</span></span>

<span data-ttu-id="ac0a3-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="ac0a3-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ac0a3-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="ac0a3-107">PROPVARIANT member</span></span>

<span data-ttu-id="ac0a3-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="ac0a3-108">\**WCHAR\** _</span></span>

<span data-ttu-id="ac0a3-109">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="ac0a3-109">VT\_LPWSTR</span></span>

<span data-ttu-id="ac0a3-110">_ *pwszVal*\*</span><span class="sxs-lookup"><span data-stu-id="ac0a3-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="ac0a3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ac0a3-111">Remarks</span></span>

<span data-ttu-id="ac0a3-112">La \_ constante MFNETSOURCE Stream \_ Language définit le GUID de la clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-112">The MFNETSOURCE\_STREAM\_LANGUAGE constant defines the GUID for the property key.</span></span> <span data-ttu-id="ac0a3-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="ac0a3-114">Pour définir cette propriété sur la source réseau, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="ac0a3-115">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="ac0a3-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac0a3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac0a3-116">Requirements</span></span>



| <span data-ttu-id="ac0a3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac0a3-117">Requirement</span></span> | <span data-ttu-id="ac0a3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac0a3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0a3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac0a3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ac0a3-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac0a3-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ac0a3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac0a3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ac0a3-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac0a3-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ac0a3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac0a3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac0a3-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac0a3-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac0a3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac0a3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac0a3-126">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac0a3-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ac0a3-127">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac0a3-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




