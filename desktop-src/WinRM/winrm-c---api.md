---
title: API WinRM C++
description: Les interfaces Windows Remote Management peuvent être utilisées pour obtenir des données ou gérer des ressources sur un ordinateur distant. Cette API est principalement destinée à un usage interne. Nous vous recommandons d’utiliser à la place l’API du shell client WinRM dans la mesure du possible.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940122"
---
# <a name="winrm-c-api"></a><span data-ttu-id="78ebf-105">API WinRM C++</span><span class="sxs-lookup"><span data-stu-id="78ebf-105">WinRM C++ API</span></span>

<span data-ttu-id="78ebf-106">Les interfaces Windows Remote Management peuvent être utilisées pour obtenir des données ou gérer des [*ressources*](windows-remote-management-glossary.md) sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="78ebf-106">The Windows Remote Management interfaces can be used to obtain data or manage [*resources*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="78ebf-107">Cette API est principalement destinée à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="78ebf-107">This API is intended primarily for internal use.</span></span> <span data-ttu-id="78ebf-108">Nous vous recommandons d’utiliser à la place l' [API du shell client WinRM](client-shell-api.md) dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="78ebf-108">We recommend using the [WinRM Client Shell API](client-shell-api.md) instead whenever possible.</span></span> <span data-ttu-id="78ebf-109">Les interfaces correspondent étroitement à l' [API de script WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="78ebf-109">The interfaces closely correspond to the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="78ebf-110">Les interfaces WinRM qui héritent directement de **IDispatch** ont chacune un objet de script correspondant.</span><span class="sxs-lookup"><span data-stu-id="78ebf-110">The WinRM interfaces that inherit directly from **IDispatch** each have a corresponding scripting object.</span></span> <span data-ttu-id="78ebf-111">Pour plus d’informations, consultez l' [API de script WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="78ebf-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="78ebf-112">Pour les applications multithread, WinRM ne prend pas en charge les threads distincts qui accèdent au même objet [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) .</span><span class="sxs-lookup"><span data-stu-id="78ebf-112">For multithreaded applications, WinRM does not support separate threads accessing the same [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) object.</span></span>

<span data-ttu-id="78ebf-113">Les interfaces suivantes sont fournies par WinRM.</span><span class="sxs-lookup"><span data-stu-id="78ebf-113">The following interfaces are provided by WinRM.</span></span>

<dl> <dt>

<span data-ttu-id="78ebf-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="78ebf-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="78ebf-115">Fournit des méthodes et des propriétés utilisées pour créer une nouvelle session et gérer une session établie.</span><span class="sxs-lookup"><span data-stu-id="78ebf-115">Provides methods and properties used to create a new session and manage an established session.</span></span> <span data-ttu-id="78ebf-116">[**WSMan**](wsman.md) est l’objet de script correspondant.</span><span class="sxs-lookup"><span data-stu-id="78ebf-116">[**WSMan**](wsman.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="78ebf-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="78ebf-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="78ebf-118">Fournit des méthodes et des propriétés utilisées pour créer un [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="78ebf-118">Provides methods and properties used to create a new [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span> <span data-ttu-id="78ebf-119">Cette méthode est disponible pour l’objet de script [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="78ebf-119">This method is available for the [**WSMan**](wsman.md) scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="78ebf-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span><span class="sxs-lookup"><span data-stu-id="78ebf-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span></span>
</dt> <dd>

<span data-ttu-id="78ebf-121">Définit le nom d’utilisateur et le mot de passe utilisés pour les connexions à distance.</span><span class="sxs-lookup"><span data-stu-id="78ebf-121">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="78ebf-122">[**ConnectionOptions**](connectionoptions.md) est l’objet de script correspondant.</span><span class="sxs-lookup"><span data-stu-id="78ebf-122">[**ConnectionOptions**](connectionoptions.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="78ebf-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="78ebf-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span></span>
</dt> <dd>

<span data-ttu-id="78ebf-124">Définit les opérations réseau et les propriétés disponibles pour la session.</span><span class="sxs-lookup"><span data-stu-id="78ebf-124">Defines the network operations and properties available for the session.</span></span> <span data-ttu-id="78ebf-125">La [**session**](session.md) est l’objet de script correspondant.</span><span class="sxs-lookup"><span data-stu-id="78ebf-125">[**Session**](session.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="78ebf-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span><span class="sxs-lookup"><span data-stu-id="78ebf-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span></span>
</dt> <dd>

<span data-ttu-id="78ebf-127">Représente une collection de résultats retournés par l’énumération d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="78ebf-127">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="78ebf-128">L' [**énumérateur**](enumerator.md) est l’objet de script correspondant.</span><span class="sxs-lookup"><span data-stu-id="78ebf-128">[**Enumerator**](enumerator.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="78ebf-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="78ebf-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span></span>
</dt> <dd>

<span data-ttu-id="78ebf-130">Fournit le chemin d’accès à une ressource.</span><span class="sxs-lookup"><span data-stu-id="78ebf-130">Supplies the path to a resource.</span></span> <span data-ttu-id="78ebf-131">Vous pouvez utiliser un objet [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) à la place d’un [*URI de ressource*](windows-remote-management-glossary.md) dans les opérations d’objet de [**session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="78ebf-131">You can use an [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="78ebf-132">[**ResourceLocator**](resourcelocator.md) est l’objet de script correspondant.</span><span class="sxs-lookup"><span data-stu-id="78ebf-132">[**ResourceLocator**](resourcelocator.md) is the corresponding scripting object.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="78ebf-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78ebf-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ebf-134">Référence Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="78ebf-134">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




