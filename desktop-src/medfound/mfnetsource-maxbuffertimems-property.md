---
description: Quantité maximale de données que la source réseau met en mémoire tampon, en millisecondes.
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: MFNETSOURCE_MAXBUFFERTIMEMS, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f98cd17f33bb893dacd02b2a00669f3d2355e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518948"
---
# <a name="mfnetsource_maxbuffertimems-property"></a><span data-ttu-id="4c035-103">MFNETSOURCE \_ propriété MAXBUFFERTIMEMS</span><span class="sxs-lookup"><span data-stu-id="4c035-103">MFNETSOURCE\_MAXBUFFERTIMEMS property</span></span>

<span data-ttu-id="4c035-104">Quantité maximale de données que la source réseau met en mémoire tampon, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="4c035-104">Maximum amount of data the network source buffers, in milliseconds.</span></span>



<span data-ttu-id="4c035-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="4c035-105">Data type</span></span>

<span data-ttu-id="4c035-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="4c035-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4c035-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="4c035-107">PROPVARIANT member</span></span>

<span data-ttu-id="4c035-108">**DWORD** (stocké en tant que **long**)</span><span class="sxs-lookup"><span data-stu-id="4c035-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="4c035-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="4c035-109">VT\_I4</span></span>

<span data-ttu-id="4c035-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="4c035-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="4c035-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4c035-111">Remarks</span></span>

<span data-ttu-id="4c035-112">La constante **MFNETSOURCE \_ MAXBUFFERTIMEMS** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="4c035-112">The constant **MFNETSOURCE\_MAXBUFFERTIMEMS** defines the GUID for this property key.</span></span> <span data-ttu-id="4c035-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="4c035-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="4c035-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="4c035-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="4c035-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="4c035-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="4c035-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="4c035-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="4c035-117">La valeur par défaut de cette propriété est 40 000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="4c035-117">The default value of this property is 40,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c035-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c035-118">Requirements</span></span>



| <span data-ttu-id="4c035-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c035-119">Requirement</span></span> | <span data-ttu-id="4c035-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c035-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c035-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c035-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4c035-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c035-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4c035-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c035-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4c035-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c035-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4c035-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c035-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c035-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c035-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c035-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c035-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c035-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c035-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4c035-129">Fonctionnalités de la source réseau</span><span class="sxs-lookup"><span data-stu-id="4c035-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="4c035-130">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c035-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




