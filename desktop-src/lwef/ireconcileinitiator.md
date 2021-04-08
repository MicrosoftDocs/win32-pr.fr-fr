---
title: Interface IReconcileInitiator
description: Expose des méthodes qui fournissent le réconciliateur de porte-documents avec le moyen d’informer l’initiateur de sa progression, de définir un objet de fin et de demander une version donnée d’un document. L’initiateur est responsable de l’implémentation de cette interface.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IReconcileInitiator
- Fonctionnalités d’environnement Windows héritées de l’interface IReconcileInitiator, Description
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741597"
---
# <a name="ireconcileinitiator-interface"></a><span data-ttu-id="2b9f3-106">Interface IReconcileInitiator</span><span class="sxs-lookup"><span data-stu-id="2b9f3-106">IReconcileInitiator interface</span></span>

<span data-ttu-id="2b9f3-107">Expose des méthodes qui fournissent le réconciliateur de porte-documents avec le moyen d’informer l’initiateur de sa progression, de définir un objet de fin et de demander une version donnée d’un document.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-107">Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document.</span></span> <span data-ttu-id="2b9f3-108">L’initiateur est responsable de l’implémentation de cette interface.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-108">The initiator is responsible for implementing this interface.</span></span>

## <a name="members"></a><span data-ttu-id="2b9f3-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2b9f3-109">Members</span></span>

<span data-ttu-id="2b9f3-110">L’interface **IReconcileInitiator** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2b9f3-110">The **IReconcileInitiator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2b9f3-111">**IReconcileInitiator** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2b9f3-111">**IReconcileInitiator** also has these types of members:</span></span>

-   [<span data-ttu-id="2b9f3-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2b9f3-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2b9f3-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2b9f3-113">Methods</span></span>

<span data-ttu-id="2b9f3-114">L’interface **IReconcileInitiator** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-114">The **IReconcileInitiator** interface has these methods.</span></span>



| <span data-ttu-id="2b9f3-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="2b9f3-115">Method</span></span>                                                                 | <span data-ttu-id="2b9f3-116">Description</span><span class="sxs-lookup"><span data-stu-id="2b9f3-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b9f3-117">**SetAbortCallback**</span><span class="sxs-lookup"><span data-stu-id="2b9f3-117">**SetAbortCallback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | <span data-ttu-id="2b9f3-118">Définit l’objet par le biais duquel l’initiateur peut arrêter de manière asynchrone un rapprochement.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-118">Sets the object through which the initiator can asynchronously terminate a reconciliation.</span></span> <span data-ttu-id="2b9f3-119">Un réconciliateur de porte-documents définit généralement cet objet pour les réconciliations qui sont longues ou qui impliquent une interaction avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-119">A briefcase reconciler typically sets this object for reconciliations that are lengthy or involve user interaction.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="2b9f3-120">**SetProgressFeedback**</span><span class="sxs-lookup"><span data-stu-id="2b9f3-120">**SetProgressFeedback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | <span data-ttu-id="2b9f3-121">Indique la progression du réconciliateur de porte-documents sur la réalisation du rapprochement.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-121">Indicates the amount of progress the briefcase reconciler has made toward completing the reconciliation.</span></span> <span data-ttu-id="2b9f3-122">Le montant est une fraction et est calculé comme le quotient des paramètres *ulProgress* et *ulProgressMax* .</span><span class="sxs-lookup"><span data-stu-id="2b9f3-122">The amount is a fraction and is computed as the quotient of the *ulProgress* and *ulProgressMax* parameters.</span></span> <span data-ttu-id="2b9f3-123">Les réviseurs doivent appeler cette méthode périodiquement au cours de leur processus de rapprochement.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-123">Reconcilers should call this method periodically during their reconciliation process.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b9f3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b9f3-124">Requirements</span></span>



| <span data-ttu-id="2b9f3-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b9f3-125">Requirement</span></span> | <span data-ttu-id="2b9f3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b9f3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b9f3-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b9f3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2b9f3-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b9f3-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="2b9f3-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b9f3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2b9f3-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b9f3-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2b9f3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2b9f3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b9f3-132"><dt>Shell32.dll (version 4,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="2b9f3-132"><dt>Shell32.dll (version 4.0 or later)</dt></span></span> </dl> |



 

