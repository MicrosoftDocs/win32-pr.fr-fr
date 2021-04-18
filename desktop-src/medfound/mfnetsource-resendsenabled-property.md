---
description: Spécifie si la source réseau envoie des demandes de renvoi UDP en réponse à des paquets perdus.
ms.assetid: 7956536d-9f3d-4875-8006-17e2cd577b61
title: MFNETSOURCE_RESENDSENABLED, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2646a9ef3e23fbcc9b3dff205f87d268115177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519805"
---
# <a name="mfnetsource_resendsenabled-property"></a><span data-ttu-id="5090b-103">MFNETSOURCE \_ propriété RESENDSENABLED</span><span class="sxs-lookup"><span data-stu-id="5090b-103">MFNETSOURCE\_RESENDSENABLED property</span></span>

<span data-ttu-id="5090b-104">Spécifie si la source réseau envoie des demandes de renvoi UDP en réponse à des paquets perdus.</span><span class="sxs-lookup"><span data-stu-id="5090b-104">Specifies whether the network source sends UDP resend requests in response to lost packets.</span></span>



<span data-ttu-id="5090b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5090b-105">Data type</span></span>

<span data-ttu-id="5090b-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="5090b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5090b-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="5090b-107">PROPVARIANT member</span></span>

<span data-ttu-id="5090b-108">Boolean (**long**)</span><span class="sxs-lookup"><span data-stu-id="5090b-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="5090b-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="5090b-109">VT\_I4</span></span>

<span data-ttu-id="5090b-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="5090b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="5090b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5090b-111">Remarks</span></span>

<span data-ttu-id="5090b-112">La constante **MFNETSOURCE \_ RESENDSENABLED** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="5090b-112">The constant **MFNETSOURCE\_RESENDSENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="5090b-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5090b-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="5090b-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="5090b-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="5090b-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="5090b-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="5090b-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5090b-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="5090b-117">La valeur par défaut de cette propriété est **true**.</span><span class="sxs-lookup"><span data-stu-id="5090b-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5090b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5090b-118">Requirements</span></span>



| <span data-ttu-id="5090b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5090b-119">Requirement</span></span> | <span data-ttu-id="5090b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5090b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5090b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5090b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5090b-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5090b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5090b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5090b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5090b-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5090b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5090b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5090b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5090b-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5090b-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5090b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5090b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5090b-128">Journalisation du client</span><span class="sxs-lookup"><span data-stu-id="5090b-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="5090b-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5090b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5090b-130">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5090b-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




