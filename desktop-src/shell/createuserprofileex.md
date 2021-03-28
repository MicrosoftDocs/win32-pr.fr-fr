---
description: Crée un profil utilisateur pour un utilisateur spécifié.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: CreateUserProfileEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982946"
---
# <a name="createuserprofileex-function"></a><span data-ttu-id="9c0db-103">CreateUserProfileEx fonction)</span><span class="sxs-lookup"><span data-stu-id="9c0db-103">CreateUserProfileEx function</span></span>

<span data-ttu-id="9c0db-104">\[Cette fonction n’est pas disponible à partir de Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="9c0db-104">\[This function is not available as of Windows Vista.\]</span></span>

<span data-ttu-id="9c0db-105">Crée un profil utilisateur pour un utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="9c0db-105">Creates a user profile for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c0db-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c0db-106">Syntax</span></span>


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a><span data-ttu-id="9c0db-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c0db-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c0db-108">*pSid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c0db-108">*pSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0db-109">Type : **PSID**</span><span class="sxs-lookup"><span data-stu-id="9c0db-109">Type: **PSID**</span></span>

<span data-ttu-id="9c0db-110">SID du nouvel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9c0db-110">The SID of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="9c0db-111">*lpUserName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c0db-111">*lpUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0db-112">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="9c0db-112">Type: **LPCTSTR**</span></span>

<span data-ttu-id="9c0db-113">Pointeur vers une mémoire tampon qui contient le nom d’utilisateur du nouvel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9c0db-113">Pointer to a buffer that contains the user name of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="9c0db-114">*lpUserHive* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9c0db-114">*lpUserHive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0db-115">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="9c0db-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="9c0db-116">Pointeur vers une mémoire tampon qui contient la [ruche de Registre](../sysinfo/registry-hives.md) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9c0db-116">Pointer to a buffer that contains the [registry hive](../sysinfo/registry-hives.md) to use.</span></span> <span data-ttu-id="9c0db-117">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9c0db-117">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9c0db-118">*lpProfileDir* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9c0db-118">*lpProfileDir* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0db-119">Type : **LPTStr**</span><span class="sxs-lookup"><span data-stu-id="9c0db-119">Type: **LPTSTR**</span></span>

<span data-ttu-id="9c0db-120">Pointeur vers une mémoire tampon qui, lorsque cette fonction est retournée, reçoit le chemin d’accès au répertoire de profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9c0db-120">Pointer to a buffer that, when this function returns, receives the user's profile directory path.</span></span> <span data-ttu-id="9c0db-121">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9c0db-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9c0db-122">*dwDirSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c0db-122">*dwDirSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0db-123">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9c0db-123">Type: **DWORD**</span></span>

<span data-ttu-id="9c0db-124">Taille de la mémoire tampon spécifiée par *lpProfileDir*, dans TCHARs.</span><span class="sxs-lookup"><span data-stu-id="9c0db-124">Size of the buffer specified by *lpProfileDir*, in TCHARs.</span></span>

</dd> <dt>

<span data-ttu-id="9c0db-125">*bWin9xUpg* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c0db-125">*bWin9xUpg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0db-126">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="9c0db-126">Type: **BOOL**</span></span>

<span data-ttu-id="9c0db-127">**True** si le profil utilisateur est créé dans le cadre d’une migration de profil à partir de Windows 9x ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="9c0db-127">**TRUE** if the user profile is being created as part of a profile migration from Windows 9x; otherwise, **FALSE**.</span></span>

<span data-ttu-id="9c0db-128">Si la **valeur est true**, le profil utilisateur est configuré dans le répertoire de profil par défaut (normalement C : \\ Documents and Settings \\ *username*).</span><span class="sxs-lookup"><span data-stu-id="9c0db-128">When **TRUE**, the user profile is set up in the default profile directory—normally C:\\Documents and Settings\\*UserName*.</span></span> <span data-ttu-id="9c0db-129">Si ce répertoire existe déjà, il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="9c0db-129">If that directory already exists, it is used.</span></span> <span data-ttu-id="9c0db-130">Si ce n’est pas le cas, il est créé.</span><span class="sxs-lookup"><span data-stu-id="9c0db-130">If it does not, it is created.</span></span>

<span data-ttu-id="9c0db-131">Si la **valeur est false**, le répertoire de profil par défaut est créé s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="9c0db-131">If **FALSE**, the default profile directory is created if it does not exist.</span></span> <span data-ttu-id="9c0db-132">Si le répertoire de profil par défaut existe déjà, un nouveau répertoire est créé pour ce profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9c0db-132">If the default profile directory already exists, a new directory is created for this user profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c0db-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c0db-133">Return value</span></span>

<span data-ttu-id="9c0db-134">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="9c0db-134">Type: **BOOL**</span></span>

<span data-ttu-id="9c0db-135">Retourne la **valeur true** si le nouveau profil utilisateur a été créé avec succès ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="9c0db-135">Returns **TRUE** if the new user profile was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c0db-136">Notes</span><span class="sxs-lookup"><span data-stu-id="9c0db-136">Remarks</span></span>

<span data-ttu-id="9c0db-137">Cette fonction n’est pas déclarée dans les en-têtes du kit de développement logiciel (SDK) et n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="9c0db-137">This function is not declared in the software development kit (SDK) headers and has no associated import library.</span></span> <span data-ttu-id="9c0db-138">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison à Userenv.dll.</span><span class="sxs-lookup"><span data-stu-id="9c0db-138">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to link to Userenv.dll.</span></span> <span data-ttu-id="9c0db-139">La version ANSI de la fonction, **CreateUserProfileExA** est référencée à partir de Userenv.dll en tant qu’ordinal 153.</span><span class="sxs-lookup"><span data-stu-id="9c0db-139">The ANSI version of the function, **CreateUserProfileExA** is referenced from Userenv.dll as ordinal 153.</span></span> <span data-ttu-id="9c0db-140">La version Unicode, **CreateUserProfileExW** est référencée sous la forme ordinale 154.</span><span class="sxs-lookup"><span data-stu-id="9c0db-140">The Unicode version, **CreateUserProfileExW** is referenced as ordinal 154.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c0db-141">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9c0db-141">Requirements</span></span>



| <span data-ttu-id="9c0db-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c0db-142">Requirement</span></span> | <span data-ttu-id="9c0db-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c0db-143">Value</span></span> |
|-----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0db-144">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9c0db-144">End of client support</span></span><br/>  | <span data-ttu-id="9c0db-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c0db-145">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="9c0db-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9c0db-146">DLL</span></span><br/>                    | <dl> <span data-ttu-id="9c0db-147"><dt>Userenv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c0db-147"><dt>Userenv.dll</dt></span></span> </dl> |
| <span data-ttu-id="9c0db-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="9c0db-148">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="9c0db-149">**CreateUserProfileExW** (Unicode) et **CreateUserProfileExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9c0db-149">**CreateUserProfileExW** (Unicode) and **CreateUserProfileExA** (ANSI)</span></span><br/>      |



 

 
