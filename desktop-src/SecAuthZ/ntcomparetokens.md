---
description: Compare deux jetons d’accès et détermine s’ils sont équivalents par rapport à un appel à la fonction AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: NtCompareTokens, fonction (Ntseapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524609"
---
# <a name="ntcomparetokens-function"></a><span data-ttu-id="2ccb6-103">NtCompareTokens fonction)</span><span class="sxs-lookup"><span data-stu-id="2ccb6-103">NtCompareTokens function</span></span>

<span data-ttu-id="2ccb6-104">La fonction **NtCompareTokens** compare deux [*jetons d’accès*](/windows/desktop/SecGloss/a-gly) et détermine s’ils sont équivalents par rapport à un appel à la fonction [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) .</span><span class="sxs-lookup"><span data-stu-id="2ccb6-104">The **NtCompareTokens** function compares two [*access tokens*](/windows/desktop/SecGloss/a-gly) and determines whether they are equivalent with respect to a call to the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ccb6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ccb6-105">Syntax</span></span>


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a><span data-ttu-id="2ccb6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ccb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ccb6-107">*FirstTokenHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ccb6-107">*FirstTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ccb6-108">Handle vers le premier jeton d’accès à comparer.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-108">A handle to the first access token to compare.</span></span> <span data-ttu-id="2ccb6-109">Le jeton doit être ouvert pour l’accès à la **\_ requête de jeton** .</span><span class="sxs-lookup"><span data-stu-id="2ccb6-109">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="2ccb6-110">*SecondTokenHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ccb6-110">*SecondTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ccb6-111">Handle vers le deuxième jeton d’accès à comparer.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-111">A handle to the second access token to compare.</span></span> <span data-ttu-id="2ccb6-112">Le jeton doit être ouvert pour l’accès à la **\_ requête de jeton** .</span><span class="sxs-lookup"><span data-stu-id="2ccb6-112">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="2ccb6-113">*Égal* \[ à à\]</span><span class="sxs-lookup"><span data-stu-id="2ccb6-113">*Equal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ccb6-114">Pointeur vers une variable qui reçoit une valeur qui indique si les jetons représentés par les paramètres *FirstTokenHandle* et *SecondTokenHandle* sont équivalents.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-114">A pointer to a variable that receives a value that indicates whether the tokens represented by the *FirstTokenHandle* and *SecondTokenHandle* parameters are equivalent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ccb6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ccb6-115">Return value</span></span>

<span data-ttu-id="2ccb6-116">Si la fonction réussit, la fonction retourne l’état \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-116">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="2ccb6-117">Si la fonction échoue, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="2ccb6-117">If the function fails, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ccb6-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2ccb6-118">Remarks</span></span>

<span data-ttu-id="2ccb6-119">Deux jetons de contrôle d’accès sont considérés comme équivalents si toutes les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="2ccb6-119">Two access control tokens are considered to be equivalent if all of the following conditions are true:</span></span>

-   <span data-ttu-id="2ccb6-120">Chaque [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) qui est présent dans l’un des jetons est également présent dans l’autre jeton.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-120">Every [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) that is present in either token is also present in the other token.</span></span>
-   <span data-ttu-id="2ccb6-121">Aucun ou les deux jetons ne sont limités.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-121">Neither or both of the tokens are restricted.</span></span>
-   <span data-ttu-id="2ccb6-122">Si les deux jetons sont restreints, chaque SID qui est limité dans un jeton est également limité dans l’autre jeton.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-122">If both tokens are restricted, every SID that is restricted in one token is also restricted in the other token.</span></span>
-   <span data-ttu-id="2ccb6-123">Chaque privilège présent dans l’un des deux jetons est également présent dans l’autre jeton.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-123">Every privilege present in either token is also present in the other token.</span></span>

<span data-ttu-id="2ccb6-124">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2ccb6-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ccb6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ccb6-125">Requirements</span></span>



| <span data-ttu-id="2ccb6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ccb6-126">Requirement</span></span> | <span data-ttu-id="2ccb6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ccb6-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ccb6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ccb6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2ccb6-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ccb6-129">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2ccb6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ccb6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2ccb6-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ccb6-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2ccb6-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ccb6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ccb6-133"><dt>Ntseapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ccb6-133"><dt>Ntseapi.h</dt></span></span> </dl> |
| <span data-ttu-id="2ccb6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2ccb6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ccb6-135"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ccb6-135"><dt>Ntdll.dll</dt></span></span> </dl> |



 

