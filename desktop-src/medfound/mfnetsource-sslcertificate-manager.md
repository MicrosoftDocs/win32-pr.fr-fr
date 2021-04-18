---
description: Stocke le pointeur IUnknown de la classe qui implémente l’interface IMFSSLCertificateManager.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: MFNETSOURCE_SSLCERTIFICATE_MANAGER, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516195"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a><span data-ttu-id="97959-103">\_Propriété MFNETSOURCE SSLCERTIFICATE \_ Manager</span><span class="sxs-lookup"><span data-stu-id="97959-103">MFNETSOURCE\_SSLCERTIFICATE\_MANAGER property</span></span>

<span data-ttu-id="97959-104">Stocke le pointeur **IUnknown** de la classe qui implémente l’interface [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) .</span><span class="sxs-lookup"><span data-stu-id="97959-104">Stores the **IUnknown** pointer of the class that implements the [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) interface.</span></span> <span data-ttu-id="97959-105">L’implémentation cliente fournit des méthodes pour récupérer le certificat SSL client lorsqu’il est demandé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="97959-105">The client implemention provides methods to get the client SSL certificate when it is requested by the server.</span></span>



<span data-ttu-id="97959-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="97959-106">Data type</span></span>

<span data-ttu-id="97959-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="97959-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="97959-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="97959-108">PROPVARIANT member</span></span>

<span data-ttu-id="97959-109">**IUnknown, pointeur**</span><span class="sxs-lookup"><span data-stu-id="97959-109">**IUnknown pointer**</span></span>

<span data-ttu-id="97959-110">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="97959-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="97959-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="97959-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="97959-112">Notes</span><span class="sxs-lookup"><span data-stu-id="97959-112">Remarks</span></span>

<span data-ttu-id="97959-113">La constante **MFNETSOURCE \_ SSLCERTIFICATE \_ Manager** définit le GUID de la clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="97959-113">The **MFNETSOURCE\_SSLCERTIFICATE\_MANAGER** constant defines the GUID for the property key.</span></span> <span data-ttu-id="97959-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="97959-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="97959-115">Pour définir cette propriété sur la source réseau, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="97959-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="97959-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="97959-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97959-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97959-117">Requirements</span></span>



| <span data-ttu-id="97959-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97959-118">Requirement</span></span> | <span data-ttu-id="97959-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="97959-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97959-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97959-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97959-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97959-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="97959-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97959-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97959-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97959-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="97959-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="97959-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="97959-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97959-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97959-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97959-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97959-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97959-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="97959-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97959-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




