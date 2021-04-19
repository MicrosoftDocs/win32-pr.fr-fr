---
description: Récupère la cible d’un lien symbolique.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: NtQuerySymbolicLinkObject fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543593"
---
# <a name="ntquerysymboliclinkobject-function"></a><span data-ttu-id="5e087-103">NtQuerySymbolicLinkObject fonction)</span><span class="sxs-lookup"><span data-stu-id="5e087-103">NtQuerySymbolicLinkObject function</span></span>

<span data-ttu-id="5e087-104">\[Cette fonction peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="5e087-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5e087-105">Récupère la cible d’un lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="5e087-105">Retrieves the target of a symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e087-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e087-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a><span data-ttu-id="5e087-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e087-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e087-108">*LinkHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e087-108">*LinkHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e087-109">Handle de l’objet de lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="5e087-109">A handle to the symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="5e087-110">*LinkTarget* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5e087-110">*LinkTarget* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e087-111">Pointeur vers une chaîne Unicode initialisée qui reçoit la cible du lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="5e087-111">A pointer to an initialized Unicode string that receives the target of the symbolic link.</span></span> <span data-ttu-id="5e087-112">Les membres **MaximumLength** et **buffer** doivent être définis si l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="5e087-112">The **MaximumLength** and **Buffer** members must be set if the call fails.</span></span>

</dd> <dt>

<span data-ttu-id="5e087-113">*ReturnedLength* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5e087-113">*ReturnedLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e087-114">Pointeur vers une variable qui reçoit la longueur de la chaîne Unicode retournée dans le paramètre *LinkTarget* .</span><span class="sxs-lookup"><span data-stu-id="5e087-114">A pointer to a variable that receives the length of the Unicode string returned in the *LinkTarget* parameter.</span></span> <span data-ttu-id="5e087-115">Si la fonction retourne **une \_ mémoire tampon d’état \_ trop \_ petite**, cette variable reçoit la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="5e087-115">If the function returns **STATUS\_BUFFER\_TOO\_SMALL**, this variable receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e087-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e087-116">Return value</span></span>

<span data-ttu-id="5e087-117">La fonction retourne l’état **\_ Success** ou un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5e087-117">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e087-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5e087-118">Remarks</span></span>

<span data-ttu-id="5e087-119">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="5e087-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e087-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e087-120">Requirements</span></span>



| <span data-ttu-id="5e087-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e087-121">Requirement</span></span> | <span data-ttu-id="5e087-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e087-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5e087-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5e087-123">DLL</span></span><br/> | <dl> <span data-ttu-id="5e087-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e087-124"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e087-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e087-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e087-126">**NtOpenSymbolicLinkObject**</span><span class="sxs-lookup"><span data-stu-id="5e087-126">**NtOpenSymbolicLinkObject**</span></span>](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
