---
description: Récupère des informations sur l’espace utilisé par le cache Fichiers hors connexion.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: CSCGetSpaceUsageW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541672"
---
# <a name="cscgetspaceusagew-function"></a><span data-ttu-id="ba867-103">CSCGetSpaceUsageW fonction)</span><span class="sxs-lookup"><span data-stu-id="ba867-103">CSCGetSpaceUsageW function</span></span>

<span data-ttu-id="ba867-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]</span><span class="sxs-lookup"><span data-stu-id="ba867-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="ba867-105">Récupère des informations sur l’espace utilisé par le cache Fichiers hors connexion.</span><span class="sxs-lookup"><span data-stu-id="ba867-105">Retrieves information about the space used by the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba867-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba867-106">Syntax</span></span>


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a><span data-ttu-id="ba867-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba867-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba867-108">*lptzLocation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ba867-108">*lptzLocation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba867-109">Emplacement du répertoire du cache.</span><span class="sxs-lookup"><span data-stu-id="ba867-109">The directory location of the cache.</span></span>

</dd> <dt>

<span data-ttu-id="ba867-110">*dwSize nul* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba867-110">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba867-111">Taille de la mémoire tampon *lptzLocation* , en caractères.</span><span class="sxs-lookup"><span data-stu-id="ba867-111">The size of the *lptzLocation* buffer, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="ba867-112">*lpdwMaxSpaceHigh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ba867-112">*lpdwMaxSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba867-113">**Valeur DWORD** de poids fort du nombre maximal d’octets disponibles dans le cache.</span><span class="sxs-lookup"><span data-stu-id="ba867-113">The high-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="ba867-114">*lpdwMaxSpaceLow* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ba867-114">*lpdwMaxSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba867-115">**DWORD** de poids faible du nombre maximal d’octets disponibles dans le cache.</span><span class="sxs-lookup"><span data-stu-id="ba867-115">The low-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="ba867-116">*lpdwCurrentSpaceHigh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ba867-116">*lpdwCurrentSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba867-117">**Valeur DWORD** de poids fort du nombre actuel d’octets disponibles dans le cache.</span><span class="sxs-lookup"><span data-stu-id="ba867-117">The high-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="ba867-118">*lpdwCurrentSpaceLow* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ba867-118">*lpdwCurrentSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba867-119">**DWORD** de poids faible du nombre actuel d’octets disponibles dans le cache.</span><span class="sxs-lookup"><span data-stu-id="ba867-119">The low-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="ba867-120">*lpcntTotalFiles* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ba867-120">*lpcntTotalFiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba867-121">Nombre total de fichiers dans le cache.</span><span class="sxs-lookup"><span data-stu-id="ba867-121">The total number of files in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="ba867-122">*lpcntTotalDirs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ba867-122">*lpcntTotalDirs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba867-123">Nombre total de répertoires dans le cache.</span><span class="sxs-lookup"><span data-stu-id="ba867-123">The total number of directories in the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba867-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba867-124">Return value</span></span>

<span data-ttu-id="ba867-125">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="ba867-125">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba867-126">Notes</span><span class="sxs-lookup"><span data-stu-id="ba867-126">Remarks</span></span>

<span data-ttu-id="ba867-127">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ba867-127">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba867-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba867-128">Requirements</span></span>



| <span data-ttu-id="ba867-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba867-129">Requirement</span></span> | <span data-ttu-id="ba867-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba867-130">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba867-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ba867-131">DLL</span></span><br/> | <dl> <span data-ttu-id="ba867-132"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba867-132"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
