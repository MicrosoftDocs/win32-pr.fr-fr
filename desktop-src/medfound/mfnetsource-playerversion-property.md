---
description: Valeur de la &\# 0034 ; c-playerversion&\# 0034 ; le champ que la source réseau utilise pour la journalisation.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: MFNETSOURCE_PLAYERVERSION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759669"
---
# <a name="mfnetsource_playerversion-property"></a><span data-ttu-id="414e8-103">MFNETSOURCE \_ propriété PLAYERVERSION</span><span class="sxs-lookup"><span data-stu-id="414e8-103">MFNETSOURCE\_PLAYERVERSION property</span></span>

<span data-ttu-id="414e8-104">Valeur du champ « c-playerversion » que la source réseau utilise pour la journalisation.</span><span class="sxs-lookup"><span data-stu-id="414e8-104">The value of the "c-playerversion" field that the network source uses for logging.</span></span> <span data-ttu-id="414e8-105">Les applications peuvent affecter à cette propriété le numéro de version de l’application.</span><span class="sxs-lookup"><span data-stu-id="414e8-105">Applications can set this property to the version number of the application.</span></span>



<span data-ttu-id="414e8-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="414e8-106">Data type</span></span>

<span data-ttu-id="414e8-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="414e8-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="414e8-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="414e8-108">PROPVARIANT member</span></span>

<span data-ttu-id="414e8-109">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="414e8-109">**LONGLONG**</span></span>

<span data-ttu-id="414e8-110">Le \_ i8 VT</span><span class="sxs-lookup"><span data-stu-id="414e8-110">VT\_I8</span></span>

<span data-ttu-id="414e8-111">**hVal**</span><span class="sxs-lookup"><span data-stu-id="414e8-111">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="414e8-112">Notes</span><span class="sxs-lookup"><span data-stu-id="414e8-112">Remarks</span></span>

<span data-ttu-id="414e8-113">La constante **MFNETSOURCE \_ PLAYERVERSION** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="414e8-113">The constant **MFNETSOURCE\_PLAYERVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="414e8-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="414e8-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="414e8-115">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="414e8-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="414e8-116">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="414e8-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="414e8-117">Pour plus d’informations, consultez la page programme de [résolution source](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="414e8-117">For more information, see [Source Resolver](source-resolver.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="414e8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="414e8-118">Requirements</span></span>



| <span data-ttu-id="414e8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="414e8-119">Requirement</span></span> | <span data-ttu-id="414e8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="414e8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="414e8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="414e8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="414e8-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="414e8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="414e8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="414e8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="414e8-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="414e8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="414e8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="414e8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="414e8-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="414e8-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="414e8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="414e8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414e8-128">Journalisation du client</span><span class="sxs-lookup"><span data-stu-id="414e8-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="414e8-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="414e8-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="414e8-130">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="414e8-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




