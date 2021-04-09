---
description: Définit la configuration du flux pour la source du média WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: MFPKEY_SBESourceMode, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951660"
---
# <a name="mfpkey_sbesourcemode-property"></a><span data-ttu-id="e2df3-103">MFPKEY \_ propriété SBESourceMode</span><span class="sxs-lookup"><span data-stu-id="e2df3-103">MFPKEY\_SBESourceMode property</span></span>

<span data-ttu-id="e2df3-104">Définit la configuration du flux pour la source du média WTV.</span><span class="sxs-lookup"><span data-stu-id="e2df3-104">Sets the stream configuration for the WTV media source.</span></span>



<span data-ttu-id="e2df3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e2df3-105">Data type</span></span>

<span data-ttu-id="e2df3-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e2df3-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e2df3-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e2df3-107">PROPVARIANT member</span></span>

<span data-ttu-id="e2df3-108">**INT**</span><span class="sxs-lookup"><span data-stu-id="e2df3-108">**INT**</span></span>

<span data-ttu-id="e2df3-109">VT \_ int</span><span class="sxs-lookup"><span data-stu-id="e2df3-109">VT\_INT</span></span>

<span data-ttu-id="e2df3-110">**intVal**</span><span class="sxs-lookup"><span data-stu-id="e2df3-110">**intVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e2df3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e2df3-111">Remarks</span></span>

<span data-ttu-id="e2df3-112">Utilisez cette propriété pour configurer la source du média WTV.</span><span class="sxs-lookup"><span data-stu-id="e2df3-112">Use this property to configure the WTV media source.</span></span> <span data-ttu-id="e2df3-113">Pour définir la propriété, transmettez un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="e2df3-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="e2df3-114">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e2df3-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="e2df3-115">La source du média WTV lit les fichiers de l’émission TV enregistrée (. wtv et. ms-DRV) Windows.</span><span class="sxs-lookup"><span data-stu-id="e2df3-115">The WTV media source reads Windows Recorded TV Show (.wtv and .ms-drv) files.</span></span>

<span data-ttu-id="e2df3-116">Cette propriété doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e2df3-116">This property must have one of the following values.</span></span>

-   <span data-ttu-id="e2df3-117">1 : mapper les flux audio disponibles à une sortie unique, en fonction de la valeur système locale.</span><span class="sxs-lookup"><span data-stu-id="e2df3-117">1: Map available audio streams to a single output, based on the system local.</span></span> <span data-ttu-id="e2df3-118">Ce mode est approprié pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="e2df3-118">This mode is appropriate for playback.</span></span> <span data-ttu-id="e2df3-119">(valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="e2df3-119">(Default.)</span></span>
-   2. <span data-ttu-id="e2df3-120">Tous les flux et sous-flux audio (tels que les flux de données et de légende) sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="e2df3-120">All audio streams and substreams (such as caption and data streams) are selected.</span></span> <span data-ttu-id="e2df3-121">Ce mode est approprié pour le remuxing ou le transcodage.</span><span class="sxs-lookup"><span data-stu-id="e2df3-121">This mode is appropriate for remuxing or transcoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2df3-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2df3-122">Requirements</span></span>



| <span data-ttu-id="e2df3-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2df3-123">Requirement</span></span> | <span data-ttu-id="e2df3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2df3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2df3-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2df3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e2df3-126">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e2df3-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e2df3-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2df3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e2df3-128">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="e2df3-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e2df3-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2df3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2df3-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2df3-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2df3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2df3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2df3-132">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2df3-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
