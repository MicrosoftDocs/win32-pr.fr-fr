---
description: Convertit un chemin d’accès Microsoft MS-DOS en URL canonique.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MFCreateURLFromPath fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516938"
---
# <a name="mfcreateurlfrompath-function"></a><span data-ttu-id="3be39-103">MFCreateURLFromPath fonction)</span><span class="sxs-lookup"><span data-stu-id="3be39-103">MFCreateURLFromPath function</span></span>

<span data-ttu-id="3be39-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="3be39-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="3be39-105">Au lieu de cela, les applications doivent appeler [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span><span class="sxs-lookup"><span data-stu-id="3be39-105">Instead, Applications should call [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span></span>

<span data-ttu-id="3be39-106">Convertit un chemin d’accès Microsoft MS-DOS en URL canonique.</span><span class="sxs-lookup"><span data-stu-id="3be39-106">Converts a Microsoft MS-DOS path to a canonicalized URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be39-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3be39-107">Syntax</span></span>


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a><span data-ttu-id="3be39-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3be39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be39-109">*pwszFilePath* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3be39-109">*pwszFilePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3be39-110">Chaîne terminée par le caractère null qui contient le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="3be39-110">A null-terminated string that contains the path.</span></span> <span data-ttu-id="3be39-111">La longueur maximale de la chaîne est la longueur de l' **\_ \_ URL \_ maximale Internet**.</span><span class="sxs-lookup"><span data-stu-id="3be39-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="3be39-112">*ppwszFileURL* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3be39-112">*ppwszFileURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3be39-113">Reçoit une chaîne terminée par le caractère null qui contient l’URL.</span><span class="sxs-lookup"><span data-stu-id="3be39-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="3be39-114">L’appelant doit libérer la chaîne en appelant [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="3be39-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3be39-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3be39-115">Return value</span></span>

<span data-ttu-id="3be39-116">La fonction retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3be39-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="3be39-117">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3be39-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3be39-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3be39-118">Return code</span></span>                                                                             | <span data-ttu-id="3be39-119">Description</span><span class="sxs-lookup"><span data-stu-id="3be39-119">Description</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3be39-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3be39-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="3be39-121">La chaîne spécifiée dans le paramètre *pwszFilePath* est déjà au format URL.</span><span class="sxs-lookup"><span data-stu-id="3be39-121">The string given in the *pwszFilePath* parameter is already in URL format.</span></span> <span data-ttu-id="3be39-122">Dans ce cas, *pszFilePath* est simplement copié sur *ppszFileURL* sans modification.</span><span class="sxs-lookup"><span data-stu-id="3be39-122">In this case, *pszFilePath* is simply copied to *ppszFileURL* without modification.</span></span><br/> |
| <dl> <span data-ttu-id="3be39-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3be39-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="3be39-124">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="3be39-124">The function succeeded.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="3be39-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3be39-125">Remarks</span></span>

<span data-ttu-id="3be39-126">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="3be39-126">This function has no associated import library.</span></span> <span data-ttu-id="3be39-127">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mfplat.dll.</span><span class="sxs-lookup"><span data-stu-id="3be39-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be39-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3be39-128">Requirements</span></span>



| <span data-ttu-id="3be39-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3be39-129">Requirement</span></span> | <span data-ttu-id="3be39-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="3be39-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3be39-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3be39-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3be39-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3be39-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3be39-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3be39-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3be39-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3be39-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3be39-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3be39-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3be39-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3be39-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be39-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3be39-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be39-138">Fonctions Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3be39-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
