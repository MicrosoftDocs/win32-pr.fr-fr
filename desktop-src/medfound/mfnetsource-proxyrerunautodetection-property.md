---
description: Spécifie si le localisateur de proxy par défaut doit forcer la détection automatique de proxy.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: MFNETSOURCE_PROXYRERUNAUTODETECTION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37021c7e96b135389f0dffa2f8c26b8067df2b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528227"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a><span data-ttu-id="e0219-103">MFNETSOURCE \_ propriété PROXYRERUNAUTODETECTION</span><span class="sxs-lookup"><span data-stu-id="e0219-103">MFNETSOURCE\_PROXYRERUNAUTODETECTION property</span></span>

<span data-ttu-id="e0219-104">Spécifie si le localisateur de proxy par défaut doit forcer la détection automatique de proxy.</span><span class="sxs-lookup"><span data-stu-id="e0219-104">Specifies whether the default proxy locator should force proxy auto-detection.</span></span>



<span data-ttu-id="e0219-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e0219-105">Data type</span></span>

<span data-ttu-id="e0219-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e0219-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e0219-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e0219-107">PROPVARIANT member</span></span>

<span data-ttu-id="e0219-108">Boolean (**long**)</span><span class="sxs-lookup"><span data-stu-id="e0219-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="e0219-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="e0219-109">VT\_I4</span></span>

<span data-ttu-id="e0219-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="e0219-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e0219-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e0219-111">Remarks</span></span>

<span data-ttu-id="e0219-112">La constante **MFNETSOURCE \_ PROXYSETTINGS** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="e0219-112">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="e0219-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e0219-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e0219-114">Les applications peuvent utiliser cette propriété pour configurer le localisateur de proxy lors de la création de l’objet localisateur de proxy.</span><span class="sxs-lookup"><span data-stu-id="e0219-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="e0219-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** dans le paramètre *pProxyConfig* de la fonction [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="e0219-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="e0219-116">En mode de détection automatique, le localisateur de proxy utilise le mécanisme de détection de proxy WinInet.</span><span class="sxs-lookup"><span data-stu-id="e0219-116">In auto-detect mode, the proxy locator uses the WinInet proxy detection mechanism.</span></span> <span data-ttu-id="e0219-117">Pour forcer la détection automatique, définissez la valeur sur 0.</span><span class="sxs-lookup"><span data-stu-id="e0219-117">To force auto-detection, set the value to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0219-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0219-118">Requirements</span></span>



| <span data-ttu-id="e0219-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0219-119">Requirement</span></span> | <span data-ttu-id="e0219-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0219-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0219-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0219-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e0219-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0219-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e0219-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0219-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e0219-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0219-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0219-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0219-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0219-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0219-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0219-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0219-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0219-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0219-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e0219-129">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0219-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="e0219-130">Prise en charge du proxy pour les sources réseau</span><span class="sxs-lookup"><span data-stu-id="e0219-130">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




