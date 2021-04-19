---
title: IBackgroundCopyError GetFile, méthode (Deliveryoptimization. h)
description: Récupère un pointeur d’interface vers l’objet de fichier associé à l’erreur.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- GetFile, méthode
- GetFile, méthode, interface IBackgroundCopyError
- Interface IBackgroundCopyError, méthode GetFile
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510533"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a><span data-ttu-id="08794-106">IBackgroundCopyError :: GetFile, méthode</span><span class="sxs-lookup"><span data-stu-id="08794-106">IBackgroundCopyError::GetFile method</span></span>

<span data-ttu-id="08794-107">Récupère un pointeur d’interface vers l’objet de fichier associé à l’erreur.</span><span class="sxs-lookup"><span data-stu-id="08794-107">Retrieves an interface pointer to the file object associated with the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="08794-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08794-108">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="08794-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08794-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08794-110">*ppFile* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="08794-110">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08794-111">Pointeur d’interface [**IBackgroundCopyFile**](ibackgroundcopyfile.md) dont les méthodes vous permettent de déterminer les noms de fichiers locaux et distants associés à l’erreur.</span><span class="sxs-lookup"><span data-stu-id="08794-111">An [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface pointer whose methods you use to determine the local and remote file names associated with the error.</span></span> <span data-ttu-id="08794-112">Le paramètre *ppFile* a la valeur **null** si l’erreur n’est pas associée au fichier local ou distant.</span><span class="sxs-lookup"><span data-stu-id="08794-112">The *ppFile* parameter is set to **NULL** if the error is not associated with the local or remote file.</span></span> <span data-ttu-id="08794-113">Lorsque vous avez terminé, libérez *ppFile*.</span><span class="sxs-lookup"><span data-stu-id="08794-113">When done, release *ppFile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08794-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08794-114">Return value</span></span>

<span data-ttu-id="08794-115">Cette méthode retourne les valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="08794-115">This method returns the following **HRESULT** values.</span></span>



| <span data-ttu-id="08794-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="08794-116">Return code</span></span>                                                                                                | <span data-ttu-id="08794-117">Description</span><span class="sxs-lookup"><span data-stu-id="08794-117">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08794-118"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="08794-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                   | <span data-ttu-id="08794-119">Un pointeur d’interface a été récupéré avec succès sur l’objet fichier.</span><span class="sxs-lookup"><span data-stu-id="08794-119">Successfully retrieved an interface pointer to the file object.</span></span><br/>                                     |
| <dl> <span data-ttu-id="08794-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="08794-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="08794-121">L’erreur n’est pas associée à un fichier local ou distant.</span><span class="sxs-lookup"><span data-stu-id="08794-121">The error is not associated with a local or remote file.</span></span> <span data-ttu-id="08794-122">Le paramètre *ppFile* a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="08794-122">The *ppFile* parameter is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="08794-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08794-123">Requirements</span></span>



| <span data-ttu-id="08794-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08794-124">Requirement</span></span> | <span data-ttu-id="08794-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="08794-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08794-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08794-126">Minimum supported client</span></span><br/> | <span data-ttu-id="08794-127">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08794-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="08794-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08794-128">Minimum supported server</span></span><br/> | <span data-ttu-id="08794-129">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08794-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="08794-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="08794-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="08794-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="08794-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="08794-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="08794-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="08794-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="08794-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="08794-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="08794-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="08794-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08794-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="08794-136">DLL</span><span class="sxs-lookup"><span data-stu-id="08794-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08794-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08794-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="08794-138">IID</span><span class="sxs-lookup"><span data-stu-id="08794-138">IID</span></span><br/>                      | <span data-ttu-id="08794-139">IID_IBackgroundCopyError est défini en tant que 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="08794-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="08794-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08794-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08794-141">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="08794-141">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="08794-142">**IBackgroundCopyError::GetError**</span><span class="sxs-lookup"><span data-stu-id="08794-142">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





