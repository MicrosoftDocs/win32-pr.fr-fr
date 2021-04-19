---
description: Détermine si une chaîne Unicode correspond au modèle spécifié.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: RtlIsNameInExpression fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516772"
---
# <a name="rtlisnameinexpression-function"></a><span data-ttu-id="6b5e1-103">RtlIsNameInExpression fonction)</span><span class="sxs-lookup"><span data-stu-id="6b5e1-103">RtlIsNameInExpression function</span></span>

<span data-ttu-id="6b5e1-104">Détermine si une chaîne Unicode correspond au modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-104">Determines whether a Unicode string matches the specified pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b5e1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b5e1-105">Syntax</span></span>


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a><span data-ttu-id="6b5e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b5e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b5e1-107">*Expression* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b5e1-107">*Expression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5e1-108">Pointeur vers la chaîne du modèle.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-108">A pointer to the pattern string.</span></span> <span data-ttu-id="6b5e1-109">Cette chaîne peut contenir des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-109">This string can contain wildcard characters.</span></span> <span data-ttu-id="6b5e1-110">Si le paramètre *ignoreCase* a la valeur true, la chaîne ne doit contenir que des caractères majuscules.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-110">If the *IgnoreCase* parameter is TRUE, the string must contain only uppercase characters.</span></span>

</dd> <dt>

<span data-ttu-id="6b5e1-111">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b5e1-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5e1-112">Pointeur vers la chaîne à comparer au modèle.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-112">A pointer to the string to be compared against the pattern.</span></span> <span data-ttu-id="6b5e1-113">Cette chaîne ne peut pas contenir de caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-113">This string cannot contain wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="6b5e1-114">*IgnoreCase* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b5e1-114">*IgnoreCase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5e1-115">**True** pour une correspondance qui ne respecte pas la casse, ou **false** pour la correspondance respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-115">**TRUE** for case-insensitive matching, or **FALSE** for case-sensitive matching.</span></span>

</dd> <dt>

<span data-ttu-id="6b5e1-116">*UpcaseTable* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6b5e1-116">*UpcaseTable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5e1-117">Pointeur facultatif vers une table de caractères en majuscules à utiliser pour la correspondance qui ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-117">An optional pointer to an uppercase character table to use for case-insensitive matching.</span></span> <span data-ttu-id="6b5e1-118">Si ce paramètre a la valeur NULL, la table de caractères majuscules du système par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-118">If this parameter is NULL, the default system uppercase character table is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b5e1-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b5e1-119">Return value</span></span>

<span data-ttu-id="6b5e1-120">Retourne la **valeur true** si la chaîne correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-120">Returns **TRUE** if the string matches the pattern.</span></span> <span data-ttu-id="6b5e1-121">Si la chaîne ne correspond pas au modèle, cette fonction retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-121">If the string does not match the pattern, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b5e1-122">Notes</span><span class="sxs-lookup"><span data-stu-id="6b5e1-122">Remarks</span></span>

<span data-ttu-id="6b5e1-123">Cette fonction n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-123">This function has no associated header file.</span></span> <span data-ttu-id="6b5e1-124">La bibliothèque d’importation associée, ntdll. lib, est disponible dans Microsoft Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="6b5e1-124">The associated import library, Ntdll.lib, is available in the Microsoft Windows Driver Kit (WDK).</span></span> <span data-ttu-id="6b5e1-125">Vous pouvez également appeler cette fonction à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="6b5e1-125">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b5e1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b5e1-126">Requirements</span></span>



| <span data-ttu-id="6b5e1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b5e1-127">Requirement</span></span> | <span data-ttu-id="6b5e1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b5e1-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6b5e1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b5e1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6b5e1-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b5e1-130">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6b5e1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b5e1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6b5e1-132">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b5e1-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6b5e1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6b5e1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b5e1-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b5e1-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
