---
title: Interface IConnectionBrokerClient (Cbclient. h)
description: Fournit les méthodes nécessaires pour utiliser le client Connexion Bureau à distance Broker.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IConnectionBrokerClient
- Services Bureau à distance de l’interface IConnectionBrokerClient, Description
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466758"
---
# <a name="iconnectionbrokerclient-interface"></a><span data-ttu-id="7a589-105">Interface IConnectionBrokerClient</span><span class="sxs-lookup"><span data-stu-id="7a589-105">IConnectionBrokerClient interface</span></span>

<span data-ttu-id="7a589-106">Fournit les méthodes nécessaires pour utiliser le client Connexion Bureau à distance Broker.</span><span class="sxs-lookup"><span data-stu-id="7a589-106">Provides the methods needed to use the Remote Desktop Connection Broker client.</span></span>

<span data-ttu-id="7a589-107">Cette interface est implémentée par le système.</span><span class="sxs-lookup"><span data-stu-id="7a589-107">This interface is implemented by the system.</span></span> <span data-ttu-id="7a589-108">Pour obtenir une instance de cette interface, utilisez la fonction [**CBCreateClientInstance**](cbcreateclientinstance.md) .</span><span class="sxs-lookup"><span data-stu-id="7a589-108">To obtain an instance of this interface, use the [**CBCreateClientInstance**](cbcreateclientinstance.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="7a589-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7a589-109">Members</span></span>

<span data-ttu-id="7a589-110">L’interface **IConnectionBrokerClient** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7a589-110">The **IConnectionBrokerClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7a589-111">**IConnectionBrokerClient** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7a589-111">**IConnectionBrokerClient** also has these types of members:</span></span>

-   [<span data-ttu-id="7a589-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7a589-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7a589-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7a589-113">Methods</span></span>

<span data-ttu-id="7a589-114">L’interface **IConnectionBrokerClient** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7a589-114">The **IConnectionBrokerClient** interface has these methods.</span></span>



| <span data-ttu-id="7a589-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="7a589-115">Method</span></span>                                                         | <span data-ttu-id="7a589-116">Description</span><span class="sxs-lookup"><span data-stu-id="7a589-116">Description</span></span>                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a589-117">**GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="7a589-117">**GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md) | <span data-ttu-id="7a589-118">Demande des informations sur l’ordinateur cible sur lequel la connexion doit être redirigée.</span><span class="sxs-lookup"><span data-stu-id="7a589-118">Requests information about the target computer where the connection should be redirected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7a589-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a589-119">Requirements</span></span>



| <span data-ttu-id="7a589-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a589-120">Requirement</span></span> | <span data-ttu-id="7a589-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a589-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a589-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a589-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7a589-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7a589-123">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="7a589-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a589-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7a589-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a589-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="7a589-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a589-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a589-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a589-127"><dt>Cbclient.h</dt></span></span> </dl>      |
| <span data-ttu-id="7a589-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a589-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a589-129"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a589-129"><dt>Cbclient.lib</dt></span></span> </dl>    |
| <span data-ttu-id="7a589-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7a589-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a589-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a589-131"><dt>Cbclient.dll</dt></span></span> </dl>    |
| <span data-ttu-id="7a589-132">IID</span><span class="sxs-lookup"><span data-stu-id="7a589-132">IID</span></span><br/>                      | <span data-ttu-id="7a589-133">IID \_ IConnectionBrokerClient est défini en tant que D6818DF2-8338-4EB7-AD77-DE210817987C</span><span class="sxs-lookup"><span data-stu-id="7a589-133">IID\_IConnectionBrokerClient is defined as D6818DF2-8338-4EB7-AD77-DE210817987C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a589-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a589-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a589-135">**CBCreateClientInstance**</span><span class="sxs-lookup"><span data-stu-id="7a589-135">**CBCreateClientInstance**</span></span>](cbcreateclientinstance.md)
</dt> </dl>

 

