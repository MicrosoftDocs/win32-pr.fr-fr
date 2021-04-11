---
description: Obtient la taille du tableau qui doit être allouée avant d’appeler CreateOPMProtectedOutputs.
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: GetSuggestedOPMProtectedOutputArraySize fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 87139f0b485ef3c01e5196db85b36faeb662e4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111762"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a><span data-ttu-id="d2d54-103">GetSuggestedOPMProtectedOutputArraySize fonction)</span><span class="sxs-lookup"><span data-stu-id="d2d54-103">GetSuggestedOPMProtectedOutputArraySize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2d54-104">Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d2d54-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="d2d54-105">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d2d54-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="d2d54-106">Obtient la taille du tableau qui doit être allouée avant d’appeler [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="d2d54-106">Gets the size of the array that should be allocated before calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d54-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2d54-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="d2d54-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2d54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d54-109">*pstrDeviceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2d54-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d54-110">Pointeur vers une structure [**de \_ chaîne Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) qui contient le nom du périphérique d’affichage, tel que retourné par la fonction [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="d2d54-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="d2d54-111">*pdwSuggestedOPMProtectedOutputArraySize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d2d54-111">*pdwSuggestedOPMProtectedOutputArraySize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d54-112">Reçoit la taille qui doit être allouée pour le tableau, en nombre d’éléments de tableau.</span><span class="sxs-lookup"><span data-stu-id="d2d54-112">Receives the size that should be allocated for the array, in number of array elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d54-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2d54-113">Return value</span></span>

<span data-ttu-id="d2d54-114">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="d2d54-114">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="d2d54-115">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="d2d54-115">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2d54-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d2d54-116">Remarks</span></span>

<span data-ttu-id="d2d54-117">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="d2d54-117">This function has no associated import library.</span></span> <span data-ttu-id="d2d54-118">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="d2d54-118">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2d54-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2d54-119">Requirements</span></span>



| <span data-ttu-id="d2d54-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2d54-120">Requirement</span></span> | <span data-ttu-id="d2d54-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2d54-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d54-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2d54-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d54-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2d54-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d2d54-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2d54-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d54-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2d54-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d2d54-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d2d54-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2d54-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2d54-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2d54-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2d54-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d54-129">Fonctions OPM</span><span class="sxs-lookup"><span data-stu-id="d2d54-129">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="d2d54-130">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="d2d54-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
