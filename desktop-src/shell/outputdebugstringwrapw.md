---
description: Envoie une chaîne Unicode au débogueur pour l’affichage.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: OutputDebugStringWrapW, fonction (Shlwapip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991633"
---
# <a name="outputdebugstringwrapw-function"></a><span data-ttu-id="71275-103">OutputDebugStringWrapW fonction)</span><span class="sxs-lookup"><span data-stu-id="71275-103">OutputDebugStringWrapW function</span></span>

<span data-ttu-id="71275-104">\[Cette fonction peut être utilisée dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="71275-104">\[This function is available for use in Windows XP.</span></span> <span data-ttu-id="71275-105">Elle n’est peut-être pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="71275-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="71275-106">Utilisez [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="71275-106">Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in its place.\]</span></span>

<span data-ttu-id="71275-107">Envoie une chaîne Unicode au débogueur pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="71275-107">Sends a Unicode string to the debugger for display.</span></span>

> [!Note]  
> <span data-ttu-id="71275-108">**OutputDebugStringWrapW** est un wrapper pour la fonction **OutputDebugStringW** .</span><span class="sxs-lookup"><span data-stu-id="71275-108">**OutputDebugStringWrapW** is a wrapper for the **OutputDebugStringW** function.</span></span> <span data-ttu-id="71275-109">Pour plus d’informations sur les remarques d’utilisation, consultez la page [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) .</span><span class="sxs-lookup"><span data-stu-id="71275-109">See the [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="71275-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71275-110">Syntax</span></span>


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a><span data-ttu-id="71275-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71275-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71275-112">*lpOutputString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71275-112">*lpOutputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71275-113">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="71275-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="71275-114">Pointeur vers la chaîne Unicode terminée par le caractère null à afficher.</span><span class="sxs-lookup"><span data-stu-id="71275-114">A pointer to the null-terminated Unicode string to be displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71275-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71275-115">Return value</span></span>

<span data-ttu-id="71275-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="71275-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71275-117">Notes</span><span class="sxs-lookup"><span data-stu-id="71275-117">Remarks</span></span>

<span data-ttu-id="71275-118">**OutputDebugStringWrapW** offre la possibilité d’utiliser des chaînes Unicode dans les systèmes d’exploitation antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="71275-118">**OutputDebugStringWrapW** provides the ability to use Unicode strings in operating systems prior to Windows XP.</span></span> <span data-ttu-id="71275-119">La méthode recommandée consiste à utiliser [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) conjointement avec la couche Microsoft pour Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="71275-119">The preferred method is to use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="71275-120">**OutputDebugStringWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 115.</span><span class="sxs-lookup"><span data-stu-id="71275-120">**OutputDebugStringWrapW** must be called directly from Shlwapi.dll, using ordinal 115.</span></span>

<span data-ttu-id="71275-121">Si l’application n’a pas de débogueur, le débogueur système affiche la chaîne.</span><span class="sxs-lookup"><span data-stu-id="71275-121">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="71275-122">Si l’application n’a pas de débogueur et que le débogueur système n’est pas actif, **OutputDebugStringWrapW** ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="71275-122">If the application has no debugger and the system debugger is not active, **OutputDebugStringWrapW** does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="71275-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="71275-123">Requirements</span></span>



| <span data-ttu-id="71275-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71275-124">Requirement</span></span> | <span data-ttu-id="71275-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="71275-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71275-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71275-126">Minimum supported client</span></span><br/> | <span data-ttu-id="71275-127">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71275-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71275-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71275-128">Minimum supported server</span></span><br/> | <span data-ttu-id="71275-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71275-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="71275-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="71275-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="71275-131"><dt>Shlwapip. h</dt></span><span class="sxs-lookup"><span data-stu-id="71275-131"><dt>Shlwapip.h</dt></span></span> </dl>                         |
| <span data-ttu-id="71275-132">DLL</span><span class="sxs-lookup"><span data-stu-id="71275-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71275-133"><dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="71275-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71275-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71275-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71275-135">**OutputDebugString**</span><span class="sxs-lookup"><span data-stu-id="71275-135">**OutputDebugString**</span></span>](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
