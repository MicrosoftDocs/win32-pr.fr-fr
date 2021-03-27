---
description: Détermine si un caractère est un caractère alphabétique ou numérique.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: IsCharAlphaNumericWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972434"
---
# <a name="ischaralphanumericwrapw-function"></a><span data-ttu-id="5e2f4-103">IsCharAlphaNumericWrapW fonction)</span><span class="sxs-lookup"><span data-stu-id="5e2f4-103">IsCharAlphaNumericWrapW function</span></span>

<span data-ttu-id="5e2f4-104">\[**IsCharAlphaNumericWrapW** peut être utilisé dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5e2f4-104">\[**IsCharAlphaNumericWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="5e2f4-105">Elle ne sera pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5e2f4-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="5e2f4-106">Vous devez utiliser [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="5e2f4-106">You should use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in its place.\]</span></span>

<span data-ttu-id="5e2f4-107">Détermine si un caractère est un caractère alphabétique ou numérique.</span><span class="sxs-lookup"><span data-stu-id="5e2f4-107">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="5e2f4-108">Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="5e2f4-108">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span>

> [!Note]  
> <span data-ttu-id="5e2f4-109">**IsCharAlphaNumericWrapW** est un wrapper pour la fonction **IsCharAlphaNumericW** .</span><span class="sxs-lookup"><span data-stu-id="5e2f4-109">**IsCharAlphaNumericWrapW** is a wrapper for the **IsCharAlphaNumericW** function.</span></span> <span data-ttu-id="5e2f4-110">Pour plus d’informations sur les remarques d’utilisation, consultez la page [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) .</span><span class="sxs-lookup"><span data-stu-id="5e2f4-110">See the [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5e2f4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e2f4-111">Syntax</span></span>


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a><span data-ttu-id="5e2f4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e2f4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e2f4-113">*ch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e2f4-113">*ch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e2f4-114">Type : **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="5e2f4-114">Type: **WCHAR**</span></span>

<span data-ttu-id="5e2f4-115">Caractère Unicode à tester.</span><span class="sxs-lookup"><span data-stu-id="5e2f4-115">The Unicode character to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e2f4-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e2f4-116">Return value</span></span>

<span data-ttu-id="5e2f4-117">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="5e2f4-117">Type: **BOOL**</span></span>

<span data-ttu-id="5e2f4-118">Si le caractère est alphanumérique, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="5e2f4-118">If the character is alphanumeric, the return value is nonzero.</span></span>

<span data-ttu-id="5e2f4-119">Si le caractère n’est pas alphanumérique, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="5e2f4-119">If the character is not alphanumeric, the return value is zero.</span></span> <span data-ttu-id="5e2f4-120">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="5e2f4-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e2f4-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e2f4-121">Remarks</span></span>

<span data-ttu-id="5e2f4-122">**IsCharAlphaNumericWrapW** offre la possibilité d’utiliser des chaînes Unicode dans des systèmes d’exploitation antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5e2f4-122">**IsCharAlphaNumericWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="5e2f4-123">La méthode recommandée consiste à utiliser [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) conjointement avec la couche Microsoft pour Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="5e2f4-123">The preferred method is to use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="5e2f4-124">**IsCharAlphaNumericWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 28.</span><span class="sxs-lookup"><span data-stu-id="5e2f4-124">**IsCharAlphaNumericWrapW** must be called directly from Shlwapi.dll, using ordinal 28.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e2f4-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5e2f4-125">Requirements</span></span>



| <span data-ttu-id="5e2f4-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e2f4-126">Requirement</span></span> | <span data-ttu-id="5e2f4-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e2f4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2f4-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e2f4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5e2f4-129">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e2f4-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e2f4-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e2f4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5e2f4-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e2f4-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5e2f4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5e2f4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e2f4-133"><dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="5e2f4-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e2f4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e2f4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e2f4-135">**IsCharAlphaNumeric**</span><span class="sxs-lookup"><span data-stu-id="5e2f4-135">**IsCharAlphaNumeric**</span></span>](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
