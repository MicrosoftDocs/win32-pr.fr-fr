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
ms.openlocfilehash: 953bf54ff64cf41724ce0dfabd064f9c7b980cc6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842810"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a><span data-ttu-id="9adb7-103">IShellFolderSearchableCallback :: RunBegin, méthode</span><span class="sxs-lookup"><span data-stu-id="9adb7-103">IShellFolderSearchableCallback::RunBegin method</span></span>

<span data-ttu-id="9adb7-104">Indique qu’une recherche a été démarrée.</span><span class="sxs-lookup"><span data-stu-id="9adb7-104">Indicates that a search was started.</span></span>

## <a name="syntax"></a><span data-ttu-id="9adb7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9adb7-105">Syntax</span></span>


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="9adb7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9adb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9adb7-107">*dwReserved* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9adb7-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9adb7-108">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9adb7-108">Type: **DWORD**</span></span>

<span data-ttu-id="9adb7-109">Réservé.</span><span class="sxs-lookup"><span data-stu-id="9adb7-109">Reserved.</span></span> <span data-ttu-id="9adb7-110">Doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="9adb7-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9adb7-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9adb7-111">Return value</span></span>

<span data-ttu-id="9adb7-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9adb7-112">Type: **HRESULT**</span></span>

<span data-ttu-id="9adb7-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9adb7-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9adb7-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9adb7-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9adb7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9adb7-115">Remarks</span></span>

<span data-ttu-id="9adb7-116">En réponse à ce rappel, l’application peut activer le bouton **Annuler** , par exemple.</span><span class="sxs-lookup"><span data-stu-id="9adb7-116">In response to this callback, the application may enable the **Cancel** button, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="9adb7-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9adb7-117">Requirements</span></span>



| <span data-ttu-id="9adb7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9adb7-118">Requirement</span></span> | <span data-ttu-id="9adb7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9adb7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9adb7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9adb7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9adb7-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9adb7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9adb7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9adb7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9adb7-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9adb7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9adb7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9adb7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9adb7-125"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9adb7-125"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




