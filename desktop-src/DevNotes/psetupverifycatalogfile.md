---
description: Vérifie un fichier catalogue unique à l’aide de la stratégie de signature de code du système d’exploitation standard, telle que la signature du pilote.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: pSetupVerifyCatalogFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528016"
---
# <a name="psetupverifycatalogfile-function"></a><span data-ttu-id="e729a-103">pSetupVerifyCatalogFile fonction)</span><span class="sxs-lookup"><span data-stu-id="e729a-103">pSetupVerifyCatalogFile function</span></span>

<span data-ttu-id="e729a-104">\[Cette fonction n’est plus prise en charge par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e729a-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="e729a-105">Pour un fichier INF (installation d’appareils), les développeurs doivent utiliser **SetupVerifyInfFile**.</span><span class="sxs-lookup"><span data-stu-id="e729a-105">For an INF file (device install), developers should use **SetupVerifyInfFile**.</span></span> <span data-ttu-id="e729a-106">Pour valider un catalogue non-INF, utilisez **WinVerifyTrust**.\]</span><span class="sxs-lookup"><span data-stu-id="e729a-106">To validate a non-INF based catalog, use **WinVerifyTrust**.\]</span></span>

<span data-ttu-id="e729a-107">Vérifie un fichier catalogue unique à l’aide de la stratégie de signature de code du système d’exploitation standard, telle que la signature du pilote.</span><span class="sxs-lookup"><span data-stu-id="e729a-107">Verifies a single catalog file using standard operating system code signing policy, such as driver signing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e729a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e729a-108">Syntax</span></span>


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="e729a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e729a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e729a-110">*CatalogFullPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e729a-110">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e729a-111">Chemin d’accès qualifié complet du fichier catalogue à vérifier.</span><span class="sxs-lookup"><span data-stu-id="e729a-111">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e729a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e729a-112">Return value</span></span>

<span data-ttu-id="e729a-113">Si la fonction réussit, elle retourne l' **erreur \_ réussite**; sinon, elle retourne l’erreur de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span><span class="sxs-lookup"><span data-stu-id="e729a-113">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

## <a name="remarks"></a><span data-ttu-id="e729a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e729a-114">Remarks</span></span>

<span data-ttu-id="e729a-115">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e729a-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e729a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e729a-116">Requirements</span></span>



| <span data-ttu-id="e729a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e729a-117">Requirement</span></span> | <span data-ttu-id="e729a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e729a-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e729a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e729a-119">DLL</span></span><br/> | <dl> <span data-ttu-id="e729a-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e729a-120"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e729a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e729a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e729a-122">**SetupVerifyInfFile**</span><span class="sxs-lookup"><span data-stu-id="e729a-122">**SetupVerifyInfFile**</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[<span data-ttu-id="e729a-123">**WinVerifyTrust**</span><span class="sxs-lookup"><span data-stu-id="e729a-123">**WinVerifyTrust**</span></span>](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
