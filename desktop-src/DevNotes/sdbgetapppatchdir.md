---
description: Récupère le répertoire AppPatch du système.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: SdbGetAppPatchDir fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109923"
---
# <a name="sdbgetapppatchdir-function"></a><span data-ttu-id="7b0d7-103">SdbGetAppPatchDir fonction)</span><span class="sxs-lookup"><span data-stu-id="7b0d7-103">SdbGetAppPatchDir function</span></span>

<span data-ttu-id="7b0d7-104">Récupère le répertoire AppPatch du système.</span><span class="sxs-lookup"><span data-stu-id="7b0d7-104">Retrieves the system AppPatch directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b0d7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b0d7-105">Syntax</span></span>


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a><span data-ttu-id="7b0d7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b0d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b0d7-107">*hSDB* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7b0d7-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7b0d7-108">Handle de la base de données de shims retournée par la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="7b0d7-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7b0d7-109">*szAppPatchPath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7b0d7-109">*szAppPatchPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b0d7-110">Chemin d’accès résultant.</span><span class="sxs-lookup"><span data-stu-id="7b0d7-110">The resulting path.</span></span>

</dd> <dt>

<span data-ttu-id="7b0d7-111">*cchSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7b0d7-111">*cchSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b0d7-112">Taille de la mémoire tampon *szAppPatchPath* , en caractères.</span><span class="sxs-lookup"><span data-stu-id="7b0d7-112">The size of the *szAppPatchPath* buffer, in characters.</span></span> <span data-ttu-id="7b0d7-113">Si la fonction échoue, ce paramètre est défini sur la chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="7b0d7-113">If the function fails, this parameter is set to the empty string ("").</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b0d7-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7b0d7-114">Return value</span></span>

<span data-ttu-id="7b0d7-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7b0d7-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b0d7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b0d7-116">Requirements</span></span>



| <span data-ttu-id="7b0d7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b0d7-117">Requirement</span></span> | <span data-ttu-id="7b0d7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b0d7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0d7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b0d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7b0d7-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b0d7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7b0d7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b0d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7b0d7-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b0d7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7b0d7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7b0d7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b0d7-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b0d7-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b0d7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b0d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b0d7-126">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="7b0d7-126">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




