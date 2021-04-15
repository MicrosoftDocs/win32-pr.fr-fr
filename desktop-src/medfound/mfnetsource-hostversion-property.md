---
description: Valeur de la &\# 0034 ; c-hostexever&\# 0034 ; le champ que la source réseau utilise pour la journalisation.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: MFNETSOURCE_HOSTVERSION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485201"
---
# <a name="mfnetsource_hostversion-property"></a><span data-ttu-id="2cdfc-103">MFNETSOURCE \_ propriété HOSTVERSION</span><span class="sxs-lookup"><span data-stu-id="2cdfc-103">MFNETSOURCE\_HOSTVERSION property</span></span>

<span data-ttu-id="2cdfc-104">Valeur du champ « c-hostexever » que la source réseau utilise pour la journalisation.</span><span class="sxs-lookup"><span data-stu-id="2cdfc-104">The value of the "c-hostexever" field that the network source uses for logging.</span></span> <span data-ttu-id="2cdfc-105">Les applications peuvent affecter à cette propriété le numéro de version de l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="2cdfc-105">Applications can set this property to the version number of the host application.</span></span> <span data-ttu-id="2cdfc-106">L’application hôte est le fichier. exe identifié par le champ c-hostexe.</span><span class="sxs-lookup"><span data-stu-id="2cdfc-106">The host application is the .exe file identified by the c-hostexe field.</span></span>



<span data-ttu-id="2cdfc-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="2cdfc-107">Data type</span></span>

<span data-ttu-id="2cdfc-108">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="2cdfc-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2cdfc-109">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="2cdfc-109">PROPVARIANT member</span></span>

<span data-ttu-id="2cdfc-110">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="2cdfc-110">**LONGLONG**</span></span>

<span data-ttu-id="2cdfc-111">Le \_ i8 VT</span><span class="sxs-lookup"><span data-stu-id="2cdfc-111">VT\_I8</span></span>

<span data-ttu-id="2cdfc-112">**hVal**</span><span class="sxs-lookup"><span data-stu-id="2cdfc-112">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2cdfc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2cdfc-113">Remarks</span></span>

<span data-ttu-id="2cdfc-114">La constante **MFNETSOURCE \_ HOSTVERSION** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="2cdfc-114">The constant **MFNETSOURCE\_HOSTVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="2cdfc-115">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2cdfc-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="2cdfc-116">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="2cdfc-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="2cdfc-117">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="2cdfc-117">To set the property, pass an **IPropertyStore** pointer to the Source resolver.</span></span> <span data-ttu-id="2cdfc-118">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2cdfc-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cdfc-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cdfc-119">Requirements</span></span>



| <span data-ttu-id="2cdfc-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cdfc-120">Requirement</span></span> | <span data-ttu-id="2cdfc-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cdfc-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2cdfc-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cdfc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2cdfc-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cdfc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2cdfc-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cdfc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2cdfc-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cdfc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2cdfc-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2cdfc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cdfc-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cdfc-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cdfc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cdfc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cdfc-129">Journalisation du client</span><span class="sxs-lookup"><span data-stu-id="2cdfc-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="2cdfc-130">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2cdfc-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2cdfc-131">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2cdfc-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




