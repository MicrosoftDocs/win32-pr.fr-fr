---
description: Poursuit une opération de recherche de fichiers.
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: CSCFindNextFileW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindNextFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 50b387a1ff99a95fcbe0fae8fe8ad93d14c335b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533333"
---
# <a name="cscfindnextfilew-function"></a><span data-ttu-id="dbd4e-103">CSCFindNextFileW fonction)</span><span class="sxs-lookup"><span data-stu-id="dbd4e-103">CSCFindNextFileW function</span></span>

<span data-ttu-id="dbd4e-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]</span><span class="sxs-lookup"><span data-stu-id="dbd4e-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="dbd4e-105">Poursuit une opération de recherche de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-105">Continues a file search operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbd4e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbd4e-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindNextFileW(
  _In_  HANDLE           hFind,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _In_  FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="dbd4e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbd4e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbd4e-108">*hFind* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dbd4e-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd4e-109">Un handle de recherche retourné par la fonction [**CSCFindFirstFileW**](cscfindfirstfilew.md) .</span><span class="sxs-lookup"><span data-stu-id="dbd4e-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="dbd4e-110">*lpFind32* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dbd4e-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd4e-111">Pointeur vers la structure [**de \_ \_ données de recherche Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) qui reçoit des informations sur le fichier ou le sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="dbd4e-112">*lpdwStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dbd4e-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd4e-113">Code NTSTATUS qui indique l’état de l’appel.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="dbd4e-114">*lpdwPinCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dbd4e-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd4e-115">Ce paramètre est différent de zéro si le fichier a été rendu disponible hors connexion ou 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="dbd4e-116">*lpdwHintFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dbd4e-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd4e-117">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="dbd4e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbd4e-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="dbd4e-119">Signification</span><span class="sxs-lookup"><span data-stu-id="dbd4e-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="dbd4e-120"><dt>**Indicateur \_ \_ \_ Code confidentiel \_ d’indicateur CSC utilisateur**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="dbd4e-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="dbd4e-121">Un utilisateur a rendu le fichier disponible hors connexion.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="dbd4e-122"><dt>**Indicateur \_ \_Code pin d’indicateur CSC \_ \_ inherit \_ User**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="dbd4e-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="dbd4e-123">Un utilisateur a rendu le parent disponible hors connexion et marqué le parent de sorte que ses enfants soient disponibles hors connexion.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="dbd4e-124"><dt>**Indicateur \_ \_Code PIN de l’indicateur CSC \_ \_ inherit \_ System**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="dbd4e-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="dbd4e-125">Un administrateur ou une stratégie de groupe a rendu le parent disponible hors connexion et marqué le parent de telle sorte que ses enfants soient disponibles hors connexion.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="dbd4e-126"><dt>**Indicateur \_ \_Système de \_ pin \_ d’indicateur CSC**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="dbd4e-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="dbd4e-127">Un administrateur ou une stratégie de groupe a rendu le fichier disponible hors connexion.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="dbd4e-128">*lpOrgFileTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dbd4e-128">*lpOrgFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd4e-129">Pointeur vers une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) pour recevoir les informations de date et d’heure du fichier ou du sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbd4e-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbd4e-130">Return value</span></span>

<span data-ttu-id="dbd4e-131">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="dbd4e-131">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbd4e-132">Notes</span><span class="sxs-lookup"><span data-stu-id="dbd4e-132">Remarks</span></span>

<span data-ttu-id="dbd4e-133">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="dbd4e-133">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbd4e-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbd4e-134">Requirements</span></span>



| <span data-ttu-id="dbd4e-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbd4e-135">Requirement</span></span> | <span data-ttu-id="dbd4e-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbd4e-136">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbd4e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dbd4e-137">DLL</span></span><br/> | <dl> <span data-ttu-id="dbd4e-138"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbd4e-138"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
