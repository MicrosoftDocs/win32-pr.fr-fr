---
description: Convertit les caractères minuscules d’une mémoire tampon en caractères majuscules.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: CharUpperBuffWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: dacc5e7609ca7f91bf7c66651d7ba9bdd11ab688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525396"
---
# <a name="charupperbuffwrapw-function"></a><span data-ttu-id="ba43d-103">CharUpperBuffWrapW fonction)</span><span class="sxs-lookup"><span data-stu-id="ba43d-103">CharUpperBuffWrapW function</span></span>

<span data-ttu-id="ba43d-104">\[**CharUpperBuffWrapW** peut être utilisé dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ba43d-104">\[**CharUpperBuffWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="ba43d-105">Elle n’est peut-être pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ba43d-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="ba43d-106">Vous devez utiliser [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="ba43d-106">You should use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in its place.\]</span></span>

<span data-ttu-id="ba43d-107">Convertit les caractères minuscules d’une mémoire tampon en caractères majuscules.</span><span class="sxs-lookup"><span data-stu-id="ba43d-107">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="ba43d-108">La fonction convertit les caractères sur place.</span><span class="sxs-lookup"><span data-stu-id="ba43d-108">The function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="ba43d-109">**CharUpperBuffWrapW** est un wrapper pour la fonction **CharUpperBuffW** .</span><span class="sxs-lookup"><span data-stu-id="ba43d-109">**CharUpperBuffWrapW** is a wrapper for the **CharUpperBuffW** function.</span></span> <span data-ttu-id="ba43d-110">Pour plus d’informations sur les remarques d’utilisation, consultez la page [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) .</span><span class="sxs-lookup"><span data-stu-id="ba43d-110">See the [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ba43d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba43d-111">Syntax</span></span>


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a><span data-ttu-id="ba43d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba43d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba43d-113">*PCH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba43d-113">*pch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba43d-114">Type : **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="ba43d-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="ba43d-115">Pointeur vers une mémoire tampon qui contient un ou plusieurs caractères Unicode à traiter.</span><span class="sxs-lookup"><span data-stu-id="ba43d-115">A pointer to a buffer that contains one or more Unicode characters to process.</span></span>

</dd> <dt>

<span data-ttu-id="ba43d-116">*cchLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba43d-116">*cchLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba43d-117">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ba43d-117">Type: **DWORD**</span></span>

<span data-ttu-id="ba43d-118">Spécifie la taille, en caractères, de la mémoire tampon vers laquelle pointe *PCH*.</span><span class="sxs-lookup"><span data-stu-id="ba43d-118">Specifies the size, in characters, of the buffer pointed to by *pch*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba43d-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba43d-119">Return value</span></span>

<span data-ttu-id="ba43d-120">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ba43d-120">Type: **DWORD**</span></span>

<span data-ttu-id="ba43d-121">Nombre de caractères traités.</span><span class="sxs-lookup"><span data-stu-id="ba43d-121">The number of characters processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba43d-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ba43d-122">Remarks</span></span>

<span data-ttu-id="ba43d-123">La méthode recommandée consiste à utiliser [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) conjointement avec la couche Microsoft pour Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="ba43d-123">The preferred method is to use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="ba43d-124">**CharUpperBuffWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 44.</span><span class="sxs-lookup"><span data-stu-id="ba43d-124">**CharUpperBuffWrapW** must be called directly from Shlwapi.dll, using ordinal 44.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba43d-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ba43d-125">Requirements</span></span>



| <span data-ttu-id="ba43d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba43d-126">Requirement</span></span> | <span data-ttu-id="ba43d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba43d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba43d-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba43d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ba43d-129">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba43d-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba43d-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba43d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ba43d-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba43d-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ba43d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ba43d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba43d-133"><dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="ba43d-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba43d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba43d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba43d-135">**CharUpperBuff**</span><span class="sxs-lookup"><span data-stu-id="ba43d-135">**CharUpperBuff**</span></span>](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
