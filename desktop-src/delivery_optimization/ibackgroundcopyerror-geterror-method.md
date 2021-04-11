---
title: Méthode IBackgroundCopyError GetError (Deliveryoptimization. h)
description: Récupère le code d’erreur et identifie le contexte dans lequel l’erreur s’est produite.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Méthode GetError
- Méthode GetError, interface IBackgroundCopyError
- Interface IBackgroundCopyError, méthode GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942037"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a><span data-ttu-id="62a80-106">IBackgroundCopyError :: GetError, méthode</span><span class="sxs-lookup"><span data-stu-id="62a80-106">IBackgroundCopyError::GetError method</span></span>

<span data-ttu-id="62a80-107">Récupère le code d’erreur et identifie le contexte dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="62a80-107">Retrieves the error code and identify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a80-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62a80-108">Syntax</span></span>


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="62a80-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62a80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a80-110">*pContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="62a80-110">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62a80-111">Contexte dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="62a80-111">Context in which the error occurred.</span></span> <span data-ttu-id="62a80-112">Pour obtenir la liste des valeurs de contexte, consultez l’énumération [**BG_ERROR_CONTEXT**](bg-error-context.md) .</span><span class="sxs-lookup"><span data-stu-id="62a80-112">For a list of context values, see the [**BG_ERROR_CONTEXT**](bg-error-context.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="62a80-113">*pErrorCode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="62a80-113">*pErrorCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62a80-114">Code d’erreur de l’erreur qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="62a80-114">Error code of the error that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a80-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62a80-115">Return value</span></span>

<span data-ttu-id="62a80-116">Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com HRESULT standard en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="62a80-116">This method returns **S_OK** on success or one of the standard COM HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a80-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62a80-117">Requirements</span></span>



| <span data-ttu-id="62a80-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62a80-118">Requirement</span></span> | <span data-ttu-id="62a80-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="62a80-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a80-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62a80-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62a80-121">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62a80-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="62a80-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62a80-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62a80-123">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62a80-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="62a80-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="62a80-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62a80-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="62a80-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="62a80-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="62a80-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62a80-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62a80-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="62a80-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="62a80-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="62a80-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62a80-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="62a80-130">DLL</span><span class="sxs-lookup"><span data-stu-id="62a80-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62a80-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a80-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="62a80-132">IID</span><span class="sxs-lookup"><span data-stu-id="62a80-132">IID</span></span><br/>                      | <span data-ttu-id="62a80-133">IID_IBackgroundCopyError est défini en tant que 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="62a80-133">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="62a80-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62a80-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a80-135">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="62a80-135">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="62a80-136">**IBackgroundCopyError :: GetFile**</span><span class="sxs-lookup"><span data-stu-id="62a80-136">**IBackgroundCopyError::GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





