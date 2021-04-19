---
description: Spécifie si le protocole de multidiffusion de diffusion multimédia en continu (MSB) est activé dans la source réseau.
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: MFNETSOURCE_ENABLE_MSB, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b2a49876cf504bfc4e086ab1e064e6835283a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513019"
---
# <a name="mfnetsource_enable_msb-property"></a><span data-ttu-id="aae67-103">MFNETSOURCE \_ activer la \_ propriété MSB</span><span class="sxs-lookup"><span data-stu-id="aae67-103">MFNETSOURCE\_ENABLE\_MSB property</span></span>

<span data-ttu-id="aae67-104">Spécifie si le protocole de multidiffusion de diffusion multimédia en continu (MSB) est activé dans la source réseau.</span><span class="sxs-lookup"><span data-stu-id="aae67-104">Specifies whether the Media Stream Broadcast (MSB) multicast protocol is enabled in the network source.</span></span>



<span data-ttu-id="aae67-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="aae67-105">Data type</span></span>

<span data-ttu-id="aae67-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="aae67-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="aae67-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="aae67-107">PROPVARIANT member</span></span>

<span data-ttu-id="aae67-108">**LONG**</span><span class="sxs-lookup"><span data-stu-id="aae67-108">**LONG**</span></span>

<span data-ttu-id="aae67-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="aae67-109">VT\_I4</span></span>

<span data-ttu-id="aae67-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="aae67-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="aae67-111">Notes</span><span class="sxs-lookup"><span data-stu-id="aae67-111">Remarks</span></span>

<span data-ttu-id="aae67-112">La constante **MFNETSOURCE \_ Enable \_ MSB** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="aae67-112">The constant **MFNETSOURCE\_ENABLE\_MSB** defines the GUID for this property key.</span></span> <span data-ttu-id="aae67-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="aae67-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="aae67-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="aae67-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="aae67-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="aae67-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="aae67-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="aae67-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aae67-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aae67-117">Requirements</span></span>



| <span data-ttu-id="aae67-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aae67-118">Requirement</span></span> | <span data-ttu-id="aae67-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="aae67-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aae67-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aae67-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aae67-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aae67-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="aae67-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aae67-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aae67-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aae67-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="aae67-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="aae67-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aae67-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae67-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae67-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aae67-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae67-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aae67-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="aae67-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aae67-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="aae67-129">Protocoles pris en charge</span><span class="sxs-lookup"><span data-stu-id="aae67-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




