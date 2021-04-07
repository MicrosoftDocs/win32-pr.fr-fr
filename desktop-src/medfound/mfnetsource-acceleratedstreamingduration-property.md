---
description: Durée de la diffusion en continu accélérée pour la source réseau, en millisecondes.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: MFNETSOURCE_ACCELERATEDSTREAMINGDURATION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863166"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a><span data-ttu-id="363ec-103">MFNETSOURCE \_ propriété ACCELERATEDSTREAMINGDURATION</span><span class="sxs-lookup"><span data-stu-id="363ec-103">MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="363ec-104">Durée de la diffusion en continu accélérée pour la source réseau, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="363ec-104">Duration of accelerated streaming for the network source, in milliseconds.</span></span>



<span data-ttu-id="363ec-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="363ec-105">Data type</span></span>

<span data-ttu-id="363ec-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="363ec-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="363ec-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="363ec-107">PROPVARIANT member</span></span>

<span data-ttu-id="363ec-108">**DWORD** (stocké en tant que **long**)</span><span class="sxs-lookup"><span data-stu-id="363ec-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="363ec-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="363ec-109">VT\_I4</span></span>

<span data-ttu-id="363ec-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="363ec-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="363ec-111">Notes</span><span class="sxs-lookup"><span data-stu-id="363ec-111">Remarks</span></span>

<span data-ttu-id="363ec-112">La constante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="363ec-112">The constant **MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="363ec-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="363ec-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="363ec-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="363ec-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="363ec-115">Pour définir la propriété, transmettez un objet **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="363ec-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="363ec-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="363ec-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="363ec-117">Cette propriété s’applique à la fonctionnalité de démarrage rapide de Windows Media Services, qui lit rapidement le contenu sans attendre une longue mise en mémoire tampon initiale.</span><span class="sxs-lookup"><span data-stu-id="363ec-117">This property applies to the Fast Start feature of Windows Media Services, which plays content quickly without waiting for lengthy initial buffering.</span></span> <span data-ttu-id="363ec-118">Lorsque vous utilisez le démarrage rapide, le serveur exécutant Windows Media Services enverra des données au début du contenu à un rythme plus rapide que celui spécifié par la vitesse de transmission du contenu.</span><span class="sxs-lookup"><span data-stu-id="363ec-118">When using Fast Start, the server running Windows Media Services will send some data at the beginning of the content at a faster rate than that specified by the bit rate of the content.</span></span>

<span data-ttu-id="363ec-119">La valeur par défaut de cette propriété est 10 000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="363ec-119">The default value of this property is 10,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="363ec-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="363ec-120">Requirements</span></span>



| <span data-ttu-id="363ec-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="363ec-121">Requirement</span></span> | <span data-ttu-id="363ec-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="363ec-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="363ec-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="363ec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="363ec-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="363ec-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="363ec-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="363ec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="363ec-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="363ec-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="363ec-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="363ec-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="363ec-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="363ec-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="363ec-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="363ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363ec-130">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="363ec-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="363ec-131">Fonctionnalités de la source réseau</span><span class="sxs-lookup"><span data-stu-id="363ec-131">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="363ec-132">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="363ec-132">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




