---
title: API de script WinRM
description: Les objets de script Windows Remote Management sont implémentés en tant que couche au-dessus du protocole WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510421"
---
# <a name="winrm-scripting-api"></a><span data-ttu-id="c02f4-103">API de script WinRM</span><span class="sxs-lookup"><span data-stu-id="c02f4-103">WinRM Scripting API</span></span>

<span data-ttu-id="c02f4-104">Les objets de script Windows Remote Management sont implémentés en tant que couche au-dessus du [protocole WS-Management](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="c02f4-104">Windows Remote Management scripting objects are implemented as a layer above the [WS-Management Protocol](ws-management-protocol.md).</span></span> <span data-ttu-id="c02f4-105">Les objets de script vous permettent d’obtenir des données ou de gérer des [*ressources*](windows-remote-management-glossary.md) sur des ordinateurs locaux et distants.</span><span class="sxs-lookup"><span data-stu-id="c02f4-105">The scripting objects enable you to obtain data or manage [*resources*](windows-remote-management-glossary.md) on local and remote computers.</span></span>

## <a name="ws-management-objects"></a><span data-ttu-id="c02f4-106">Objets WS-Management</span><span class="sxs-lookup"><span data-stu-id="c02f4-106">WS-Management Objects</span></span>

<span data-ttu-id="c02f4-107">Chaque objet de script a une interface C++ correspondante.</span><span class="sxs-lookup"><span data-stu-id="c02f4-107">Each scripting object has a corresponding C++ interface.</span></span> <span data-ttu-id="c02f4-108">Pour plus d’informations, consultez [API C++ WinRM](winrm-c---api.md) et [scripts dans Windows Remote Management](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="c02f4-108">For more information, see [WinRM C++ API](winrm-c---api.md) and [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="c02f4-109">Les objets suivants sont fournis par l’API de script WinRM.</span><span class="sxs-lookup"><span data-stu-id="c02f4-109">The following objects are provided by the WinRM Scripting API.</span></span>

<dl> <dt>

<span data-ttu-id="c02f4-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span><span class="sxs-lookup"><span data-stu-id="c02f4-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span></span>
</dt> <dd>

<span data-ttu-id="c02f4-111">Définit le nom d’utilisateur et le mot de passe utilisés pour les connexions à distance.</span><span class="sxs-lookup"><span data-stu-id="c02f4-111">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="c02f4-112">Le nom d’utilisateur et le mot de passe sont transmis lors de l’appel de la méthode [**CreateConnectionOptions**](wsman-createconnectionoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="c02f4-112">The user name and password are passed when calling the [**CreateConnectionOptions**](wsman-createconnectionoptions.md) method.</span></span> <span data-ttu-id="c02f4-113">Pour plus d’informations, consultez [obtention de données à partir d’un ordinateur distant](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="c02f4-113">For more information, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="c02f4-114">L’interface C++ correspondante est [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span><span class="sxs-lookup"><span data-stu-id="c02f4-114">The corresponding C++ interface is [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span></span>

</dd> <dt>

<span data-ttu-id="c02f4-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Énumérateur**](enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="c02f4-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerator**](enumerator.md)</span></span>
</dt> <dd>

<span data-ttu-id="c02f4-116">Représente une collection de résultats retournés par l’énumération d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="c02f4-116">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="c02f4-117">Pour plus d’informations, consultez [énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="c02f4-117">For more information, see [Enumerating or Listing All the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span> <span data-ttu-id="c02f4-118">L’interface C++ correspondante est [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="c02f4-118">The corresponding C++ interface is [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="c02f4-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span><span class="sxs-lookup"><span data-stu-id="c02f4-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span></span>
</dt> <dd>

<span data-ttu-id="c02f4-120">Fournit le chemin d’accès à une ressource.</span><span class="sxs-lookup"><span data-stu-id="c02f4-120">Supplies the path to a resource.</span></span> <span data-ttu-id="c02f4-121">Vous pouvez utiliser un objet [**ResourceLocator**](resourcelocator.md) à la place d’un [*URI de ressource*](windows-remote-management-glossary.md) dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="c02f4-121">You can use a [**ResourceLocator**](resourcelocator.md) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations, such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="c02f4-122">L’interface C++ correspondante est [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="c02f4-122">The corresponding C++ interface is [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span>

</dd> <dt>

<span data-ttu-id="c02f4-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Session**](session.md)</span><span class="sxs-lookup"><span data-stu-id="c02f4-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Session**](session.md)</span></span>
</dt> <dd>

<span data-ttu-id="c02f4-124">Définit les opérations réseau et les propriétés disponibles pour la session, telles que [**session. obtenir**](session-get.md), [**session. Enumerate**](session-enumerate.md), [**session. Invoke**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="c02f4-124">Defines the network operations and properties available for the session, such as [**Session.Get**](session-get.md), [**Session.Enumerate**](session-enumerate.md), [**Session.Invoke**](session-invoke.md).</span></span> <span data-ttu-id="c02f4-125">Pour plus d’informations, consultez [obtention de données à partir de l’ordinateur local](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="c02f4-125">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span> <span data-ttu-id="c02f4-126">L’interface C++ correspondante est [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span><span class="sxs-lookup"><span data-stu-id="c02f4-126">The corresponding C++ interface is [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span></span>

</dd> <dt>

<span data-ttu-id="c02f4-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span><span class="sxs-lookup"><span data-stu-id="c02f4-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span></span>
</dt> <dd>

<span data-ttu-id="c02f4-128">Fournit des méthodes et des propriétés utilisées pour créer une session ou gérer une session établie.</span><span class="sxs-lookup"><span data-stu-id="c02f4-128">Provides methods and properties used to create a new session or manage an established session.</span></span> <span data-ttu-id="c02f4-129">Pour plus d’informations, consultez [utilisation de Windows Remote Management](using-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="c02f4-129">For more information see, [Using Windows Remote Management](using-windows-remote-management.md).</span></span> <span data-ttu-id="c02f4-130">Les interfaces C++ correspondantes sont [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) et [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span><span class="sxs-lookup"><span data-stu-id="c02f4-130">The corresponding C++ interfaces are [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c02f4-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c02f4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c02f4-132">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="c02f4-132">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="c02f4-133">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="c02f4-133">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="c02f4-134">Scripts dans Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="c02f4-134">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="c02f4-135">Référence Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="c02f4-135">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




