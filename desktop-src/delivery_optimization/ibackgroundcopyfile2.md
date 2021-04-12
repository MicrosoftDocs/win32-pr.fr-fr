---
title: Interface IBackgroundCopyFile2 (Deliveryoptimization. h)
description: Utilisez l’interface IBackgroundCopyFile2 pour spécifier un nouveau nom distant pour le fichier et récupérer la liste des plages à télécharger.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- Interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032772"
---
# <a name="ibackgroundcopyfile2-interface"></a><span data-ttu-id="9a354-105">Interface IBackgroundCopyFile2</span><span class="sxs-lookup"><span data-stu-id="9a354-105">IBackgroundCopyFile2 interface</span></span>

<span data-ttu-id="9a354-106">Utilisez l’interface **IBackgroundCopyFile2** pour spécifier un nouveau nom distant pour le fichier et récupérer la liste des plages à télécharger.</span><span class="sxs-lookup"><span data-stu-id="9a354-106">Use the **IBackgroundCopyFile2** interface to specify a new remote name for the file and retrieve the list of ranges to download.</span></span>

<span data-ttu-id="9a354-107">L’interface **IBackgroundCopyFile2** hérite de l’interface [**IBackgroundCopyFile**](ibackgroundcopyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="9a354-107">The **IBackgroundCopyFile2** interface inherits from the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface.</span></span>

<span data-ttu-id="9a354-108">Pour obtenir un pointeur d’interface **IBackgroundCopyFile2** , appelez la méthode **IBackgroundCopyFile :: QueryInterface** à l’aide de __uuidof (IBackgroundCopyFile2) pour l’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="9a354-108">To get an **IBackgroundCopyFile2** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile2) for the interface identifier.</span></span> <span data-ttu-id="9a354-109">Utilisez le pointeur d’interface **IBackgroundCopyFile2** pour appeler les méthodes [**IBackgroundCopyFile**](ibackgroundcopyfile.md) et **IBackgroundCopyFile2** .</span><span class="sxs-lookup"><span data-stu-id="9a354-109">Use the **IBackgroundCopyFile2** interface pointer to call both the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) and **IBackgroundCopyFile2** methods.</span></span>

## <a name="members"></a><span data-ttu-id="9a354-110">Membres</span><span class="sxs-lookup"><span data-stu-id="9a354-110">Members</span></span>

<span data-ttu-id="9a354-111">L’interface **IBackgroundCopyFile2** hérite de [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span><span class="sxs-lookup"><span data-stu-id="9a354-111">The **IBackgroundCopyFile2** interface inherits from [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span></span> <span data-ttu-id="9a354-112">**IBackgroundCopyFile2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9a354-112">**IBackgroundCopyFile2** also has these types of members:</span></span>

-   [<span data-ttu-id="9a354-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9a354-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9a354-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9a354-114">Methods</span></span>

<span data-ttu-id="9a354-115">L’interface **IBackgroundCopyFile2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9a354-115">The **IBackgroundCopyFile2** interface has these methods.</span></span>



| <span data-ttu-id="9a354-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="9a354-116">Method</span></span>                                                             | <span data-ttu-id="9a354-117">Description</span><span class="sxs-lookup"><span data-stu-id="9a354-117">Description</span></span>                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="9a354-118">**GetFileRanges**</span><span class="sxs-lookup"><span data-stu-id="9a354-118">**GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md) | <span data-ttu-id="9a354-119">Récupère le tableau de plages que vous souhaitez télécharger à partir de l’URL.</span><span class="sxs-lookup"><span data-stu-id="9a354-119">Retrieves the array of ranges that you want to download from the URL.</span></span><br/> |
| [<span data-ttu-id="9a354-120">**SetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="9a354-120">**SetRemoteName**</span></span>](ibackgroundcopyfile2-setremotename-method.md) | <span data-ttu-id="9a354-121">Remplace le nom distant par une nouvelle URL.</span><span class="sxs-lookup"><span data-stu-id="9a354-121">Changes the remote name to a new URL.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="9a354-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a354-122">Requirements</span></span>



| <span data-ttu-id="9a354-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a354-123">Requirement</span></span> | <span data-ttu-id="9a354-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a354-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a354-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a354-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9a354-126">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a354-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9a354-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a354-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9a354-128">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a354-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9a354-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a354-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a354-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a354-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a354-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="9a354-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a354-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a354-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9a354-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9a354-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a354-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a354-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9a354-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9a354-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a354-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a354-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9a354-137">IID</span><span class="sxs-lookup"><span data-stu-id="9a354-137">IID</span></span><br/>                      | <span data-ttu-id="9a354-138">IID_IBackgroundCopyFile2 est défini en tant que 83E81B93-0873-474D-8A8C-F2018B1A939C</span><span class="sxs-lookup"><span data-stu-id="9a354-138">IID_IBackgroundCopyFile2 is defined as 83E81B93-0873-474D-8A8C-F2018B1A939C</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="9a354-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a354-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a354-140">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="9a354-140">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> </dl>

 

 





