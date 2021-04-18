---
description: Convertit une URL de fichier en un chemin d’accès Microsoft MS-DOS.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: MFCreatePathFromURL fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516053"
---
# <a name="mfcreatepathfromurl-function"></a><span data-ttu-id="f3fbc-103">MFCreatePathFromURL fonction)</span><span class="sxs-lookup"><span data-stu-id="f3fbc-103">MFCreatePathFromURL function</span></span>

<span data-ttu-id="f3fbc-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f3fbc-105">Au lieu de cela, les applications doivent appeler [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span><span class="sxs-lookup"><span data-stu-id="f3fbc-105">Instead, applications should call [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span></span>

<span data-ttu-id="f3fbc-106">Convertit une URL de fichier en un chemin d’accès Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-106">Converts a file URL to a Microsoft MS-DOS path.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3fbc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3fbc-107">Syntax</span></span>


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a><span data-ttu-id="f3fbc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3fbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3fbc-109">*pwszFileURL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f3fbc-109">*pwszFileURL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f3fbc-110">Chaîne terminée par le caractère null qui contient l’URL.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-110">A null-terminated string that contains the URL.</span></span> <span data-ttu-id="f3fbc-111">La longueur maximale de la chaîne est la longueur de l' **\_ \_ URL \_ maximale Internet**.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="f3fbc-112">*ppwszFilePath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f3fbc-112">*ppwszFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3fbc-113">Reçoit une chaîne terminée par le caractère null qui contient l’URL.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="f3fbc-114">L’appelant doit libérer la chaîne en appelant [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="f3fbc-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3fbc-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3fbc-115">Return value</span></span>

<span data-ttu-id="f3fbc-116">La fonction retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="f3fbc-117">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f3fbc-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f3fbc-118">Return code</span></span>                                                                                  | <span data-ttu-id="f3fbc-119">Description</span><span class="sxs-lookup"><span data-stu-id="f3fbc-119">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3fbc-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f3fbc-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f3fbc-121">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-121">The function succeeded.</span></span> <br/>                                                                         |
| <dl> <span data-ttu-id="f3fbc-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f3fbc-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f3fbc-123">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-123">Invalid argument.</span></span> <span data-ttu-id="f3fbc-124">La chaîne spécifiée dans le paramètre *pwszFileURL* ne peut pas être convertie en chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-124">The string given in the *pwszFileURL* parameter cannot be converted to a path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f3fbc-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f3fbc-125">Remarks</span></span>

<span data-ttu-id="f3fbc-126">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-126">This function has no associated import library.</span></span> <span data-ttu-id="f3fbc-127">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mfplat.dll.</span><span class="sxs-lookup"><span data-stu-id="f3fbc-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3fbc-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3fbc-128">Requirements</span></span>



| <span data-ttu-id="f3fbc-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3fbc-129">Requirement</span></span> | <span data-ttu-id="f3fbc-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3fbc-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3fbc-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3fbc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f3fbc-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3fbc-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3fbc-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3fbc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f3fbc-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3fbc-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3fbc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f3fbc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3fbc-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3fbc-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3fbc-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3fbc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3fbc-138">Fonctions Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3fbc-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
