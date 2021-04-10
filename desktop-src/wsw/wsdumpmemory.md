---
title: WsDumpMemory, fonction (WebServicesDebug. h)
description: Cette fonction vide toutes les allocations de mémoire dans la console.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Services Web de fonction WsDumpMemory pour Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942602"
---
# <a name="wsdumpmemory-function"></a><span data-ttu-id="83f20-104">WsDumpMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="83f20-104">WsDumpMemory function</span></span>

<span data-ttu-id="83f20-105">Cette fonction vide toutes les allocations de mémoire dans la console.</span><span class="sxs-lookup"><span data-stu-id="83f20-105">This function dumps all memory allocations to the console.</span></span>

> [!Note]  
> <span data-ttu-id="83f20-106">Cette fonction est destinée uniquement au débogage.</span><span class="sxs-lookup"><span data-stu-id="83f20-106">This function is for DEBUG ONLY.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="83f20-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83f20-107">Syntax</span></span>


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="83f20-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83f20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83f20-109">*erreur* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="83f20-109">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83f20-110">Pointeur vers un objet [d' \_ erreur WS](ws-error.md) où des informations supplémentaires sur l’erreur doivent être stockées si la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="83f20-110">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83f20-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83f20-111">Return value</span></span>

<span data-ttu-id="83f20-112">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="83f20-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="83f20-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="83f20-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="83f20-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83f20-114">Requirements</span></span>



| <span data-ttu-id="83f20-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83f20-115">Requirement</span></span> | <span data-ttu-id="83f20-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="83f20-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="83f20-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83f20-117">Minimum supported client</span></span><br/> | <span data-ttu-id="83f20-118">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="83f20-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                             |
| <span data-ttu-id="83f20-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83f20-119">Minimum supported server</span></span><br/> | <span data-ttu-id="83f20-120">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="83f20-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="83f20-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="83f20-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="83f20-122"><dt>WebServicesDebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="83f20-122"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





