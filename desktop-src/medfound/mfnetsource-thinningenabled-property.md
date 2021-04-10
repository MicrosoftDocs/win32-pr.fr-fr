---
description: Spécifie si le basculement de flux est activé sur la source réseau.
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: MFNETSOURCE_THINNINGENABLED, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d5b1b362f8776e80e3d12b591dbf2116217846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950895"
---
# <a name="mfnetsource_thinningenabled-property"></a><span data-ttu-id="e2abc-103">MFNETSOURCE \_ propriété THINNINGENABLED</span><span class="sxs-lookup"><span data-stu-id="e2abc-103">MFNETSOURCE\_THINNINGENABLED property</span></span>

<span data-ttu-id="e2abc-104">Spécifie si le basculement de flux est activé sur la source réseau.</span><span class="sxs-lookup"><span data-stu-id="e2abc-104">Specifies whether stream switching is enabled on the network source.</span></span> <span data-ttu-id="e2abc-105">Le basculement de flux permet au serveur multimédia de modifier les flux dans un fichier à débit binaire multiple (MBR), en fonction de la bande passante disponible.</span><span class="sxs-lookup"><span data-stu-id="e2abc-105">Stream switching enables the media server to change streams in a multiple bit-rate (MBR) file, based on available bandwidth.</span></span>



<span data-ttu-id="e2abc-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="e2abc-106">Data type</span></span>

<span data-ttu-id="e2abc-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e2abc-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e2abc-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e2abc-108">PROPVARIANT member</span></span>

<span data-ttu-id="e2abc-109">Boolean (**long**)</span><span class="sxs-lookup"><span data-stu-id="e2abc-109">Boolean (**LONG**)</span></span>

<span data-ttu-id="e2abc-110">VT \_</span><span class="sxs-lookup"><span data-stu-id="e2abc-110">VT\_I4</span></span>

<span data-ttu-id="e2abc-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="e2abc-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e2abc-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e2abc-112">Remarks</span></span>

<span data-ttu-id="e2abc-113">La constante **MFNETSOURCE \_ THINNINGENABLED** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="e2abc-113">The constant **MFNETSOURCE\_THINNINGENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="e2abc-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e2abc-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e2abc-115">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="e2abc-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="e2abc-116">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="e2abc-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="e2abc-117">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e2abc-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="e2abc-118">La valeur par défaut de cette propriété est **true**.</span><span class="sxs-lookup"><span data-stu-id="e2abc-118">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2abc-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2abc-119">Requirements</span></span>



| <span data-ttu-id="e2abc-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2abc-120">Requirement</span></span> | <span data-ttu-id="e2abc-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2abc-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2abc-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2abc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e2abc-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2abc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e2abc-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2abc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e2abc-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2abc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e2abc-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2abc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2abc-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2abc-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2abc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2abc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2abc-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2abc-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e2abc-130">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2abc-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




