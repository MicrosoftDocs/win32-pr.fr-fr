---
description: Détermine l’emplacement d’une ressource avec le type et le nom spécifiés, dans le module spécifié.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: FindResourceWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202796"
---
# <a name="findresourcewrapw-function"></a><span data-ttu-id="e4027-103">FindResourceWrapW fonction)</span><span class="sxs-lookup"><span data-stu-id="e4027-103">FindResourceWrapW function</span></span>

<span data-ttu-id="e4027-104">\[**FindResourceWrapW** peut être utilisé dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e4027-104">\[**FindResourceWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="e4027-105">Elle n’est peut-être pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e4027-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="e4027-106">Vous devez utiliser [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="e4027-106">You should use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) instead.\]</span></span>

<span data-ttu-id="e4027-107">Détermine l’emplacement d’une ressource avec le type et le nom spécifiés, dans le module spécifié.</span><span class="sxs-lookup"><span data-stu-id="e4027-107">Determines the location of a resource with the specified type and name, in the specified module.</span></span>

> [!Note]  
> <span data-ttu-id="e4027-108">**FindResourceWrapW** est un wrapper pour la fonction **FindResourceW** .</span><span class="sxs-lookup"><span data-stu-id="e4027-108">**FindResourceWrapW** is a wrapper for the **FindResourceW** function.</span></span> <span data-ttu-id="e4027-109">Pour plus d’informations sur l’utilisation, consultez [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) .</span><span class="sxs-lookup"><span data-stu-id="e4027-109">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e4027-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4027-110">Syntax</span></span>


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a><span data-ttu-id="e4027-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4027-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4027-112">*HMODULE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4027-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4027-113">Type : **HMODULE**</span><span class="sxs-lookup"><span data-stu-id="e4027-113">Type: **HMODULE**</span></span>

<span data-ttu-id="e4027-114">Handle du module dont le fichier exécutable contient la ressource.</span><span class="sxs-lookup"><span data-stu-id="e4027-114">A handle to the module whose executable file contains the resource.</span></span> <span data-ttu-id="e4027-115">La valeur **null** spécifie le descripteur de module associé au fichier image utilisé par le système d’exploitation pour créer le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="e4027-115">A value of **NULL** specifies the module handle associated with the image file that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="e4027-116">*lpName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4027-116">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4027-117">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e4027-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="e4027-118">Nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="e4027-118">The name of the resource.</span></span> <span data-ttu-id="e4027-119">Pour plus d’informations, consultez [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="e4027-119">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="e4027-120">*lpType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4027-120">*lpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4027-121">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e4027-121">Type: **LPCWSTR**</span></span>

<span data-ttu-id="e4027-122">Pointeur vers une chaîne qui spécifie le type de ressource.</span><span class="sxs-lookup"><span data-stu-id="e4027-122">A pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="e4027-123">Pour plus d’informations, consultez [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="e4027-123">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4027-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4027-124">Return value</span></span>

<span data-ttu-id="e4027-125">Type : **HRSRC**</span><span class="sxs-lookup"><span data-stu-id="e4027-125">Type: **HRSRC**</span></span>

<span data-ttu-id="e4027-126">Si la fonction est réussie, la valeur de retour est un handle vers le bloc d’informations de la ressource spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e4027-126">If the function succeeds, the return value is a handle to the specified resource's information block.</span></span> <span data-ttu-id="e4027-127">Pour obtenir un descripteur de la ressource, transmettez ce handle à la fonction [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .</span><span class="sxs-lookup"><span data-stu-id="e4027-127">To obtain a handle to the resource, pass this handle to the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

<span data-ttu-id="e4027-128">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="e4027-128">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="e4027-129">Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="e4027-129">To get extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4027-130">Notes</span><span class="sxs-lookup"><span data-stu-id="e4027-130">Remarks</span></span>

<span data-ttu-id="e4027-131">Si vous devez spécifier une localisation particulière, utilisez la fonction [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) au lieu de **FindResourceWrapW**.</span><span class="sxs-lookup"><span data-stu-id="e4027-131">If you need to specify a particular localization, use the [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) function rather than **FindResourceWrapW**.</span></span>

<span data-ttu-id="e4027-132">**FindResourceWrapW** offre la possibilité d’utiliser des chaînes Unicode dans les systèmes d’exploitation plus anciens.</span><span class="sxs-lookup"><span data-stu-id="e4027-132">**FindResourceWrapW** provides the ability to use Unicode strings in older operating systems.</span></span> <span data-ttu-id="e4027-133">La méthode recommandée consiste à utiliser [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) conjointement avec la couche Microsoft pour Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="e4027-133">The preferred method is to use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="e4027-134">**FindResourceWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 66.</span><span class="sxs-lookup"><span data-stu-id="e4027-134">**FindResourceWrapW** must be called directly from Shlwapi.dll, using ordinal 66.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4027-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e4027-135">Requirements</span></span>



| <span data-ttu-id="e4027-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4027-136">Requirement</span></span> | <span data-ttu-id="e4027-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4027-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4027-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4027-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e4027-139">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4027-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4027-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4027-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e4027-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4027-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e4027-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4027-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4027-143"><dt>Aucun</dt></span><span class="sxs-lookup"><span data-stu-id="e4027-143"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="e4027-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e4027-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4027-145"><dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e4027-145"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="e4027-146">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e4027-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e4027-147">**FindResourceWrapW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="e4027-147">**FindResourceWrapW** (Unicode)</span></span><br/>                                                                    |



## <a name="see-also"></a><span data-ttu-id="e4027-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4027-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4027-149">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="e4027-149">**FindResource**</span></span>](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
