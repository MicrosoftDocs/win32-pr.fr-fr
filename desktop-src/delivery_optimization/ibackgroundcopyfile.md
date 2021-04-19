---
title: Interface IBackgroundCopyFile (Deliveryoptimization. h)
description: IBackgroundCopyFile contient des informations sur un fichier qui fait partie d’un travail. Par exemple, vous pouvez utiliser les méthodes IBackgroundCopyFile pour récupérer les noms locaux et distants du fichier et transférer les informations de progression.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543421"
---
# <a name="ibackgroundcopyfile-interface"></a><span data-ttu-id="3f7ae-106">Interface IBackgroundCopyFile</span><span class="sxs-lookup"><span data-stu-id="3f7ae-106">IBackgroundCopyFile interface</span></span>

<span data-ttu-id="3f7ae-107">**IBackgroundCopyFile** contient des informations sur un fichier qui fait partie d’un travail.</span><span class="sxs-lookup"><span data-stu-id="3f7ae-107">**IBackgroundCopyFile** contains information about a file that is part of a job.</span></span> <span data-ttu-id="3f7ae-108">Par exemple, vous pouvez utiliser les méthodes **IBackgroundCopyFile** pour récupérer les noms locaux et distants du fichier et transférer les informations de progression.</span><span class="sxs-lookup"><span data-stu-id="3f7ae-108">For example, you can use **IBackgroundCopyFile** methods to retrieve the local and remote names of the file and transfer progress information.</span></span>

<span data-ttu-id="3f7ae-109">Pour récupérer un pointeur d’interface **IBackgroundCopyFile** , appelez la méthode [**IBackgroundCopyError :: GetFile**](ibackgroundcopyerror-getfile-method.md) ou la méthode [**IEnumBackgroundCopyFiles :: Next**](ienumbackgroundcopyfiles-next.md) .</span><span class="sxs-lookup"><span data-stu-id="3f7ae-109">To get an **IBackgroundCopyFile** interface pointer, call the [**IBackgroundCopyError::GetFile**](ibackgroundcopyerror-getfile-method.md) method or the [**IEnumBackgroundCopyFiles::Next**](ienumbackgroundcopyfiles-next.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="3f7ae-110">Membres</span><span class="sxs-lookup"><span data-stu-id="3f7ae-110">Members</span></span>

<span data-ttu-id="3f7ae-111">L’interface **IBackgroundCopyFile** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3f7ae-111">The **IBackgroundCopyFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3f7ae-112">**IBackgroundCopyFile** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3f7ae-112">**IBackgroundCopyFile** also has these types of members:</span></span>

-   [<span data-ttu-id="3f7ae-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f7ae-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3f7ae-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f7ae-114">Methods</span></span>

<span data-ttu-id="3f7ae-115">L’interface **IBackgroundCopyFile** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3f7ae-115">The **IBackgroundCopyFile** interface has these methods.</span></span>



| <span data-ttu-id="3f7ae-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="3f7ae-116">Method</span></span>                                                            | <span data-ttu-id="3f7ae-117">Description</span><span class="sxs-lookup"><span data-stu-id="3f7ae-117">Description</span></span>                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="3f7ae-118">**GetLocalName**</span><span class="sxs-lookup"><span data-stu-id="3f7ae-118">**GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)   | <span data-ttu-id="3f7ae-119">Récupère le nom local du fichier.</span><span class="sxs-lookup"><span data-stu-id="3f7ae-119">Retrieves the local name of the file.</span></span><br/>        |
| [<span data-ttu-id="3f7ae-120">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="3f7ae-120">**GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)     | <span data-ttu-id="3f7ae-121">Récupère la progression du transfert de fichier.</span><span class="sxs-lookup"><span data-stu-id="3f7ae-121">Retrieves the progress of the file transfer.</span></span><br/> |
| [<span data-ttu-id="3f7ae-122">**GetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="3f7ae-122">**GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md) | <span data-ttu-id="3f7ae-123">Récupère le nom distant du fichier.</span><span class="sxs-lookup"><span data-stu-id="3f7ae-123">Retrieves the remote name of the file.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="3f7ae-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f7ae-124">Requirements</span></span>



| <span data-ttu-id="3f7ae-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f7ae-125">Requirement</span></span> | <span data-ttu-id="3f7ae-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f7ae-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7ae-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f7ae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3f7ae-128">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f7ae-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3f7ae-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f7ae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3f7ae-130">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f7ae-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3f7ae-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f7ae-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f7ae-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f7ae-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f7ae-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="3f7ae-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3f7ae-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3f7ae-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3f7ae-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f7ae-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f7ae-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f7ae-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3f7ae-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3f7ae-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f7ae-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f7ae-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3f7ae-139">IID</span><span class="sxs-lookup"><span data-stu-id="3f7ae-139">IID</span></span><br/>                      | <span data-ttu-id="3f7ae-140">IID_IBackgroundCopyFile est défini en tant que 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="3f7ae-140">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="3f7ae-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f7ae-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f7ae-142">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="3f7ae-142">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="3f7ae-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="3f7ae-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> <dt>

[<span data-ttu-id="3f7ae-144">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="3f7ae-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="3f7ae-145">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="3f7ae-145">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

