---
description: Crée une instance du moteur de capture.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: MFCreateCaptureEngine fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527337"
---
# <a name="mfcreatecaptureengine-function"></a><span data-ttu-id="ed8c3-103">MFCreateCaptureEngine fonction)</span><span class="sxs-lookup"><span data-stu-id="ed8c3-103">MFCreateCaptureEngine function</span></span>

<span data-ttu-id="ed8c3-104">\[MFCreateCaptureEngine n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-104">\[MFCreateCaptureEngine is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="ed8c3-105">\]</span><span class="sxs-lookup"><span data-stu-id="ed8c3-105">\]</span></span>

<span data-ttu-id="ed8c3-106">Crée une instance du moteur de capture.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-106">Creates an instance of the capture engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed8c3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed8c3-107">Syntax</span></span>


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a><span data-ttu-id="ed8c3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed8c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8c3-109">*ppCaptureEngine* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed8c3-109">*ppCaptureEngine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8c3-110">Reçoit un pointeur vers l’interface [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) .</span><span class="sxs-lookup"><span data-stu-id="ed8c3-110">Receives a pointer to the [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) interface.</span></span> <span data-ttu-id="ed8c3-111">L’appelant doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-111">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed8c3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed8c3-112">Return value</span></span>

<span data-ttu-id="ed8c3-113">Si la fonction est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-113">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="ed8c3-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ed8c3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed8c3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ed8c3-115">Remarks</span></span>

<span data-ttu-id="ed8c3-116">Cette fonction n’a pas de bibliothèque d’importation associée et n’est pas déclarée dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-116">This function has no associated import library and is not declared in a public header file.</span></span> <span data-ttu-id="ed8c3-117">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à MFCaptureEngine.dll.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-117">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to MFCaptureEngine.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8c3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed8c3-118">Requirements</span></span>



| <span data-ttu-id="ed8c3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed8c3-119">Requirement</span></span> | <span data-ttu-id="ed8c3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed8c3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8c3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed8c3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8c3-122">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed8c3-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ed8c3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed8c3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8c3-124">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed8c3-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed8c3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ed8c3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed8c3-126"><dt>MFCaptureEngine.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed8c3-126"><dt>MFCaptureEngine.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed8c3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed8c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8c3-128">Fonctions Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ed8c3-128">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
