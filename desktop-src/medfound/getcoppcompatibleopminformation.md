---
description: Envoie une demande d’État COPP (Certified Output Protection Protocol) à un objet de sortie protégé.
ms.assetid: 24300591-c0c0-48a2-99d3-be98c0c1492a
title: GetCOPPCompatibleOPMInformation fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCOPPCompatibleOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7e5eac24dfcf08e45ce414090835792e594d7c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201146"
---
# <a name="getcoppcompatibleopminformation-function"></a><span data-ttu-id="cbec8-103">GetCOPPCompatibleOPMInformation fonction)</span><span class="sxs-lookup"><span data-stu-id="cbec8-103">GetCOPPCompatibleOPMInformation function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbec8-104">Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cbec8-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="cbec8-105">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cbec8-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="cbec8-106">Envoie une demande d’État COPP (Certified Output Protection Protocol) à un objet de sortie protégé.</span><span class="sxs-lookup"><span data-stu-id="cbec8-106">Sends a Certified Output Protection Protocol (COPP) status request to a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbec8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbec8-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCOPPCompatibleOPMInformation(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE                     opoOPMProtectedOutput,
  _In_  DXGKMDT_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
  _Out_ DXGKMDT_OPM_REQUESTED_INFORMATION               *pRequestedInformation
);
```



## <a name="parameters"></a><span data-ttu-id="cbec8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbec8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbec8-109">*opoOPMProtectedOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbec8-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbec8-110">Handle de l’objet de sortie protégé.</span><span class="sxs-lookup"><span data-stu-id="cbec8-110">A handle to the protected output object.</span></span> <span data-ttu-id="cbec8-111">Ce handle est obtenu en appelant [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="cbec8-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbec8-112">*pParameters* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbec8-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbec8-113">Pointeur vers une structure **DXGKMDT \_ OPM \_ Copp \_ compatible \_ obtenir \_ les \_ paramètres** qui contient des données d’entrée pour la demande d’État.</span><span class="sxs-lookup"><span data-stu-id="cbec8-113">A pointer to a **DXGKMDT\_OPM\_COPP\_COMPATIBLE\_GET\_INFO\_PARAMETERS** structure that contains input data for the status request.</span></span>

</dd> <dt>

<span data-ttu-id="cbec8-114">*pRequestedInformation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cbec8-114">*pRequestedInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbec8-115">Pointeur vers une structure **d' \_ \_ \_ informations DXGKMDT OPM demandée** qui reçoit les résultats de la demande d’État.</span><span class="sxs-lookup"><span data-stu-id="cbec8-115">A pointer to a **DXGKMDT\_OPM\_REQUESTED\_INFORMATION** structure that receives the results of the status request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbec8-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cbec8-116">Return value</span></span>

<span data-ttu-id="cbec8-117">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="cbec8-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="cbec8-118">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="cbec8-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbec8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="cbec8-119">Remarks</span></span>

<span data-ttu-id="cbec8-120">Les applications doivent appeler [**IOPMVideoOutput :: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) au lieu d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cbec8-120">Applications should call [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) instead of calling this function.</span></span>

<span data-ttu-id="cbec8-121">L’objet de sortie protégé doit être créé avec la sémantique COPP.</span><span class="sxs-lookup"><span data-stu-id="cbec8-121">The protected output object must be created with COPP semantics.</span></span> <span data-ttu-id="cbec8-122">Consultez [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="cbec8-122">See [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

<span data-ttu-id="cbec8-123">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="cbec8-123">This function has no associated import library.</span></span> <span data-ttu-id="cbec8-124">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="cbec8-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbec8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbec8-125">Requirements</span></span>



| <span data-ttu-id="cbec8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbec8-126">Requirement</span></span> | <span data-ttu-id="cbec8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbec8-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cbec8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbec8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cbec8-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbec8-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cbec8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbec8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cbec8-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbec8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cbec8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cbec8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbec8-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbec8-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbec8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbec8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbec8-135">Fonctions OPM</span><span class="sxs-lookup"><span data-stu-id="cbec8-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="cbec8-136">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="cbec8-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
