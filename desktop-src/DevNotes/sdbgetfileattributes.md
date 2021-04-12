---
description: Récupère les données d’attribut pour le fichier spécifié.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: SdbGetFileAttributes fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109918"
---
# <a name="sdbgetfileattributes-function"></a><span data-ttu-id="5a2e6-103">SdbGetFileAttributes fonction)</span><span class="sxs-lookup"><span data-stu-id="5a2e6-103">SdbGetFileAttributes function</span></span>

<span data-ttu-id="5a2e6-104">Récupère les données d’attribut pour le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="5a2e6-104">Retrieves the attribute data for the specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a2e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a2e6-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a><span data-ttu-id="5a2e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a2e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a2e6-107">*lpwszFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a2e6-107">*lpwszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2e6-108">Chemin d'accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="5a2e6-108">The path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="5a2e6-109">*ppAttrInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a2e6-109">*ppAttrInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2e6-110">Tableau de structures [**ATTRINFO**](attrinfo.md) qui contiennent les données d’attribut.</span><span class="sxs-lookup"><span data-stu-id="5a2e6-110">An array of [**ATTRINFO**](attrinfo.md) structures that contain the attribute data.</span></span>

</dd> <dt>

<span data-ttu-id="5a2e6-111">*lpdwAttrCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a2e6-111">*lpdwAttrCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2e6-112">Nombre d'attributs.</span><span class="sxs-lookup"><span data-stu-id="5a2e6-112">The number of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a2e6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a2e6-113">Return value</span></span>

<span data-ttu-id="5a2e6-114">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5a2e6-114">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a2e6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5a2e6-115">Remarks</span></span>

<span data-ttu-id="5a2e6-116">Une fois les données terminées, libérez-les à l’aide de la fonction [**SdbFreeFileAttributes**](sdbfreefileattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="5a2e6-116">When you have finished with the data, free it using the [**SdbFreeFileAttributes**](sdbfreefileattributes.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2e6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a2e6-117">Requirements</span></span>



| <span data-ttu-id="5a2e6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a2e6-118">Requirement</span></span> | <span data-ttu-id="5a2e6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a2e6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2e6-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a2e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a2e6-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a2e6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5a2e6-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a2e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a2e6-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a2e6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5a2e6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5a2e6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a2e6-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a2e6-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a2e6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a2e6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2e6-127">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="5a2e6-127">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="5a2e6-128">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="5a2e6-128">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> </dl>

 

 




