---
description: Récupère des informations sur l’objet d’annuaire spécifié.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: NtQueryDirectoryObject fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528443"
---
# <a name="ntquerydirectoryobject-function"></a><span data-ttu-id="37902-103">NtQueryDirectoryObject fonction)</span><span class="sxs-lookup"><span data-stu-id="37902-103">NtQueryDirectoryObject function</span></span>

<span data-ttu-id="37902-104">\[Cette fonction peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="37902-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="37902-105">Récupère des informations sur l’objet d’annuaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="37902-105">Retrieves information about the specified directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="37902-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37902-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="37902-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37902-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37902-108">*DirectoryHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37902-108">*DirectoryHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37902-109">Handle de l’objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="37902-109">A handle to the directory object.</span></span>

</dd> <dt>

<span data-ttu-id="37902-110">*Mémoire tampon* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="37902-110">*Buffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37902-111">Pointeur vers une mémoire tampon qui reçoit les informations d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="37902-111">A pointer to a buffer that receives the directory information.</span></span> <span data-ttu-id="37902-112">Cette mémoire tampon reçoit une ou plusieurs structures d' **\_ \_ informations d’annuaire d’objets** , la dernière ayant la **valeur null**, suivie de chaînes qui contiennent les noms des entrées de répertoire.</span><span class="sxs-lookup"><span data-stu-id="37902-112">This buffer receives one or more **OBJECT\_DIRECTORY\_INFORMATION** structures, the last one being **NULL**, followed by strings that contain the names of the directory entries.</span></span> <span data-ttu-id="37902-113">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="37902-113">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="37902-114">*Longueur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37902-114">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37902-115">Taille de la mémoire tampon de sortie fournie par l’utilisateur, en octets.</span><span class="sxs-lookup"><span data-stu-id="37902-115">The size of the user-supplied output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="37902-116">*ReturnSingleEntry* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37902-116">*ReturnSingleEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37902-117">Indique si la fonction doit retourner une seule entrée.</span><span class="sxs-lookup"><span data-stu-id="37902-117">Indicates whether the function should return only a single entry.</span></span>

</dd> <dt>

<span data-ttu-id="37902-118">*RestartScan* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37902-118">*RestartScan* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37902-119">Indique s’il faut redémarrer l’analyse ou continuer l’énumération à l’aide des informations passées dans le paramètre de *contexte* .</span><span class="sxs-lookup"><span data-stu-id="37902-119">Indicates whether to restart the scan or continue the enumeration using the information passed in the *Context* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="37902-120">*Contexte* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37902-120">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37902-121">Contexte d’énumération.</span><span class="sxs-lookup"><span data-stu-id="37902-121">The enumeration context.</span></span>

</dd> <dt>

<span data-ttu-id="37902-122">*ReturnLength* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="37902-122">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37902-123">Pointeur vers une variable qui reçoit la longueur des informations de répertoire retournées dans la mémoire tampon de sortie, en octets.</span><span class="sxs-lookup"><span data-stu-id="37902-123">A pointer to a variable that receives the length of the directory information returned in the output buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37902-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37902-124">Return value</span></span>

<span data-ttu-id="37902-125">La fonction retourne l’état **\_ Success** ou un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="37902-125">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="37902-126">Notes</span><span class="sxs-lookup"><span data-stu-id="37902-126">Remarks</span></span>

<span data-ttu-id="37902-127">Voici la définition de la structure d' **\_ \_ informations de répertoire** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="37902-127">The following is the definition of the **OBJECT\_DIRECTORY\_INFORMATION** structure.</span></span>

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

<span data-ttu-id="37902-128">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="37902-128">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="37902-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37902-129">Requirements</span></span>



| <span data-ttu-id="37902-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37902-130">Requirement</span></span> | <span data-ttu-id="37902-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="37902-131">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="37902-132">DLL</span><span class="sxs-lookup"><span data-stu-id="37902-132">DLL</span></span><br/> | <dl> <span data-ttu-id="37902-133"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37902-133"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37902-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37902-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37902-135">**NtOpenDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="37902-135">**NtOpenDirectoryObject**</span></span>](ntopendirectoryobject.md)
</dt> </dl>

 

 
