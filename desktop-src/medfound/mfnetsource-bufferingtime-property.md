---
description: Nombre de secondes de données que la source réseau met en mémoire tampon au démarrage.
ms.assetid: 186b55fc-d1b1-4187-a748-efaee114eca9
title: MFNETSOURCE_BUFFERINGTIME, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21c165e58ebd5f2aec0f1ca7ce38281f8c94896d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114003"
---
# <a name="mfnetsource_bufferingtime-property"></a><span data-ttu-id="e9d6b-103">MFNETSOURCE \_ propriété BUFFERINGTIME</span><span class="sxs-lookup"><span data-stu-id="e9d6b-103">MFNETSOURCE\_BUFFERINGTIME property</span></span>

<span data-ttu-id="e9d6b-104">Nombre de secondes de données que la source réseau met en mémoire tampon au démarrage.</span><span class="sxs-lookup"><span data-stu-id="e9d6b-104">Number of seconds of data that the network source buffers at startup.</span></span>



<span data-ttu-id="e9d6b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e9d6b-105">Data type</span></span>

<span data-ttu-id="e9d6b-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e9d6b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e9d6b-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e9d6b-107">PROPVARIANT member</span></span>

<span data-ttu-id="e9d6b-108">**DWORD** (stocké en tant que **long**)</span><span class="sxs-lookup"><span data-stu-id="e9d6b-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="e9d6b-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="e9d6b-109">VT\_I4</span></span>

<span data-ttu-id="e9d6b-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="e9d6b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e9d6b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e9d6b-111">Remarks</span></span>

<span data-ttu-id="e9d6b-112">La constante **MFNETSOURCE \_ BUFFERINGTIME** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="e9d6b-112">The constant **MFNETSOURCE\_BUFFERINGTIME** defines the GUID for this property key.</span></span> <span data-ttu-id="e9d6b-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e9d6b-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e9d6b-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="e9d6b-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="e9d6b-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="e9d6b-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="e9d6b-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e9d6b-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="e9d6b-117">La valeur par défaut de cette propriété est de 5 secondes.</span><span class="sxs-lookup"><span data-stu-id="e9d6b-117">The default value of this property is 5 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d6b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9d6b-118">Requirements</span></span>



| <span data-ttu-id="e9d6b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9d6b-119">Requirement</span></span> | <span data-ttu-id="e9d6b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9d6b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d6b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9d6b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e9d6b-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9d6b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e9d6b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9d6b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e9d6b-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9d6b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e9d6b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9d6b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9d6b-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9d6b-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9d6b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9d6b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9d6b-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9d6b-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e9d6b-129">Fonctionnalités de la source réseau</span><span class="sxs-lookup"><span data-stu-id="e9d6b-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="e9d6b-130">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9d6b-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




