---
description: Spécifie le nom d’hôte du serveur proxy.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: MFNETSOURCE_PROXYHOSTNAME, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc59d5b827276eb5063febf7a8cb7647002ca72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533749"
---
# <a name="mfnetsource_proxyhostname-property"></a><span data-ttu-id="26130-103">MFNETSOURCE \_ propriété PROXYHOSTNAME</span><span class="sxs-lookup"><span data-stu-id="26130-103">MFNETSOURCE\_PROXYHOSTNAME property</span></span>

<span data-ttu-id="26130-104">Spécifie le nom d’hôte du serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="26130-104">Specifies the host name of the proxy server.</span></span>



<span data-ttu-id="26130-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="26130-105">Data type</span></span>

<span data-ttu-id="26130-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="26130-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="26130-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="26130-107">PROPVARIANT member</span></span>

<span data-ttu-id="26130-108">Chaîne de caractères larges (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="26130-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="26130-109">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="26130-109">VT\_LPWSTR</span></span>

<span data-ttu-id="26130-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="26130-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="26130-111">Notes</span><span class="sxs-lookup"><span data-stu-id="26130-111">Remarks</span></span>

<span data-ttu-id="26130-112">La constante **MFNETSOURCE \_ PROXYHOSTNAME** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="26130-112">The constant **MFNETSOURCE\_PROXYHOSTNAME** defines the GUID for this property key.</span></span> <span data-ttu-id="26130-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="26130-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="26130-114">Les applications peuvent utiliser cette propriété pour configurer le localisateur de proxy par défaut lors de la création de l’objet localisateur de proxy.</span><span class="sxs-lookup"><span data-stu-id="26130-114">Applications can use this property to configure the default proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="26130-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** dans le paramètre *pProxyConfig* de la fonction [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="26130-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="26130-116">Cette propriété doit être définie par l’application lorsque le localisateur de proxy est configuré pour fonctionner en mode manuel.</span><span class="sxs-lookup"><span data-stu-id="26130-116">This property must be set by the application when the proxy locator is configured to operate in the manual mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="26130-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26130-117">Requirements</span></span>



| <span data-ttu-id="26130-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26130-118">Requirement</span></span> | <span data-ttu-id="26130-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="26130-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26130-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26130-120">Minimum supported client</span></span><br/> | <span data-ttu-id="26130-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26130-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="26130-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26130-122">Minimum supported server</span></span><br/> | <span data-ttu-id="26130-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26130-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="26130-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="26130-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="26130-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26130-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26130-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26130-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26130-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26130-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="26130-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26130-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="26130-129">Prise en charge du proxy pour les sources réseau</span><span class="sxs-lookup"><span data-stu-id="26130-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




