---
description: Spécifie si le localisateur de proxy doit utiliser un serveur proxy pour les adresses locales.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: MFNETSOURCE_PROXYBYPASSFORLOCAL, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749196"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a><span data-ttu-id="0f2c9-103">MFNETSOURCE \_ propriété PROXYBYPASSFORLOCAL</span><span class="sxs-lookup"><span data-stu-id="0f2c9-103">MFNETSOURCE\_PROXYBYPASSFORLOCAL property</span></span>

<span data-ttu-id="0f2c9-104">Spécifie si le localisateur de proxy doit utiliser un serveur proxy pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="0f2c9-104">Specifies whether the proxy locator should use a proxy server for local addresses.</span></span>



<span data-ttu-id="0f2c9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0f2c9-105">Data type</span></span>

<span data-ttu-id="0f2c9-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="0f2c9-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="0f2c9-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="0f2c9-107">PROPVARIANT member</span></span>

<span data-ttu-id="0f2c9-108">Boolean (**long**)</span><span class="sxs-lookup"><span data-stu-id="0f2c9-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="0f2c9-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="0f2c9-109">VT\_I4</span></span>

<span data-ttu-id="0f2c9-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="0f2c9-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="0f2c9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0f2c9-111">Remarks</span></span>

<span data-ttu-id="0f2c9-112">La constante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="0f2c9-112">The constant **MFNETSOURCE\_PROXYBYPASSFORLOCAL** defines the GUID for this property key.</span></span> <span data-ttu-id="0f2c9-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0f2c9-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="0f2c9-114">Les applications peuvent utiliser cette propriété pour configurer le localisateur de proxy lors de la création de l’objet localisateur de proxy.</span><span class="sxs-lookup"><span data-stu-id="0f2c9-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="0f2c9-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** dans le paramètre *pProxyConfig* de la fonction [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="0f2c9-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="0f2c9-116">La valeur doit être égale à 0 si le serveur proxy doit être utilisé pour les adresses locales. Sinon, une valeur différente de zéro configure le localisateur de proxy par défaut pour ignorer le serveur proxy pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="0f2c9-116">The value must be set to 0 if the proxy server is to be used for local addresses; otherwise a nonzero value configures the default proxy locator to skip the proxy server for local addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f2c9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f2c9-117">Requirements</span></span>



| <span data-ttu-id="0f2c9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f2c9-118">Requirement</span></span> | <span data-ttu-id="0f2c9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f2c9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f2c9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f2c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0f2c9-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f2c9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0f2c9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f2c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0f2c9-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f2c9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0f2c9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f2c9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f2c9-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f2c9-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f2c9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f2c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f2c9-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f2c9-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0f2c9-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f2c9-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="0f2c9-129">Prise en charge du proxy pour les sources réseau</span><span class="sxs-lookup"><span data-stu-id="0f2c9-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




