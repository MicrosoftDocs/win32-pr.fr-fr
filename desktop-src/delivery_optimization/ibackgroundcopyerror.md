---
title: Interface IBackgroundCopyError (Deliveryoptimization. h)
description: Utilisez l’interface IBackgroundCopyError pour déterminer la cause d’une erreur et si le processus de transfert peut se poursuivre.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Interface IBackgroundCopyError
- Interface IBackgroundCopyError, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465078"
---
# <a name="ibackgroundcopyerror-interface"></a><span data-ttu-id="dd979-105">Interface IBackgroundCopyError</span><span class="sxs-lookup"><span data-stu-id="dd979-105">IBackgroundCopyError interface</span></span>

<span data-ttu-id="dd979-106">Utilisez l’interface **IBackgroundCopyError** pour déterminer la cause d’une erreur et si le processus de transfert peut se poursuivre.</span><span class="sxs-lookup"><span data-stu-id="dd979-106">Use the **IBackgroundCopyError** interface to determine the cause of an error and if the transfer process can proceed.</span></span>

<span data-ttu-id="dd979-107">Crée un objet d’erreur uniquement lorsque l’état du travail est BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="dd979-107">DO creates an error object only when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="dd979-108">NE créez pas d’objet d’erreur lorsqu’une méthode d’interface **IBackgroundCopyXXXX** échoue.</span><span class="sxs-lookup"><span data-stu-id="dd979-108">DO does not create an error object when an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="dd979-109">L’objet d’erreur est disponible jusqu’à ce que commence à transférer les données (l’état du travail passe à BG_JOB_STATE_TRANSFERRING) pour le travail.</span><span class="sxs-lookup"><span data-stu-id="dd979-109">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job.</span></span>

<span data-ttu-id="dd979-110">Pour récupérer un objet **IBackgroundCopyError** , appelez la méthode [**méthode ibackgroundcopyjob :: GetError**](ibackgroundcopyjob-geterror.md) .</span><span class="sxs-lookup"><span data-stu-id="dd979-110">To get an **IBackgroundCopyError** object, call the [**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="dd979-111">Membres</span><span class="sxs-lookup"><span data-stu-id="dd979-111">Members</span></span>

<span data-ttu-id="dd979-112">L’interface **IBackgroundCopyError** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dd979-112">The **IBackgroundCopyError** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dd979-113">**IBackgroundCopyError** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dd979-113">**IBackgroundCopyError** also has these types of members:</span></span>

-   [<span data-ttu-id="dd979-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dd979-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dd979-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dd979-115">Methods</span></span>

<span data-ttu-id="dd979-116">L’interface **IBackgroundCopyError** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dd979-116">The **IBackgroundCopyError** interface has these methods.</span></span>



| <span data-ttu-id="dd979-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="dd979-117">Method</span></span>                                                   | <span data-ttu-id="dd979-118">Description</span><span class="sxs-lookup"><span data-stu-id="dd979-118">Description</span></span>                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd979-119">**GetError**</span><span class="sxs-lookup"><span data-stu-id="dd979-119">**GetError**</span></span>](ibackgroundcopyerror-geterror-method.md) | <span data-ttu-id="dd979-120">Récupère le code d’erreur et identifie le contexte dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="dd979-120">Retrieves the error code and identifies the context in which the error occurred.</span></span><br/> |
| [<span data-ttu-id="dd979-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="dd979-121">**GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)   | <span data-ttu-id="dd979-122">Récupère un pointeur d’interface vers l’objet de fichier associé à l’erreur.</span><span class="sxs-lookup"><span data-stu-id="dd979-122">Retrieves an interface pointer to the file object associated with the error.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="dd979-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd979-123">Requirements</span></span>



| <span data-ttu-id="dd979-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd979-124">Requirement</span></span> | <span data-ttu-id="dd979-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd979-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd979-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd979-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dd979-127">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd979-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dd979-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd979-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dd979-129">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd979-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dd979-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd979-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd979-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd979-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd979-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="dd979-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd979-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd979-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="dd979-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd979-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd979-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd979-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="dd979-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dd979-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd979-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd979-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="dd979-138">IID</span><span class="sxs-lookup"><span data-stu-id="dd979-138">IID</span></span><br/>                      | <span data-ttu-id="dd979-139">IID_IBackgroundCopyError est défini en tant que 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="dd979-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="dd979-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd979-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd979-141">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="dd979-141">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="dd979-142">**Méthode ibackgroundcopyjob :: GetError**</span><span class="sxs-lookup"><span data-stu-id="dd979-142">**IBackgroundCopyJob::GetError**</span></span>](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[<span data-ttu-id="dd979-143">**Méthode ibackgroundcopyjob :: GetState**</span><span class="sxs-lookup"><span data-stu-id="dd979-143">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[<span data-ttu-id="dd979-144">**IBackgroundCopyCallback::JobError**</span><span class="sxs-lookup"><span data-stu-id="dd979-144">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

