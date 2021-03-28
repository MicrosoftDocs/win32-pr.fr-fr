---
description: Indique qu’une recherche est terminée.
title: 'IShellFolderSearchableCallback :: RunEnd, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunEnd
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91700764-6cdf-488d-adc0-e34d9b4cb71d
ms.openlocfilehash: 73155e65f4b6edb4a4b4b9b0d52ab5b042fa68b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991300"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="fec86-103">IShellFolderSearchableCallback :: RunEnd, méthode</span><span class="sxs-lookup"><span data-stu-id="fec86-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="fec86-104">Indique qu’une recherche est terminée.</span><span class="sxs-lookup"><span data-stu-id="fec86-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec86-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fec86-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="fec86-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fec86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fec86-107">*dwReserved* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fec86-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fec86-108">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="fec86-108">Type: **DWORD**</span></span>

<span data-ttu-id="fec86-109">Réservé.</span><span class="sxs-lookup"><span data-stu-id="fec86-109">Reserved.</span></span> <span data-ttu-id="fec86-110">Doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="fec86-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fec86-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fec86-111">Return value</span></span>

<span data-ttu-id="fec86-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fec86-112">Type: **HRESULT**</span></span>

<span data-ttu-id="fec86-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fec86-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fec86-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fec86-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fec86-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fec86-115">Requirements</span></span>



| <span data-ttu-id="fec86-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fec86-116">Requirement</span></span> | <span data-ttu-id="fec86-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fec86-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fec86-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fec86-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fec86-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fec86-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fec86-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fec86-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fec86-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fec86-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fec86-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fec86-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fec86-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fec86-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




