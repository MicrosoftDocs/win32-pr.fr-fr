---
description: Installe un fichier catalogue.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: pSetupInstallCatalog fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526782"
---
# <a name="psetupinstallcatalog-function"></a><span data-ttu-id="c8f50-103">pSetupInstallCatalog fonction)</span><span class="sxs-lookup"><span data-stu-id="c8f50-103">pSetupInstallCatalog function</span></span>

<span data-ttu-id="c8f50-104">\[Cette fonction n’est plus prise en charge par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c8f50-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="c8f50-105">Les développeurs doivent utiliser **CryptCATAdminAddCatalog**.\]</span><span class="sxs-lookup"><span data-stu-id="c8f50-105">Developers should use **CryptCATAdminAddCatalog**.\]</span></span>

<span data-ttu-id="c8f50-106">Installe un fichier catalogue.</span><span class="sxs-lookup"><span data-stu-id="c8f50-106">Installs a catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f50-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8f50-107">Syntax</span></span>


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="c8f50-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8f50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8f50-109">*CatalogFullPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8f50-109">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f50-110">Chemin d’accès complet du catalogue à installer sur le système.</span><span class="sxs-lookup"><span data-stu-id="c8f50-110">The fully qualified path of the catalog to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8f50-111">*NewBaseName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8f50-111">*NewBaseName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f50-112">Nouveau nom de base à utiliser lorsque le fichier catalogue est copié dans le magasin de catalogues.</span><span class="sxs-lookup"><span data-stu-id="c8f50-112">The new base name to use when the catalog file is copied into the catalog store.</span></span>

</dd> <dt>

<span data-ttu-id="c8f50-113">*NewCatalogFullPath* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c8f50-113">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f50-114">Reçoit éventuellement le chemin d’accès complet du fichier de catalogue dans le magasin de catalogues.</span><span class="sxs-lookup"><span data-stu-id="c8f50-114">Optionally receives the fully qualified path of the catalog file within the catalog store.</span></span> <span data-ttu-id="c8f50-115">Cette mémoire tampon doit être au moins d’octets de **\_ chemin d’accès** (version ANSI) ou de caractères (version Unicode).</span><span class="sxs-lookup"><span data-stu-id="c8f50-115">This buffer should be at least **MAX\_PATH** bytes (ANSI version) or chars (Unicode version).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8f50-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8f50-116">Return value</span></span>

<span data-ttu-id="c8f50-117">Si la fonction est réussie, elle **ne retourne aucune \_ erreur**; sinon, elle retourne un code d’erreur Win32 qui indique la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="c8f50-117">If the function succeeds, it returns **NO\_ERROR**; otherwise, it returns a Win32 error code that indicates the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8f50-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c8f50-118">Remarks</span></span>

<span data-ttu-id="c8f50-119">Le fichier est copié par le système dans un répertoire spécial et est éventuellement renommé.</span><span class="sxs-lookup"><span data-stu-id="c8f50-119">The file is copied by the system into a special directory and is optionally renamed.</span></span>

<span data-ttu-id="c8f50-120">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c8f50-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f50-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8f50-121">Requirements</span></span>



| <span data-ttu-id="c8f50-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8f50-122">Requirement</span></span> | <span data-ttu-id="c8f50-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8f50-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f50-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c8f50-124">DLL</span></span><br/> | <dl> <span data-ttu-id="c8f50-125"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8f50-125"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8f50-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8f50-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f50-127">**CryptCATAdminAddCatalog**</span><span class="sxs-lookup"><span data-stu-id="c8f50-127">**CryptCATAdminAddCatalog**</span></span>](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
