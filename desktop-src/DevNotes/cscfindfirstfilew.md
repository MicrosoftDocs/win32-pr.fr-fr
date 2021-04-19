---
description: Recherche un fichier dans le cache de Fichiers hors connexion qui répond aux critères spécifiés.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: CSCFindFirstFileW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: f8cad9caf78b44f40a4126307db6deb0f71dfd1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527329"
---
# <a name="cscfindfirstfilew-function"></a><span data-ttu-id="3ba36-103">CSCFindFirstFileW fonction)</span><span class="sxs-lookup"><span data-stu-id="3ba36-103">CSCFindFirstFileW function</span></span>

<span data-ttu-id="3ba36-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]</span><span class="sxs-lookup"><span data-stu-id="3ba36-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="3ba36-105">Recherche un fichier dans le cache de Fichiers hors connexion qui répond aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3ba36-105">Searches for a file in the Offline Files cache that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba36-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ba36-106">Syntax</span></span>


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="3ba36-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ba36-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ba36-108">*lpszFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3ba36-108">*lpszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba36-109">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un répertoire UNC ou un chemin d’accès valide.</span><span class="sxs-lookup"><span data-stu-id="3ba36-109">A pointer to a null-terminated string that specifies a valid UNC directory or path.</span></span>

</dd> <dt>

<span data-ttu-id="3ba36-110">*lpFind32* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ba36-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba36-111">Pointeur vers la structure [**de \_ \_ données de recherche Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) qui reçoit des informations sur le fichier ou le sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="3ba36-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="3ba36-112">*lpdwStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ba36-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba36-113">Code NTSTATUS qui indique l’état de l’appel.</span><span class="sxs-lookup"><span data-stu-id="3ba36-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="3ba36-114">*lpdwPinCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ba36-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba36-115">Ce paramètre est différent de zéro si le fichier a été rendu disponible hors connexion ou 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3ba36-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="3ba36-116">*lpdwHintFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ba36-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba36-117">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ba36-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3ba36-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ba36-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="3ba36-119">Signification</span><span class="sxs-lookup"><span data-stu-id="3ba36-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="3ba36-120"><dt>**Indicateur \_ \_ \_ Code confidentiel \_ d’indicateur CSC utilisateur**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="3ba36-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="3ba36-121">Un utilisateur a rendu le fichier disponible hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3ba36-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="3ba36-122"><dt>**Indicateur \_ \_Code pin d’indicateur CSC \_ \_ inherit \_ User**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="3ba36-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="3ba36-123">Un utilisateur a rendu le parent disponible hors connexion et marqué le parent de sorte que ses enfants soient disponibles hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3ba36-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="3ba36-124"><dt>**Indicateur \_ \_Code PIN de l’indicateur CSC \_ \_ inherit \_ System**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="3ba36-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="3ba36-125">Un administrateur ou une stratégie de groupe a rendu le parent disponible hors connexion et marqué le parent de telle sorte que ses enfants soient disponibles hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3ba36-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="3ba36-126"><dt>**Indicateur \_ \_Système de \_ pin \_ d’indicateur CSC**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="3ba36-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="3ba36-127">Un administrateur ou une stratégie de groupe a rendu le fichier disponible hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3ba36-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="3ba36-128">*lpOrgFileTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ba36-128">*lpOrgFileTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba36-129">Pointeur vers une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) pour recevoir les informations de date et d’heure du fichier ou du sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="3ba36-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ba36-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ba36-130">Return value</span></span>

<span data-ttu-id="3ba36-131">Si la fonction est réussie, la valeur de retour est un handle de recherche utilisé dans un appel ultérieur à [**CSCFindNextFileW**](cscfindnextfilew.md) ou [**CSCFindClose**](cscfindclose.md).</span><span class="sxs-lookup"><span data-stu-id="3ba36-131">If the function succeeds, the return value is a search handle used in a subsequent call to [**CSCFindNextFileW**](cscfindnextfilew.md) or [**CSCFindClose**](cscfindclose.md).</span></span>

<span data-ttu-id="3ba36-132">Si la fonction échoue, la valeur de retour est **INVALID\_HANDLE\_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="3ba36-132">If the function fails, the return value is **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba36-133">Notes</span><span class="sxs-lookup"><span data-stu-id="3ba36-133">Remarks</span></span>

<span data-ttu-id="3ba36-134">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3ba36-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba36-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ba36-135">Requirements</span></span>



| <span data-ttu-id="3ba36-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ba36-136">Requirement</span></span> | <span data-ttu-id="3ba36-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ba36-137">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba36-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3ba36-138">DLL</span></span><br/> | <dl> <span data-ttu-id="3ba36-139"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ba36-139"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
