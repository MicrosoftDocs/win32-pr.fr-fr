---
description: Spécifie si le protocole HTTP est activé dans la source réseau.
ms.assetid: dcc4db5c-0274-4a8a-89a4-66cda62e1520
title: MFNETSOURCE_ENABLE_HTTP, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004868c92962702b774a8f6c0a9b75708c5727b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951386"
---
# <a name="mfnetsource_enable_http-property"></a><span data-ttu-id="972b0-103">MFNETSOURCE \_ activer la \_ propriété http</span><span class="sxs-lookup"><span data-stu-id="972b0-103">MFNETSOURCE\_ENABLE\_HTTP property</span></span>

<span data-ttu-id="972b0-104">Spécifie si le protocole HTTP est activé dans la source réseau.</span><span class="sxs-lookup"><span data-stu-id="972b0-104">Specifies whether HTTP protocol is enabled in the network source.</span></span>



<span data-ttu-id="972b0-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="972b0-105">Data type</span></span>

<span data-ttu-id="972b0-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="972b0-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="972b0-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="972b0-107">PROPVARIANT member</span></span>

<span data-ttu-id="972b0-108">Boolean (**long**)</span><span class="sxs-lookup"><span data-stu-id="972b0-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="972b0-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="972b0-109">VT\_I4</span></span>

<span data-ttu-id="972b0-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="972b0-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="972b0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="972b0-111">Remarks</span></span>

<span data-ttu-id="972b0-112">La constante **MFNETSOURCE \_ Enable \_ http** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="972b0-112">The constant **MFNETSOURCE\_ENABLE\_HTTP** defines the GUID for this property key.</span></span> <span data-ttu-id="972b0-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="972b0-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="972b0-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="972b0-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="972b0-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="972b0-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="972b0-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="972b0-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="972b0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="972b0-117">Requirements</span></span>



| <span data-ttu-id="972b0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="972b0-118">Requirement</span></span> | <span data-ttu-id="972b0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="972b0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="972b0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="972b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="972b0-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="972b0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="972b0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="972b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="972b0-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="972b0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="972b0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="972b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="972b0-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="972b0-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="972b0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="972b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="972b0-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="972b0-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="972b0-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="972b0-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="972b0-129">Protocoles pris en charge</span><span class="sxs-lookup"><span data-stu-id="972b0-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




