---
description: Vérifie un fichier catalogue unique.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: VerifyCatalogFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539542"
---
# <a name="verifycatalogfile-function"></a><span data-ttu-id="f6764-103">VerifyCatalogFile fonction)</span><span class="sxs-lookup"><span data-stu-id="f6764-103">VerifyCatalogFile function</span></span>

<span data-ttu-id="f6764-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]</span><span class="sxs-lookup"><span data-stu-id="f6764-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="f6764-105">Vérifie un fichier catalogue unique.</span><span class="sxs-lookup"><span data-stu-id="f6764-105">Verifies a single catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6764-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6764-106">Syntax</span></span>


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="f6764-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6764-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6764-108">*CatalogFullPath*</span><span class="sxs-lookup"><span data-stu-id="f6764-108">*CatalogFullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="f6764-109">Chemin d’accès qualifié complet du fichier catalogue à vérifier.</span><span class="sxs-lookup"><span data-stu-id="f6764-109">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6764-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6764-110">Return value</span></span>

<span data-ttu-id="f6764-111">Si la fonction réussit, elle retourne l' **erreur \_ réussite**; sinon, elle retourne l’erreur de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span><span class="sxs-lookup"><span data-stu-id="f6764-111">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

<span data-ttu-id="f6764-112">Si le catalogue est un catalogue signé par Authenticode, cette fonction retourne **l' \_ erreur \_ \_ éditeur approuvé Authenticode** si elle est réussie ; sinon, elle retourne une **erreur \_ Authenticode \_ Trust \_ non \_ établi**.</span><span class="sxs-lookup"><span data-stu-id="f6764-112">If the catalog is an Authenticode-signed catalog, this function returns **ERROR\_AUTHENTICODE\_TRUSTED\_PUBLISHER** if it succeeds; otherwise, it returns **ERROR\_AUTHENTICODE\_TRUST\_NOT\_ESTABLISHED**.</span></span>

<span data-ttu-id="f6764-113">Si la fonction ne peut pas déterminer si le serveur de publication est approuvé, elle peut également retourner une erreur non **\_ identifiée \_**.</span><span class="sxs-lookup"><span data-stu-id="f6764-113">If the function is unable to determine whether the publisher is trusted, it may also return **ERROR\_UNIDENTIFIED\_ERROR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6764-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f6764-114">Remarks</span></span>

<span data-ttu-id="f6764-115">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f6764-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6764-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6764-116">Requirements</span></span>



| <span data-ttu-id="f6764-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6764-117">Requirement</span></span> | <span data-ttu-id="f6764-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6764-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6764-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f6764-119">DLL</span></span><br/> | <dl> <span data-ttu-id="f6764-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6764-120"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
