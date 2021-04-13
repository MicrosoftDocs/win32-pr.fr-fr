---
description: Obtient le niveau d’une règle d’identification de hachage qui correspond au hachage spécifié.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: SaferiSearchMatchingHashRules fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483648"
---
# <a name="saferisearchmatchinghashrules-function"></a><span data-ttu-id="3dc30-103">SaferiSearchMatchingHashRules fonction)</span><span class="sxs-lookup"><span data-stu-id="3dc30-103">SaferiSearchMatchingHashRules function</span></span>

<span data-ttu-id="3dc30-104">Obtient le niveau d’une règle d’identification de hachage qui correspond au hachage spécifié.</span><span class="sxs-lookup"><span data-stu-id="3dc30-104">Gets the level of a hash identification rule that matches the specified hash.</span></span>

<span data-ttu-id="3dc30-105">Cette fonction n’a pas de bibliothèque d’importation associée et n’est pas déclarée dans un en-tête public.</span><span class="sxs-lookup"><span data-stu-id="3dc30-105">This function has no associated import library and is not declared in a public header.</span></span> <span data-ttu-id="3dc30-106">Vous devez définir un pointeur de fonction avec la signature de cette fonction, et vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="3dc30-106">You must define a function pointer with the signature of this function, and you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

<span data-ttu-id="3dc30-107">Nous vous recommandons d’utiliser la fonction [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) pour évaluer les stratégies de restriction logicielle.</span><span class="sxs-lookup"><span data-stu-id="3dc30-107">We recommend using the [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) function to evaluate software restriction policies.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dc30-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dc30-108">Syntax</span></span>


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3dc30-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dc30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dc30-110">*HashAlgorithm* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3dc30-110">*HashAlgorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc30-111">Identificateur de l’algorithme utilisé pour créer le hachage.</span><span class="sxs-lookup"><span data-stu-id="3dc30-111">The identifier of the algorithm used to create the hash.</span></span>

</dd> <dt>

<span data-ttu-id="3dc30-112">*pHashBytes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3dc30-112">*pHashBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc30-113">Pointeur vers un tableau d’octets qui contient le hachage.</span><span class="sxs-lookup"><span data-stu-id="3dc30-113">A pointer to an array of bytes that contains the hash.</span></span>

</dd> <dt>

<span data-ttu-id="3dc30-114">*dwHashSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3dc30-114">*dwHashSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc30-115">Taille, en octets, du tableau *pHashBytes* .</span><span class="sxs-lookup"><span data-stu-id="3dc30-115">The size, in bytes, of the *pHashBytes* array.</span></span>

</dd> <dt>

<span data-ttu-id="3dc30-116">*dwOriginalImageSize* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3dc30-116">*dwOriginalImageSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc30-117">Taille, en octets, de l’image d’origine à partir de laquelle le hachage a été calculé.</span><span class="sxs-lookup"><span data-stu-id="3dc30-117">The size, in bytes, of the original image from which the hash was computed.</span></span>

</dd> <dt>

<span data-ttu-id="3dc30-118">*pdwFoundLevel* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3dc30-118">*pdwFoundLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc30-119">Pointeur vers l’identificateur de niveau pour la règle d’identification de hachage correspondante.</span><span class="sxs-lookup"><span data-stu-id="3dc30-119">A pointer to the level identifier for the matching hash identification rule.</span></span>

</dd> <dt>

<span data-ttu-id="3dc30-120">*pdwSaferFlags*</span><span class="sxs-lookup"><span data-stu-id="3dc30-120">*pdwSaferFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="3dc30-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="3dc30-121">Reserved.</span></span> <span data-ttu-id="3dc30-122">Définissez cette valeur sur zéro.</span><span class="sxs-lookup"><span data-stu-id="3dc30-122">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dc30-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3dc30-123">Return value</span></span>

<span data-ttu-id="3dc30-124">**True** si la fonction réussit ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="3dc30-124">**TRUE** if the function is successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc30-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3dc30-125">Requirements</span></span>



| <span data-ttu-id="3dc30-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3dc30-126">Requirement</span></span> | <span data-ttu-id="3dc30-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dc30-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc30-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3dc30-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc30-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3dc30-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3dc30-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3dc30-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc30-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3dc30-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3dc30-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3dc30-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dc30-133"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dc30-133"><dt>Advapi32.dll</dt></span></span> </dl> |



 

 
