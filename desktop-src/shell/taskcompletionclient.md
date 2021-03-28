---
description: Active l’achèvement des tâches.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Interface TaskCompletionClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209932"
---
# <a name="taskcompletionclient-interface"></a><span data-ttu-id="c6dca-103">Interface TaskCompletionClient</span><span class="sxs-lookup"><span data-stu-id="c6dca-103">TaskCompletionClient interface</span></span>

<span data-ttu-id="c6dca-104">Active l’achèvement des tâches.</span><span class="sxs-lookup"><span data-stu-id="c6dca-104">Enables task completion.</span></span>

## <a name="members"></a><span data-ttu-id="c6dca-105">Membres</span><span class="sxs-lookup"><span data-stu-id="c6dca-105">Members</span></span>

<span data-ttu-id="c6dca-106">L’interface **TaskCompletionClient** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c6dca-106">The **TaskCompletionClient** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c6dca-107">**TaskCompletionClient** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c6dca-107">**TaskCompletionClient** also has these types of members:</span></span>

-   [<span data-ttu-id="c6dca-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c6dca-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c6dca-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c6dca-109">Methods</span></span>

<span data-ttu-id="c6dca-110">L’interface **TaskCompletionClient** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c6dca-110">The **TaskCompletionClient** interface has these methods.</span></span>



| <span data-ttu-id="c6dca-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="c6dca-111">Method</span></span>                                                                    | <span data-ttu-id="c6dca-112">Description</span><span class="sxs-lookup"><span data-stu-id="c6dca-112">Description</span></span>                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [<span data-ttu-id="c6dca-113">**ApplyTaskCompletion**</span><span class="sxs-lookup"><span data-stu-id="c6dca-113">**ApplyTaskCompletion**</span></span>](taskcompletionclient-applytaskcompletion.md)   | <span data-ttu-id="c6dca-114">Commence l’achèvement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="c6dca-114">Begins the task completion.</span></span><br/> |
| [<span data-ttu-id="c6dca-115">**RevokeTaskCompletion**</span><span class="sxs-lookup"><span data-stu-id="c6dca-115">**RevokeTaskCompletion**</span></span>](taskcompletionclient-revoketaskcompletion.md) | <span data-ttu-id="c6dca-116">Met fin à l’achèvement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="c6dca-116">Ends the task completion.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="c6dca-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c6dca-117">Remarks</span></span>

<span data-ttu-id="c6dca-118">Le GUID de cette interface est « E97D552D-9AE9-46AA-9151-D2DA4BBB5E96 ».</span><span class="sxs-lookup"><span data-stu-id="c6dca-118">The GUID for this interface is "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span></span>

<span data-ttu-id="c6dca-119">Cette API est déconseillée et peut ne pas être disponible dans les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="c6dca-119">This API is deprecated and may not be available in future versions of Windows.</span></span> <span data-ttu-id="c6dca-120">Les applications doivent utiliser les API de l’espace de noms [**Windows. ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) à la place.</span><span class="sxs-lookup"><span data-stu-id="c6dca-120">Apps should use the APIs in the [**Windows.ApplicationModel.ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) namespace instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6dca-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c6dca-121">Requirements</span></span>



| <span data-ttu-id="c6dca-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6dca-122">Requirement</span></span> | <span data-ttu-id="c6dca-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6dca-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6dca-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6dca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c6dca-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6dca-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6dca-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6dca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c6dca-127">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6dca-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c6dca-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c6dca-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6dca-129"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6dca-129"><dt>ExecModelClient.dll</dt></span></span> </dl> |



 

 
