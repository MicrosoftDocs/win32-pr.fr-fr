---
description: Définit la clé de signature et deux numéros de séquence sur un objet de sortie protégé.
ms.assetid: 278a80f5-198d-4311-aa43-10b6dc33b3a4
title: SetOPMSigningKeyAndSequenceNumbers fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetOPMSigningKeyAndSequenceNumbers
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: cbd088b83acd4e93cc186e6c7b5635ad1e3d8346
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201846"
---
# <a name="setopmsigningkeyandsequencenumbers-function"></a><span data-ttu-id="375c7-103">SetOPMSigningKeyAndSequenceNumbers fonction)</span><span class="sxs-lookup"><span data-stu-id="375c7-103">SetOPMSigningKeyAndSequenceNumbers function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="375c7-104">Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="375c7-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="375c7-105">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="375c7-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="375c7-106">Définit la clé de signature et deux numéros de séquence sur un objet de sortie protégé.</span><span class="sxs-lookup"><span data-stu-id="375c7-106">Sets the signing key and two sequence numbers on a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="375c7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="375c7-107">Syntax</span></span>


```C++
NTSTATUS WINAPI SetOPMSigningKeyAndSequenceNumbers(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _Out_ const DXGKMDT_OPM_ENCRYPTED_PARAMETERS *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="375c7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="375c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="375c7-109">*opoOPMProtectedOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="375c7-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="375c7-110">Handle de l’objet de sortie protégé.</span><span class="sxs-lookup"><span data-stu-id="375c7-110">A handle to the protected output object.</span></span> <span data-ttu-id="375c7-111">Ce handle est obtenu en appelant [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="375c7-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="375c7-112">*pParameters* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="375c7-112">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="375c7-113">Pointeur vers une structure [**de \_ \_ \_ paramètres chiffrés OPM DXGKMDT**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) qui contient un tableau de 256 octets.</span><span class="sxs-lookup"><span data-stu-id="375c7-113">A pointer to a [**DXGKMDT\_OPM\_ENCRYPTED\_PARAMETERS**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) structure that contains a 256-byte array.</span></span> <span data-ttu-id="375c7-114">Pour plus d’informations sur l’initialisation de ce tableau, consultez [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span><span class="sxs-lookup"><span data-stu-id="375c7-114">For more information about how to initialize this array, see [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="375c7-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="375c7-115">Return value</span></span>

<span data-ttu-id="375c7-116">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="375c7-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="375c7-117">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="375c7-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="375c7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="375c7-118">Remarks</span></span>

<span data-ttu-id="375c7-119">Les applications doivent appeler [**IOPMVideoOutput :: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) au lieu d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="375c7-119">Applications should call [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) instead of calling this function.</span></span>

<span data-ttu-id="375c7-120">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="375c7-120">This function has no associated import library.</span></span> <span data-ttu-id="375c7-121">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="375c7-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="375c7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="375c7-122">Requirements</span></span>



| <span data-ttu-id="375c7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="375c7-123">Requirement</span></span> | <span data-ttu-id="375c7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="375c7-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="375c7-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="375c7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="375c7-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="375c7-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="375c7-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="375c7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="375c7-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="375c7-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="375c7-129">DLL</span><span class="sxs-lookup"><span data-stu-id="375c7-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="375c7-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="375c7-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="375c7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="375c7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="375c7-132">Fonctions OPM</span><span class="sxs-lookup"><span data-stu-id="375c7-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="375c7-133">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="375c7-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
