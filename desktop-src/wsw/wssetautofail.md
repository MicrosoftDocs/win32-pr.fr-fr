---
title: WsSetAutoFail, fonction (WebServicesDebug. h)
description: Définit le point suivant pour injecter un échec. Il s’agit d’une fonction de débogage uniquement.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Services Web de fonction WsSetAutoFail pour Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509082"
---
# <a name="wssetautofail-function"></a><span data-ttu-id="a816e-105">WsSetAutoFail fonction)</span><span class="sxs-lookup"><span data-stu-id="a816e-105">WsSetAutoFail function</span></span>

<span data-ttu-id="a816e-106">Définit le point suivant pour injecter un échec.</span><span class="sxs-lookup"><span data-stu-id="a816e-106">Sets the next point to inject a failure.</span></span> <span data-ttu-id="a816e-107">Il s’agit d’une fonction de débogage uniquement.</span><span class="sxs-lookup"><span data-stu-id="a816e-107">This is a DEBUG ONLY function.</span></span>

## <a name="syntax"></a><span data-ttu-id="a816e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a816e-108">Syntax</span></span>


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="a816e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a816e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a816e-110">*nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a816e-110">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a816e-111">Spécifie combien d’opérations avant les échecs commencent à se produire.</span><span class="sxs-lookup"><span data-stu-id="a816e-111">Specifies how many operations before failures begin to occur.</span></span>

</dd> <dt>

<span data-ttu-id="a816e-112">*erreur* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a816e-112">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a816e-113">Pointeur vers un objet [d' \_ erreur WS](ws-error.md) où des informations supplémentaires sur l’erreur doivent être stockées si la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="a816e-113">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a816e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a816e-114">Return value</span></span>

<span data-ttu-id="a816e-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a816e-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a816e-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a816e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a816e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a816e-117">Requirements</span></span>



| <span data-ttu-id="a816e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a816e-118">Requirement</span></span> | <span data-ttu-id="a816e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a816e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a816e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a816e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a816e-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a816e-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a816e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a816e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a816e-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a816e-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a816e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a816e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a816e-125"><dt>WebServicesDebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="a816e-125"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





