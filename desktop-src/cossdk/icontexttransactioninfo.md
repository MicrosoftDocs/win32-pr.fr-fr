---
description: Fournit l’accès aux propriétés de l’objet de contexte qui sont liées aux transactions.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Interface IContextTransactionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483440"
---
# <a name="icontexttransactioninfo-interface"></a><span data-ttu-id="f2439-103">Interface IContextTransactionInfo</span><span class="sxs-lookup"><span data-stu-id="f2439-103">IContextTransactionInfo interface</span></span>

<span data-ttu-id="f2439-104">Fournit l’accès aux propriétés de l’objet de contexte qui sont liées aux transactions.</span><span class="sxs-lookup"><span data-stu-id="f2439-104">Provides access to context object properties that relate to transactions.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="f2439-105">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="f2439-105">When to implement</span></span>

<span data-ttu-id="f2439-106">Vous ne devez pas implémenter cette interface.</span><span class="sxs-lookup"><span data-stu-id="f2439-106">You should not implement this interface.</span></span> <span data-ttu-id="f2439-107">L’implémentation standard fournit des fonctionnalités complètes.</span><span class="sxs-lookup"><span data-stu-id="f2439-107">The standard implementation provides complete functionality.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f2439-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="f2439-108">When to use</span></span>

<span data-ttu-id="f2439-109">Utilisez cette interface pour accéder aux propriétés de l’objet de contexte qui sont liées aux transactions.</span><span class="sxs-lookup"><span data-stu-id="f2439-109">Use this interface to access context object properties that relate to transactions.</span></span>

## <a name="members"></a><span data-ttu-id="f2439-110">Membres</span><span class="sxs-lookup"><span data-stu-id="f2439-110">Members</span></span>

<span data-ttu-id="f2439-111">L’interface **IContextTransactionInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f2439-111">The **IContextTransactionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f2439-112">**IContextTransactionInfo** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f2439-112">**IContextTransactionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="f2439-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f2439-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f2439-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f2439-114">Methods</span></span>

<span data-ttu-id="f2439-115">L’interface **IContextTransactionInfo** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f2439-115">The **IContextTransactionInfo** interface has these methods.</span></span>



| <span data-ttu-id="f2439-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="f2439-116">Method</span></span>                                                                                         | <span data-ttu-id="f2439-117">Description</span><span class="sxs-lookup"><span data-stu-id="f2439-117">Description</span></span>                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2439-118">**FetchTransaction**</span><span class="sxs-lookup"><span data-stu-id="f2439-118">**FetchTransaction**</span></span>](icontexttransactioninfo-registertransactionproxy.md)                   | <span data-ttu-id="f2439-119">Récupère la transaction ou le proxy de transaction associé au contexte actuel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f2439-119">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span><br/>              |
| [<span data-ttu-id="f2439-120">**GetTxIsolationLevelAndTimeout**</span><span class="sxs-lookup"><span data-stu-id="f2439-120">**GetTxIsolationLevelAndTimeout**</span></span>](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | <span data-ttu-id="f2439-121">Récupère le niveau d’isolation et la valeur de délai d’attente d’une transaction qui est hébergée dans le contexte de transaction racine.</span><span class="sxs-lookup"><span data-stu-id="f2439-121">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span><br/> |
| [<span data-ttu-id="f2439-122">**RegisterTransactionProxy**</span><span class="sxs-lookup"><span data-stu-id="f2439-122">**RegisterTransactionProxy**</span></span>](icontexttransactioninfo-fetchtransaction.md)                   | <span data-ttu-id="f2439-123">Associe une implémentation de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) avec le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="f2439-123">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="f2439-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2439-124">Requirements</span></span>



| <span data-ttu-id="f2439-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2439-125">Requirement</span></span> | <span data-ttu-id="f2439-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2439-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f2439-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2439-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f2439-128">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2439-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f2439-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2439-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f2439-130">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2439-130">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



 

