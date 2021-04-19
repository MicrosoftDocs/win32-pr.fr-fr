---
description: La fonction ParserTemporaryLockFrame verrouille un frame lorsqu’il entre dans un analyseur et déverrouille le frame lorsque la fonction quitte l’analyseur.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: ParserTemporaryLockFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536833"
---
# <a name="parsertemporarylockframe-function"></a><span data-ttu-id="56264-103">ParserTemporaryLockFrame fonction)</span><span class="sxs-lookup"><span data-stu-id="56264-103">ParserTemporaryLockFrame function</span></span>

<span data-ttu-id="56264-104">La fonction **ParserTemporaryLockFrame** verrouille un frame lorsqu’il entre dans un analyseur et déverrouille le frame lorsque la fonction quitte l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="56264-104">The **ParserTemporaryLockFrame** function locks a frame when it enters a parser and unlocks the frame when the function exits the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="56264-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56264-105">Syntax</span></span>


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="56264-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56264-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56264-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56264-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56264-108">Handle vers le frame vers lequel pointe l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="56264-108">Handle to the frame that the parser points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56264-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56264-109">Return value</span></span>

<span data-ttu-id="56264-110">Si la fonction réussit, la valeur de retour est un pointeur vers le premier octet de données dans le frame.</span><span class="sxs-lookup"><span data-stu-id="56264-110">If the function is successful, the return value is a pointer to the first byte of data in the frame.</span></span>

<span data-ttu-id="56264-111">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="56264-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="56264-112">Notes</span><span class="sxs-lookup"><span data-stu-id="56264-112">Remarks</span></span>

<span data-ttu-id="56264-113">Les analyseurs ne doivent pas appeler la fonction **LockFrame** .</span><span class="sxs-lookup"><span data-stu-id="56264-113">Parsers should not call the **LockFrame** function.</span></span> <span data-ttu-id="56264-114">Si un analyseur prend un verrou, puis génère une erreur ou retourne sans déverrouiller le frame, l’analyseur laisse le système dans un État où il ne peut pas modifier les protocoles ni couper ou copier les frames.</span><span class="sxs-lookup"><span data-stu-id="56264-114">If a parser takes a lock and then generates a fault or returns without unlocking the frame, the parser leaves the system in a state where it cannot change protocols or cut or copy frames.</span></span> <span data-ttu-id="56264-115">Les analyseurs doivent utiliser la fonction **ParserTemporaryLockFrame** , qui accorde un verrou uniquement pendant le contexte de l’entrée de la fonction dans l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="56264-115">Parsers should use the **ParserTemporaryLockFrame** function, which grants a lock only during the context of the function entry into the parser.</span></span> <span data-ttu-id="56264-116">À la sortie de l’analyseur, le verrou de ce frame est libéré.</span><span class="sxs-lookup"><span data-stu-id="56264-116">On exit from the parser, the lock for that frame is released.</span></span> <span data-ttu-id="56264-117">Par conséquent, le pointeur est valide uniquement après le retour de l’analyseur à partir de l’appel à la fonction **AttachProperties** ou **RecognizeFrame** .</span><span class="sxs-lookup"><span data-stu-id="56264-117">As a result, the pointer will be valid only after the parser returns from the call to the **AttachProperties** or **RecognizeFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="56264-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56264-118">Requirements</span></span>



| <span data-ttu-id="56264-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56264-119">Requirement</span></span> | <span data-ttu-id="56264-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="56264-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="56264-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56264-121">Minimum supported client</span></span><br/> | <span data-ttu-id="56264-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56264-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="56264-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56264-123">Minimum supported server</span></span><br/> | <span data-ttu-id="56264-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56264-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="56264-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="56264-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="56264-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="56264-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="56264-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="56264-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="56264-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56264-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="56264-129">DLL</span><span class="sxs-lookup"><span data-stu-id="56264-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56264-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56264-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




