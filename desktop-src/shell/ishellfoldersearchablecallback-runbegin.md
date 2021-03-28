---
description: Indique qu’une recherche a été démarrée.
title: 'IShellFolderSearchableCallback :: RunBegin, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 2bef0f29486143f97f886c0d31ab456a070ed857
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527315"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a><span data-ttu-id="d2fb3-103">IShellFolderSearchableCallback :: RunBegin, méthode</span><span class="sxs-lookup"><span data-stu-id="d2fb3-103">IShellFolderSearchableCallback::RunBegin method</span></span>

<span data-ttu-id="d2fb3-104">Indique qu’une recherche a été démarrée.</span><span class="sxs-lookup"><span data-stu-id="d2fb3-104">Indicates that a search was started.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2fb3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2fb3-105">Syntax</span></span>


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="d2fb3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2fb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2fb3-107">*dwReserved* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2fb3-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2fb3-108">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d2fb3-108">Type: **DWORD**</span></span>

<span data-ttu-id="d2fb3-109">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d2fb3-109">Reserved.</span></span> <span data-ttu-id="d2fb3-110">Doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="d2fb3-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2fb3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2fb3-111">Return value</span></span>

<span data-ttu-id="d2fb3-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d2fb3-112">Type: **HRESULT**</span></span>

<span data-ttu-id="d2fb3-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d2fb3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d2fb3-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2fb3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2fb3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d2fb3-115">Remarks</span></span>

<span data-ttu-id="d2fb3-116">En réponse à ce rappel, l’application peut activer le bouton **Annuler** , par exemple.</span><span class="sxs-lookup"><span data-stu-id="d2fb3-116">In response to this callback, the application may enable the **Cancel** button, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2fb3-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d2fb3-117">Requirements</span></span>



| <span data-ttu-id="d2fb3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2fb3-118">Requirement</span></span> | <span data-ttu-id="d2fb3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2fb3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2fb3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2fb3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d2fb3-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2fb3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d2fb3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2fb3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d2fb3-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2fb3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d2fb3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d2fb3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2fb3-125"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2fb3-125"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




