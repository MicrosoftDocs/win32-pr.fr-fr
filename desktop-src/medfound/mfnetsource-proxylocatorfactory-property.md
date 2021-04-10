---
description: Contient un pointeur vers l’interface IMFNetProxyLocatorFactory.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: MFNETSOURCE_PROXYLOCATORFACTORY, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1199333e9eb343ab9d8f96864372b2dc385ab7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114595"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a><span data-ttu-id="5579a-103">MFNETSOURCE \_ propriété PROXYLOCATORFACTORY</span><span class="sxs-lookup"><span data-stu-id="5579a-103">MFNETSOURCE\_PROXYLOCATORFACTORY property</span></span>

<span data-ttu-id="5579a-104">Contient un pointeur vers l’interface [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="5579a-104">Contains a pointer to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>



<span data-ttu-id="5579a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5579a-105">Data type</span></span>

<span data-ttu-id="5579a-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="5579a-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5579a-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="5579a-107">PROPVARIANT member</span></span>

<span data-ttu-id="5579a-108">**IUnknown** , pointeur</span><span class="sxs-lookup"><span data-stu-id="5579a-108">**IUnknown** pointer</span></span>

<span data-ttu-id="5579a-109">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="5579a-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="5579a-110">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="5579a-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="5579a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5579a-111">Remarks</span></span>

<span data-ttu-id="5579a-112">La constante **MFNETSOURCE \_ PROXYLOCATORFACTORY** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="5579a-112">The constant **MFNETSOURCE\_PROXYLOCATORFACTORY** defines the GUID for this property key.</span></span> <span data-ttu-id="5579a-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5579a-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="5579a-114">Les applications peuvent utiliser cette propriété pour fournir un localisateur de proxy personnalisé pour la source réseau.</span><span class="sxs-lookup"><span data-stu-id="5579a-114">Applications can use this property to provide a custom proxy locator for the network source.</span></span> <span data-ttu-id="5579a-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="5579a-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="5579a-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5579a-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5579a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5579a-117">Requirements</span></span>



| <span data-ttu-id="5579a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5579a-118">Requirement</span></span> | <span data-ttu-id="5579a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5579a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5579a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5579a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5579a-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5579a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5579a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5579a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5579a-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5579a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5579a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5579a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5579a-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5579a-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5579a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5579a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5579a-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5579a-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5579a-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5579a-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="5579a-129">Prise en charge du proxy pour les sources réseau</span><span class="sxs-lookup"><span data-stu-id="5579a-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




