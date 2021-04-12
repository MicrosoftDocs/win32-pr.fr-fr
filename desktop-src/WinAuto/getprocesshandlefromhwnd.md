---
title: GetProcessHandleFromHwnd fonction)
description: Récupère un handle de processus à partir d’un handle de fenêtre.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- GetProcessHandleFromHwnd fonction d’accessibilité Windows
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103819"
---
# <a name="getprocesshandlefromhwnd-function"></a><span data-ttu-id="49e7e-104">GetProcessHandleFromHwnd fonction)</span><span class="sxs-lookup"><span data-stu-id="49e7e-104">GetProcessHandleFromHwnd function</span></span>

<span data-ttu-id="49e7e-105">Récupère un handle de processus à partir d’un handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="49e7e-105">Retrieves a process handle from a window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e7e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49e7e-106">Syntax</span></span>


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="49e7e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49e7e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e7e-108">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49e7e-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e7e-109">Type : **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="49e7e-109">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="49e7e-110">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="49e7e-110">The window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49e7e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49e7e-111">Return value</span></span>

<span data-ttu-id="49e7e-112">Type : **[ **handle**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="49e7e-112">Type: **[**HANDLE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="49e7e-113">En cas de réussite, retourne le handle du processus qui possède la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="49e7e-113">If successful, returns the handle of the process that owns the window.</span></span>

<span data-ttu-id="49e7e-114">En cas d’échec, retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="49e7e-114">If not successful, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e7e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="49e7e-115">Remarks</span></span>

<span data-ttu-id="49e7e-116">Dans les versions précédentes du système d’exploitation, un processus pouvait ouvrir un autre processus (pour accéder à sa mémoire, par exemple) à l’aide de [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span><span class="sxs-lookup"><span data-stu-id="49e7e-116">In previous versions of the operating system, a process could open another process (to access its memory, for example) using [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span></span> <span data-ttu-id="49e7e-117">Cette fonction s’exécute correctement si l’appelant dispose des privilèges appropriés. en général, l’appelant et le processus cible doivent être le même utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49e7e-117">This function succeeds if the caller has appropriate privileges; usually the caller and target process must be the same user.</span></span>

<span data-ttu-id="49e7e-118">Sur Windows Vista, toutefois, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) échoue dans le scénario où l’appelant possède l’UIAccess et le processus cible est élevé.</span><span class="sxs-lookup"><span data-stu-id="49e7e-118">On Windows Vista, however, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) fails in the scenario where the caller has UIAccess, and the target process is elevated.</span></span> <span data-ttu-id="49e7e-119">Dans ce cas, le propriétaire du processus cible se trouve dans le groupe administrateurs, mais le processus appelant s’exécute avec le jeton restreint, donc il n’est pas membre de ce groupe et l’accès au processus élevé est refusé.</span><span class="sxs-lookup"><span data-stu-id="49e7e-119">In this case, the owner of the target process is in the Administrators group, but the calling process is running with the restricted token, so does not have membership in this group, and is denied access to the elevated process.</span></span> <span data-ttu-id="49e7e-120">Toutefois, si l’appelant possède l’UIAccess, il peut utiliser un hook Windows pour injecter du code dans le processus cible et, à partir du processus cible, renvoyer un handle à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="49e7e-120">If the caller has UIAccess, however, they can use a windows hook to inject code into the target process, and from within the target process, send a handle back to the caller.</span></span>

<span data-ttu-id="49e7e-121">**GetProcessHandleFromHwnd** est une fonction pratique qui utilise cette technique pour obtenir le descripteur du processus qui possède le HWND spécifié.</span><span class="sxs-lookup"><span data-stu-id="49e7e-121">**GetProcessHandleFromHwnd** is a convenience function that uses this technique to obtain the handle of the process that owns the specified HWND.</span></span> <span data-ttu-id="49e7e-122">Notez qu’elle ne fonctionne que dans les cas où l’appelant et le processus cible s’exécutent en tant que même utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49e7e-122">Note that it only succeeds in cases where the caller and target process are running as the same user.</span></span> <span data-ttu-id="49e7e-123">Le descripteur retourné possède les privilèges suivants : traiter le handle DUP traiter l’opération de la machine virtuelle traiter le processus lire la machine virtuelle \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ écrire \| synchroniser.</span><span class="sxs-lookup"><span data-stu-id="49e7e-123">The returned handle has the following privileges: PROCESS\_DUP\_HANDLE \| PROCESS\_VM\_OPERATION \| PROCESS\_VM\_READ \| PROCESS\_VM\_WRITE \| SYNCHRONIZE.</span></span> <span data-ttu-id="49e7e-124">Si d’autres privilèges sont requis, il peut être nécessaire d’implémenter la technique de raccordement explicitement au lieu d’utiliser cette fonction.</span><span class="sxs-lookup"><span data-stu-id="49e7e-124">If other privileges are required, it may be necessary to implement the hooking technique explicitly instead of using this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="49e7e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49e7e-125">Requirements</span></span>



| <span data-ttu-id="49e7e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49e7e-126">Requirement</span></span> | <span data-ttu-id="49e7e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="49e7e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49e7e-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49e7e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="49e7e-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49e7e-129">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="49e7e-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49e7e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="49e7e-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49e7e-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49e7e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="49e7e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49e7e-133"><dt>Oleacc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49e7e-133"><dt>Oleacc.dll</dt></span></span> </dl> |



 

