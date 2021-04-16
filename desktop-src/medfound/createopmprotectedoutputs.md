---
description: Crée des objets de sortie protégés pour un périphérique d’affichage.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: CreateOPMProtectedOutputs fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 215cff4a76e7eb36e516e8fd2db312302763198e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524620"
---
# <a name="createopmprotectedoutputs-function"></a><span data-ttu-id="5aad3-103">CreateOPMProtectedOutputs fonction)</span><span class="sxs-lookup"><span data-stu-id="5aad3-103">CreateOPMProtectedOutputs function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5aad3-104">Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5aad3-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="5aad3-105">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="5aad3-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="5aad3-106">Crée des objets de sortie protégés pour un périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5aad3-106">Creates protected output objects for a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aad3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5aad3-107">Syntax</span></span>


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a><span data-ttu-id="5aad3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5aad3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aad3-109">*pstrDeviceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5aad3-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aad3-110">Pointeur vers une structure [**de \_ chaîne Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) qui contient le nom du périphérique d’affichage, tel que retourné par la fonction [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="5aad3-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="5aad3-111">*vos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5aad3-111">*vos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aad3-112">Membre de l’énumération de la **\_ \_ \_ \_ sémantique de sortie vidéo de l’DXGKMDT OPM** , indiquant si la sortie protégée aura une sémantique COPP (Certified Output Protection Protocol) ou OPM.</span><span class="sxs-lookup"><span data-stu-id="5aad3-112">A member of the **DXGKMDT\_OPM\_VIDEO\_OUTPUT\_SEMANTICS** enumeration, specifying whether the protected output will have Certified Output Protection Protocol (COPP) semantics or OPM semantics.</span></span>

</dd> <dt>

<span data-ttu-id="5aad3-113">*dwOPMProtectedOutputArraySize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5aad3-113">*dwOPMProtectedOutputArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aad3-114">Nombre d’éléments dans le tableau *pohOPMProtectedOutputArray* .</span><span class="sxs-lookup"><span data-stu-id="5aad3-114">The number of elements in the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="5aad3-115">*pdwNumOPMProtectedOutputsInArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5aad3-115">*pdwNumOPMProtectedOutputsInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5aad3-116">Reçoit le nombre d’éléments que la fonction copie dans le tableau *pohOPMProtectedOutputArray* .</span><span class="sxs-lookup"><span data-stu-id="5aad3-116">Receives the number of items that the function copies to the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="5aad3-117">*pohOPMProtectedOutputArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5aad3-117">*pohOPMProtectedOutputArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5aad3-118">Tableau qui reçoit des handles vers les objets de sortie protégés.</span><span class="sxs-lookup"><span data-stu-id="5aad3-118">An array that receives handles to the protected output objects.</span></span> <span data-ttu-id="5aad3-119">Chaque descripteur doit être libéré en appelant [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span><span class="sxs-lookup"><span data-stu-id="5aad3-119">Each handle must be released by calling [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aad3-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5aad3-120">Return value</span></span>

<span data-ttu-id="5aad3-121">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="5aad3-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="5aad3-122">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="5aad3-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aad3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="5aad3-123">Remarks</span></span>

<span data-ttu-id="5aad3-124">Au lieu d’utiliser cette fonction, les applications doivent appeler l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="5aad3-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="5aad3-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="5aad3-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [<span data-ttu-id="5aad3-126">**OPMGetVideoOutputsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="5aad3-126">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

<span data-ttu-id="5aad3-127">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="5aad3-127">This function has no associated import library.</span></span> <span data-ttu-id="5aad3-128">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="5aad3-128">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aad3-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5aad3-129">Requirements</span></span>



| <span data-ttu-id="5aad3-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5aad3-130">Requirement</span></span> | <span data-ttu-id="5aad3-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5aad3-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5aad3-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5aad3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5aad3-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5aad3-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5aad3-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5aad3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5aad3-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5aad3-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5aad3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5aad3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aad3-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aad3-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aad3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aad3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aad3-139">Fonctions OPM</span><span class="sxs-lookup"><span data-stu-id="5aad3-139">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="5aad3-140">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="5aad3-140">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
