---
title: Méthode IBackgroundCopyFile GetRemoteName (Deliveryoptimization. h)
description: Récupère le nom distant du fichier.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Méthode GetRemoteName
- Méthode GetRemoteName, interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, méthode GetRemoteName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9984ed9971fdfb91279dabc5810490b62804b7e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032773"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a><span data-ttu-id="d6bd2-106">IBackgroundCopyFile :: GetRemoteName, méthode</span><span class="sxs-lookup"><span data-stu-id="d6bd2-106">IBackgroundCopyFile::GetRemoteName method</span></span>

<span data-ttu-id="d6bd2-107">Récupère le nom distant du fichier.</span><span class="sxs-lookup"><span data-stu-id="d6bd2-107">Retrieves the remote name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6bd2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6bd2-108">Syntax</span></span>


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="d6bd2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6bd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6bd2-110">*ppName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6bd2-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bd2-111">Chaîne terminée par le caractère null qui contient le nom distant du fichier à transférer.</span><span class="sxs-lookup"><span data-stu-id="d6bd2-111">Null-terminated string that contains the remote name of the file to transfer.</span></span> <span data-ttu-id="d6bd2-112">Le nom est complet.</span><span class="sxs-lookup"><span data-stu-id="d6bd2-112">The name is fully qualified.</span></span> <span data-ttu-id="d6bd2-113">Appelez la fonction [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer *ppName* quand vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="d6bd2-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6bd2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6bd2-114">Return value</span></span>

<span data-ttu-id="d6bd2-115">Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d6bd2-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6bd2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d6bd2-116">Remarks</span></span>

<span data-ttu-id="d6bd2-117">Pour modifier le nom du fichier distant, appelez la méthode [**IBackgroundCopyFile2 :: SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) .</span><span class="sxs-lookup"><span data-stu-id="d6bd2-117">To change the remote file name, call the [**IBackgroundCopyFile2::SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6bd2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6bd2-118">Requirements</span></span>



| <span data-ttu-id="d6bd2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6bd2-119">Requirement</span></span> | <span data-ttu-id="d6bd2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6bd2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6bd2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6bd2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d6bd2-122">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6bd2-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d6bd2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6bd2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d6bd2-124">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6bd2-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d6bd2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6bd2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6bd2-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6bd2-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6bd2-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="d6bd2-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6bd2-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6bd2-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d6bd2-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d6bd2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6bd2-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6bd2-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d6bd2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d6bd2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6bd2-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6bd2-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d6bd2-133">IID</span><span class="sxs-lookup"><span data-stu-id="d6bd2-133">IID</span></span><br/>                      | <span data-ttu-id="d6bd2-134">IID_IBackgroundCopyFile est défini en tant que 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="d6bd2-134">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="d6bd2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6bd2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6bd2-136">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="d6bd2-136">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="d6bd2-137">**IBackgroundCopyFile::GetLocalName**</span><span class="sxs-lookup"><span data-stu-id="d6bd2-137">**IBackgroundCopyFile::GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

