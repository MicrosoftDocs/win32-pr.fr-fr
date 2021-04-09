---
title: Méthode IBackgroundCopyFile GetLocalName (Deliveryoptimization. h)
description: Récupère le nom local du fichier.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- Méthode GetLocalName
- Méthode GetLocalName, interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, méthode GetLocalName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032775"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a><span data-ttu-id="d77d8-106">IBackgroundCopyFile :: GetLocalName, méthode</span><span class="sxs-lookup"><span data-stu-id="d77d8-106">IBackgroundCopyFile::GetLocalName method</span></span>

<span data-ttu-id="d77d8-107">Récupère le nom local du fichier.</span><span class="sxs-lookup"><span data-stu-id="d77d8-107">Retrieves the local name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d77d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d77d8-108">Syntax</span></span>


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="d77d8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d77d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d77d8-110">*ppName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d77d8-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d77d8-111">Chaîne terminée par le caractère null qui contient le nom du fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="d77d8-111">Null-terminated string that contains the name of the file on the client.</span></span> <span data-ttu-id="d77d8-112">Le nom est complet.</span><span class="sxs-lookup"><span data-stu-id="d77d8-112">The name is fully qualified.</span></span> <span data-ttu-id="d77d8-113">Appelez la fonction [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer *ppName* quand vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="d77d8-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d77d8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d77d8-114">Return value</span></span>

<span data-ttu-id="d77d8-115">Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d77d8-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d77d8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d77d8-116">Requirements</span></span>



| <span data-ttu-id="d77d8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d77d8-117">Requirement</span></span> | <span data-ttu-id="d77d8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d77d8-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d77d8-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d77d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d77d8-120">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d77d8-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d77d8-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d77d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d77d8-122">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d77d8-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d77d8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d77d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d77d8-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d77d8-124"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d77d8-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="d77d8-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d77d8-126"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d77d8-126"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d77d8-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d77d8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="d77d8-128"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d77d8-128"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d77d8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d77d8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d77d8-130"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d77d8-130"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d77d8-131">IID</span><span class="sxs-lookup"><span data-stu-id="d77d8-131">IID</span></span><br/>                      | <span data-ttu-id="d77d8-132">IID_IBackgroundCopyFile est défini en tant que 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="d77d8-132">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="d77d8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d77d8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d77d8-134">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="d77d8-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="d77d8-135">**IBackgroundCopyFile::GetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="d77d8-135">**IBackgroundCopyFile::GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

