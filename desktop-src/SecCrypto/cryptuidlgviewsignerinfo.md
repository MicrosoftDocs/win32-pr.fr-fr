---
description: Affiche une boîte de dialogue qui contient les informations sur le signataire d’un message signé.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: CryptUIDlgViewSignerInfo, fonction
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862310"
---
# <a name="cryptuidlgviewsignerinfo-function"></a><span data-ttu-id="fbaf5-103">CryptUIDlgViewSignerInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="fbaf5-103">CryptUIDlgViewSignerInfo function</span></span>

<span data-ttu-id="fbaf5-104">\[La fonction **CryptUIDlgViewSignerInfo** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-104">\[The **CryptUIDlgViewSignerInfo** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fbaf5-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="fbaf5-106">\]</span><span class="sxs-lookup"><span data-stu-id="fbaf5-106">\]</span></span>

<span data-ttu-id="fbaf5-107">La fonction **CryptUIDlgViewSignerInfo** affiche une boîte de dialogue qui contient les informations sur le signataire d’un message signé.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-107">The **CryptUIDlgViewSignerInfo** function displays a dialog box that contains the signer information for a signed message.</span></span>

> [!Note]  
> <span data-ttu-id="fbaf5-108">Cette fonction n’est pas déclarée dans un fichier d’en-tête publié.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-108">This function is not declared in a published header file.</span></span> <span data-ttu-id="fbaf5-109">Pour utiliser cette structure, déclarez-la dans le format exact indiqué.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-109">To use this structure, declare it in the exact format shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbaf5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbaf5-110">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="fbaf5-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbaf5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbaf5-112">*pcvsi* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbaf5-112">*pcvsi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbaf5-113">Pointeur vers une structure [**de \_ \_ struct VIEWSIGNERINFO**](cryptui-viewsignerinfo-struct.md) qui contient les informations de signataire à afficher.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-113">A pointer to a [**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**](cryptui-viewsignerinfo-struct.md) structure that contains the signer information to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbaf5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbaf5-114">Return value</span></span>

<span data-ttu-id="fbaf5-115">Cette fonction retourne une valeur différente de zéro en cas de réussite et zéro en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-115">This function returns a nonzero value on success and zero on failure.</span></span> <span data-ttu-id="fbaf5-116">Pour obtenir des informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="fbaf5-116">For extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="fbaf5-117">Les codes d’erreur possibles retournés par [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) incluent, mais ne sont pas limités à, ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-117">Possible error codes returned from [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) include, but are not limited to, the following.</span></span>



| <span data-ttu-id="fbaf5-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fbaf5-118">Return code</span></span>                                                                                   | <span data-ttu-id="fbaf5-119">Description</span><span class="sxs-lookup"><span data-stu-id="fbaf5-119">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="fbaf5-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fbaf5-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fbaf5-121">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-121">One or more arguments are not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="fbaf5-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="fbaf5-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fbaf5-123">Un échec d’allocation de mémoire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-123">A memory allocation failure occurred.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="fbaf5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbaf5-124">Requirements</span></span>



| <span data-ttu-id="fbaf5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbaf5-125">Requirement</span></span> | <span data-ttu-id="fbaf5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbaf5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbaf5-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbaf5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fbaf5-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbaf5-128">Windows XP \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fbaf5-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbaf5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fbaf5-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbaf5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fbaf5-131">Fin de la prise en charge</span><span class="sxs-lookup"><span data-stu-id="fbaf5-131">End of support</span></span><br/> | <span data-ttu-id="fbaf5-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbaf5-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fbaf5-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fbaf5-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="fbaf5-134"><dt>Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbaf5-134"><dt>Cryptui.lib</dt></span></span> </dl>      |
| <span data-ttu-id="fbaf5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fbaf5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbaf5-136"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbaf5-136"><dt>Cryptui.dll</dt></span></span> </dl>      |
| <span data-ttu-id="fbaf5-137">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="fbaf5-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fbaf5-138">**CryptUIDlgViewSignerInfoW** (Unicode) et **CryptUIDlgViewSignerInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fbaf5-138">**CryptUIDlgViewSignerInfoW** (Unicode) and **CryptUIDlgViewSignerInfoA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbaf5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbaf5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbaf5-140">**\_VIEWSIGNERINFO, \_ struct**</span><span class="sxs-lookup"><span data-stu-id="fbaf5-140">**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**</span></span>](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
