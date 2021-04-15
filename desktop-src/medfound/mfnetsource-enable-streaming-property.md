---
description: Spécifie si tous les protocoles de diffusion en continu sont activés.
ms.assetid: cf072572-58f7-429a-954a-8808d05248f0
title: MFNETSOURCE_ENABLE_STREAMING, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc8ae10dedd5cb904e43ee79ff64e8f451e37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527376"
---
# <a name="mfnetsource_enable_streaming-property"></a><span data-ttu-id="e448d-103">MFNETSOURCE \_ activer la \_ propriété streaming</span><span class="sxs-lookup"><span data-stu-id="e448d-103">MFNETSOURCE\_ENABLE\_STREAMING property</span></span>

<span data-ttu-id="e448d-104">Spécifie si tous les protocoles de diffusion en continu sont activés.</span><span class="sxs-lookup"><span data-stu-id="e448d-104">Specifies whether all streaming protocols are enabled.</span></span>



<span data-ttu-id="e448d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e448d-105">Data type</span></span>

<span data-ttu-id="e448d-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e448d-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e448d-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e448d-107">PROPVARIANT member</span></span>

<span data-ttu-id="e448d-108">Boolean (**long**)</span><span class="sxs-lookup"><span data-stu-id="e448d-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="e448d-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="e448d-109">VT\_I4</span></span>

<span data-ttu-id="e448d-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="e448d-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e448d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e448d-111">Remarks</span></span>

<span data-ttu-id="e448d-112">La constante **MFNETSOURCE \_ activer la \_ diffusion en continu** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="e448d-112">The constant **MFNETSOURCE\_ENABLE\_STREAMING** defines the GUID for this property key.</span></span> <span data-ttu-id="e448d-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e448d-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e448d-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="e448d-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="e448d-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** à la [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e448d-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e448d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e448d-116">Requirements</span></span>



| <span data-ttu-id="e448d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e448d-117">Requirement</span></span> | <span data-ttu-id="e448d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e448d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e448d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e448d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e448d-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e448d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e448d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e448d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e448d-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e448d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e448d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e448d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e448d-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e448d-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e448d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e448d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e448d-126">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e448d-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e448d-127">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e448d-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="e448d-128">Protocoles pris en charge</span><span class="sxs-lookup"><span data-stu-id="e448d-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




