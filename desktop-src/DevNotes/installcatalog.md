---
description: Installe un catalogue dans un répertoire.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: InstallCatalog fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526810"
---
# <a name="installcatalog-function"></a><span data-ttu-id="51ee2-103">InstallCatalog fonction)</span><span class="sxs-lookup"><span data-stu-id="51ee2-103">InstallCatalog function</span></span>

<span data-ttu-id="51ee2-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]</span><span class="sxs-lookup"><span data-stu-id="51ee2-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="51ee2-105">Installe un catalogue dans un répertoire.</span><span class="sxs-lookup"><span data-stu-id="51ee2-105">Installs a catalog in a directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ee2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51ee2-106">Syntax</span></span>


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="51ee2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51ee2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ee2-108">*CatalogFullPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51ee2-108">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51ee2-109">Pointeur vers une chaîne qui représente le chemin d’accès complet du catalogue avant l’installation.</span><span class="sxs-lookup"><span data-stu-id="51ee2-109">A pointer to a string that represents the full path of the catalog before installation.</span></span>

</dd> <dt>

<span data-ttu-id="51ee2-110">*NewBaseName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="51ee2-110">*NewBaseName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="51ee2-111">Pointeur vers le nouveau nom de base.</span><span class="sxs-lookup"><span data-stu-id="51ee2-111">A pointer to the new base name.</span></span>

</dd> <dt>

<span data-ttu-id="51ee2-112">*NewCatalogFullPath* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="51ee2-112">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="51ee2-113">Pointeur vers une chaîne qui représente le chemin d’accès complet du catalogue après l’installation.</span><span class="sxs-lookup"><span data-stu-id="51ee2-113">A pointer to a string that represent the full path of the catalog after installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ee2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51ee2-114">Return value</span></span>

<span data-ttu-id="51ee2-115">Cette fonction n’étant pas implémentée actuellement, elle ne retourne pas de valeur réelle.</span><span class="sxs-lookup"><span data-stu-id="51ee2-115">This function is not currently implemented, so it does not return an actual value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51ee2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="51ee2-116">Remarks</span></span>

<span data-ttu-id="51ee2-117">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="51ee2-117">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ee2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51ee2-118">Requirements</span></span>



| <span data-ttu-id="51ee2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51ee2-119">Requirement</span></span> | <span data-ttu-id="51ee2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="51ee2-120">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51ee2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="51ee2-121">DLL</span></span><br/> | <dl> <span data-ttu-id="51ee2-122"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51ee2-122"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
