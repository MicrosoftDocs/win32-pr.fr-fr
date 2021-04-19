---
description: Libère un objet de sortie protégé.
ms.assetid: e9b09fd7-9db2-4189-b347-55f5fede2f80
title: DestroyOPMProtectedOutput fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 0a7ce8551cc5e01e7a2801dd129d5dc6903af697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515586"
---
# <a name="destroyopmprotectedoutput-function"></a><span data-ttu-id="a5466-103">DestroyOPMProtectedOutput fonction)</span><span class="sxs-lookup"><span data-stu-id="a5466-103">DestroyOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5466-104">Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a5466-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="a5466-105">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="a5466-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="a5466-106">Libère un objet de sortie protégé.</span><span class="sxs-lookup"><span data-stu-id="a5466-106">Releases a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5466-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5466-107">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyOPMProtectedOutput(
  _In_ OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput
);
```



## <a name="parameters"></a><span data-ttu-id="a5466-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5466-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5466-109">*opoOPMProtectedOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5466-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5466-110">Handle de l’objet de sortie protégé.</span><span class="sxs-lookup"><span data-stu-id="a5466-110">A handle to the protected output object.</span></span> <span data-ttu-id="a5466-111">Ce handle est obtenu en appelant [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="a5466-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5466-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5466-112">Return value</span></span>

<span data-ttu-id="a5466-113">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="a5466-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="a5466-114">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="a5466-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5466-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a5466-115">Remarks</span></span>

<span data-ttu-id="a5466-116">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="a5466-116">This function has no associated import library.</span></span> <span data-ttu-id="a5466-117">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="a5466-117">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5466-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5466-118">Requirements</span></span>



| <span data-ttu-id="a5466-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5466-119">Requirement</span></span> | <span data-ttu-id="a5466-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5466-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a5466-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5466-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5466-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5466-122">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a5466-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5466-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5466-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5466-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a5466-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a5466-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5466-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5466-126"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5466-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5466-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5466-128">Fonctions OPM</span><span class="sxs-lookup"><span data-stu-id="a5466-128">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="a5466-129">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="a5466-129">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
