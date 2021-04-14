---
description: Configure un objet de sortie protégé.
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: ConfigureOPMProtectedOutput fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: d72f3d8bbb7d3063fe6982c6d1de99b2f721f005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393299"
---
# <a name="configureopmprotectedoutput-function"></a><span data-ttu-id="8e2ab-103">ConfigureOPMProtectedOutput fonction)</span><span class="sxs-lookup"><span data-stu-id="8e2ab-103">ConfigureOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e2ab-104">Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="8e2ab-105">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="8e2ab-106">Configure un objet de sortie protégé.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-106">Configures a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2ab-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e2ab-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
);
```



## <a name="parameters"></a><span data-ttu-id="8e2ab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e2ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e2ab-109">*opoOPMProtectedOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e2ab-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e2ab-110">Handle de l’objet de sortie protégé.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-110">A handle to the protected output object.</span></span> <span data-ttu-id="8e2ab-111">Ce handle est obtenu en appelant [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="8e2ab-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e2ab-112">*pParameters* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e2ab-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e2ab-113">Pointeur vers une structure **de \_ \_ \_ paramètres OPM DXGKMDT configure** qui contient la commande de configuration.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-113">A pointer to a **DXGKMDT\_OPM\_CONFIGURE\_PARAMETERS** structure that contains the configuration command.</span></span>

</dd> <dt>

<span data-ttu-id="8e2ab-114">*ulAdditionalParametersSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e2ab-114">*ulAdditionalParametersSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e2ab-115">Taille de la mémoire tampon *pbAdditionalParameters* , en octets.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-115">The size of the *pbAdditionalParameters* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8e2ab-116">*pbAdditionalParameters* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e2ab-116">*pbAdditionalParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e2ab-117">Pointeur vers une mémoire tampon qui contient des informations supplémentaires pour la commande.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-117">A pointer to a buffer that contains additional information for the command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e2ab-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e2ab-118">Return value</span></span>

<span data-ttu-id="8e2ab-119">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="8e2ab-120">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="8e2ab-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e2ab-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8e2ab-121">Remarks</span></span>

<span data-ttu-id="8e2ab-122">Les applications doivent appeler [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) au lieu d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-122">Applications should call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) instead of calling this function.</span></span>

<span data-ttu-id="8e2ab-123">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-123">This function has no associated import library.</span></span> <span data-ttu-id="8e2ab-124">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="8e2ab-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e2ab-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e2ab-125">Requirements</span></span>



| <span data-ttu-id="8e2ab-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e2ab-126">Requirement</span></span> | <span data-ttu-id="8e2ab-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e2ab-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8e2ab-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e2ab-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8e2ab-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e2ab-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8e2ab-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e2ab-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8e2ab-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e2ab-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8e2ab-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8e2ab-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e2ab-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e2ab-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e2ab-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e2ab-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e2ab-135">Fonctions OPM</span><span class="sxs-lookup"><span data-stu-id="8e2ab-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="8e2ab-136">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="8e2ab-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
