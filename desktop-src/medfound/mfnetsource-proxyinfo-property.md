---
description: Stocke le nom d’hôte et le port du serveur proxy utilisé par la source réseau.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: MFNETSOURCE_PROXYINFO, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528190"
---
# <a name="mfnetsource_proxyinfo-property"></a><span data-ttu-id="f4679-103">MFNETSOURCE \_ propriété PROXYINFO</span><span class="sxs-lookup"><span data-stu-id="f4679-103">MFNETSOURCE\_PROXYINFO property</span></span>

<span data-ttu-id="f4679-104">Stocke le nom d’hôte et le port du serveur proxy utilisé par la source réseau.</span><span class="sxs-lookup"><span data-stu-id="f4679-104">Stores the host name and the port of the proxy server used by the network source.</span></span>



<span data-ttu-id="f4679-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f4679-105">Data type</span></span>

<span data-ttu-id="f4679-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f4679-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f4679-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f4679-107">PROPVARIANT member</span></span>

<span data-ttu-id="f4679-108">Chaîne de caractères larges (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="f4679-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="f4679-109">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="f4679-109">VT\_LPWSTR</span></span>

<span data-ttu-id="f4679-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="f4679-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f4679-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f4679-111">Remarks</span></span>

<span data-ttu-id="f4679-112">La constante **MFNETSOURCE \_ PROXYINFO** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="f4679-112">The constant **MFNETSOURCE\_PROXYINFO** defines the GUID for this property key.</span></span> <span data-ttu-id="f4679-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f4679-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="f4679-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f4679-114">This property is read-only.</span></span> <span data-ttu-id="f4679-115">Pour récupérer la valeur de la propriété à partir de la source réseau, appelez **IPropertyStore :: GetValue** et transmettez la structure **PROPERTYKEY** dans le paramètre *Key* .</span><span class="sxs-lookup"><span data-stu-id="f4679-115">To get the property value from the network source, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="f4679-116">Le membre **fmtid** de **PROPERTYKEY** doit avoir la valeur GUID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="f4679-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4679-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4679-117">Requirements</span></span>



| <span data-ttu-id="f4679-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4679-118">Requirement</span></span> | <span data-ttu-id="f4679-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4679-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4679-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4679-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f4679-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4679-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f4679-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4679-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f4679-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4679-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f4679-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4679-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4679-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4679-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4679-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4679-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4679-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4679-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f4679-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4679-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f4679-129">Prise en charge du proxy pour les sources réseau</span><span class="sxs-lookup"><span data-stu-id="f4679-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




