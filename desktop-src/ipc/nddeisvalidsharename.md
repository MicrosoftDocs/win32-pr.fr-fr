---
description: Détermine si un nom de partage utilise la syntaxe appropriée.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: NDdeIsValidShareName, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513967"
---
# <a name="nddeisvalidsharename-function"></a><span data-ttu-id="063d8-103">NDdeIsValidShareName fonction)</span><span class="sxs-lookup"><span data-stu-id="063d8-103">NDdeIsValidShareName function</span></span>

<span data-ttu-id="063d8-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="063d8-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="063d8-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="063d8-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="063d8-106">Détermine si un nom de partage utilise la syntaxe appropriée.</span><span class="sxs-lookup"><span data-stu-id="063d8-106">Determines whether a share name uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="063d8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="063d8-107">Syntax</span></span>


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a><span data-ttu-id="063d8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="063d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="063d8-109">*Nom_Partage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="063d8-109">*shareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="063d8-110">Nom de partage à valider.</span><span class="sxs-lookup"><span data-stu-id="063d8-110">The share name to be validated.</span></span> <span data-ttu-id="063d8-111">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="063d8-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="063d8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="063d8-112">Return value</span></span>

<span data-ttu-id="063d8-113">Si la syntaxe du nom de partage est valide, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="063d8-113">If the share name has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="063d8-114">Si la syntaxe du nom de partage n’est pas valide, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="063d8-114">If the share name does not have valid syntax, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="063d8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="063d8-115">Remarks</span></span>

<span data-ttu-id="063d8-116">Cette fonction est également appelée par [**NDdeShareAdd**](nddeshareadd.md) lors de la création du partage DDE.</span><span class="sxs-lookup"><span data-stu-id="063d8-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="063d8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="063d8-117">Requirements</span></span>



| <span data-ttu-id="063d8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="063d8-118">Requirement</span></span> | <span data-ttu-id="063d8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="063d8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="063d8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="063d8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="063d8-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="063d8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="063d8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="063d8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="063d8-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="063d8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="063d8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="063d8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="063d8-125"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="063d8-125"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="063d8-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="063d8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="063d8-127"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="063d8-127"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="063d8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="063d8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="063d8-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="063d8-129"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="063d8-130">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="063d8-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="063d8-131">**NDdeIsValidShareNameW** (Unicode) et **NDdeIsValidShareNameA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="063d8-131">**NDdeIsValidShareNameW** (Unicode) and **NDdeIsValidShareNameA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="063d8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="063d8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="063d8-133">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="063d8-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="063d8-134">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="063d8-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="063d8-135">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="063d8-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




