---
description: Spécifie le numéro de port du serveur proxy.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: MFNETSOURCE_PROXYPORT, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228f7d9390d53f7d8182a198879dcb2d81e3bae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201972"
---
# <a name="mfnetsource_proxyport-property"></a><span data-ttu-id="6b7e2-103">MFNETSOURCE \_ propriété PROXYPORT</span><span class="sxs-lookup"><span data-stu-id="6b7e2-103">MFNETSOURCE\_PROXYPORT property</span></span>

<span data-ttu-id="6b7e2-104">Spécifie le numéro de port du serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="6b7e2-104">Specifies the port number of the proxy server.</span></span>



<span data-ttu-id="6b7e2-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="6b7e2-105">Data type</span></span>

<span data-ttu-id="6b7e2-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="6b7e2-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6b7e2-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="6b7e2-107">PROPVARIANT member</span></span>

<span data-ttu-id="6b7e2-108">**DWORD** (stocké en tant que **long**)</span><span class="sxs-lookup"><span data-stu-id="6b7e2-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="6b7e2-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="6b7e2-109">VT\_I4</span></span>

<span data-ttu-id="6b7e2-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="6b7e2-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="6b7e2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6b7e2-111">Remarks</span></span>

<span data-ttu-id="6b7e2-112">La constante **MFNETSOURCE \_ PROXYPORT** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="6b7e2-112">The constant **MFNETSOURCE\_PROXYPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="6b7e2-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6b7e2-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="6b7e2-114">Les applications peuvent utiliser cette propriété pour configurer le localisateur de proxy lors de la création de l’objet localisateur de proxy.</span><span class="sxs-lookup"><span data-stu-id="6b7e2-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="6b7e2-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** dans le paramètre *pProxyConfig* de la fonction [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="6b7e2-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="6b7e2-116">Si cette propriété n’est pas définie pour HTTP, le localisateur de proxy utilise par défaut la valeur 80.</span><span class="sxs-lookup"><span data-stu-id="6b7e2-116">If this property is not set for HTTP, then by default the proxy locator uses a value of 80.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b7e2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b7e2-117">Requirements</span></span>



| <span data-ttu-id="6b7e2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b7e2-118">Requirement</span></span> | <span data-ttu-id="6b7e2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b7e2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7e2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b7e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6b7e2-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b7e2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6b7e2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b7e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6b7e2-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b7e2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6b7e2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b7e2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b7e2-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b7e2-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b7e2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b7e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b7e2-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b7e2-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6b7e2-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b7e2-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6b7e2-129">Prise en charge du proxy pour les sources réseau</span><span class="sxs-lookup"><span data-stu-id="6b7e2-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




