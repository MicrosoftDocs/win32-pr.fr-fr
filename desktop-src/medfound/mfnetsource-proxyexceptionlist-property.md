---
description: Spécifie une liste délimitée par des points-virgules de serveurs multimédias qui peuvent accepter des connexions à partir d’applications clientes sans utiliser de serveur proxy.
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: MFNETSOURCE_PROXYEXCEPTIONLIST, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591f7036491964928937f2b48b0656e60f9a20f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527882"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a><span data-ttu-id="cb854-103">MFNETSOURCE \_ propriété PROXYEXCEPTIONLIST</span><span class="sxs-lookup"><span data-stu-id="cb854-103">MFNETSOURCE\_PROXYEXCEPTIONLIST property</span></span>

<span data-ttu-id="cb854-104">Spécifie une liste délimitée par des points-virgules de serveurs multimédias qui peuvent accepter des connexions à partir d’applications clientes sans utiliser de serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="cb854-104">Specifies a semicolon-delimited list of media servers that can accept connections from client applications without using a proxy server.</span></span>



<span data-ttu-id="cb854-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="cb854-105">Data type</span></span>

<span data-ttu-id="cb854-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="cb854-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="cb854-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="cb854-107">PROPVARIANT member</span></span>

<span data-ttu-id="cb854-108">Chaîne de caractères larges (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="cb854-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="cb854-109">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="cb854-109">VT\_LPWSTR</span></span>

<span data-ttu-id="cb854-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="cb854-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="cb854-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cb854-111">Remarks</span></span>

<span data-ttu-id="cb854-112">La constante **MFNETSOURCE \_ PROXYEXCEPTIONLIST** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="cb854-112">The constant **MFNETSOURCE\_PROXYEXCEPTIONLIST** defines the GUID for this property key.</span></span> <span data-ttu-id="cb854-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cb854-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="cb854-114">Les applications peuvent utiliser cette propriété pour configurer le localisateur de proxy lors de la création de l’objet localisateur de proxy.</span><span class="sxs-lookup"><span data-stu-id="cb854-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="cb854-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** dans le paramètre *pProxyConfig* de la fonction [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="cb854-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="cb854-116">Le localisateur de proxy n’effectue pas la détection du proxy pour ces adresses.</span><span class="sxs-lookup"><span data-stu-id="cb854-116">The proxy locator does not perform proxy detection for these addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb854-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb854-117">Requirements</span></span>



| <span data-ttu-id="cb854-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb854-118">Requirement</span></span> | <span data-ttu-id="cb854-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb854-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb854-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb854-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb854-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb854-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cb854-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb854-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb854-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb854-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cb854-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb854-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb854-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb854-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb854-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb854-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb854-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb854-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="cb854-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb854-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="cb854-129">Prise en charge du proxy pour les sources réseau</span><span class="sxs-lookup"><span data-stu-id="cb854-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




