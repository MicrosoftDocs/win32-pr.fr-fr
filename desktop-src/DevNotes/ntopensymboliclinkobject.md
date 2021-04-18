---
description: Ouvre un lien symbolique existant.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: NtOpenSymbolicLinkObject fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526731"
---
# <a name="ntopensymboliclinkobject-function"></a><span data-ttu-id="4a144-103">NtOpenSymbolicLinkObject fonction)</span><span class="sxs-lookup"><span data-stu-id="4a144-103">NtOpenSymbolicLinkObject function</span></span>

<span data-ttu-id="4a144-104">\[Cette fonction peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="4a144-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4a144-105">Ouvre un lien symbolique existant.</span><span class="sxs-lookup"><span data-stu-id="4a144-105">Opens an existing symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a144-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a144-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="4a144-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a144-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a144-108">*LinkHandle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4a144-108">*LinkHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a144-109">Handle vers l’objet de lien symbolique récemment ouvert.</span><span class="sxs-lookup"><span data-stu-id="4a144-109">A handle to the newly opened symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="4a144-110">*DesiredAccess* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a144-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a144-111">[**\_ Masque d’accès**](../secauthz/access-mask.md) qui spécifie l’accès demandé à l’objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="4a144-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="4a144-112">Il est courant d’utiliser \_ la lecture générique pour que le handle puisse être passé à la fonction [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) .</span><span class="sxs-lookup"><span data-stu-id="4a144-112">It is typical to use GENERIC\_READ so the handle can be passed to the [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4a144-113">*ObjectAttributes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a144-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a144-114">Attributs de l’objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="4a144-114">The attributes for the directory object.</span></span> <span data-ttu-id="4a144-115">Pour initialiser la structure des **\_ attributs d’objet** , utilisez la macro **InitializeObjectAttributes** .</span><span class="sxs-lookup"><span data-stu-id="4a144-115">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="4a144-116">Si l’appelant n’est pas exécuté dans un contexte de thread système, il doit spécifier l’indicateur de **\_ \_ handle de noyau obj** lors de l’initialisation de la structure.</span><span class="sxs-lookup"><span data-stu-id="4a144-116">If the caller is not running in a system thread context, it must specify the **OBJ\_KERNEL\_HANDLE** flag when initializing the structure.</span></span> <span data-ttu-id="4a144-117">Pour plus d’informations, consultez la documentation de ces éléments dans la documentation du kit WDK.</span><span class="sxs-lookup"><span data-stu-id="4a144-117">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a144-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a144-118">Return value</span></span>

<span data-ttu-id="4a144-119">La fonction retourne l’état **\_ Success** ou un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4a144-119">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a144-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4a144-120">Remarks</span></span>

<span data-ttu-id="4a144-121">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4a144-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a144-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a144-122">Requirements</span></span>



| <span data-ttu-id="4a144-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a144-123">Requirement</span></span> | <span data-ttu-id="4a144-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a144-124">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4a144-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4a144-125">DLL</span></span><br/> | <dl> <span data-ttu-id="4a144-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a144-126"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a144-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a144-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a144-128">**NtQueryDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="4a144-128">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
