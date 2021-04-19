---
description: Obtient l’espace disque disponible.
ms.assetid: 4b7f4938-9918-4625-b28d-faf22de56976
title: _GetDiskFreeSpaceEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetDiskFreeSpaceEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
ms.openlocfilehash: da4a8eefabf03f6330ac9c1f135482f27dd8aa18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541469"
---
# <a name="_getdiskfreespaceex-function"></a><span data-ttu-id="3d465-103">\_GetDiskFreeSpaceEx fonction)</span><span class="sxs-lookup"><span data-stu-id="3d465-103">\_GetDiskFreeSpaceEx function</span></span>

<span data-ttu-id="3d465-104">\[Cette fonction est un wrapper sur la fonction **GetDiskFreeSpaceEx** .</span><span class="sxs-lookup"><span data-stu-id="3d465-104">\[This function is a wrapper over the **GetDiskFreeSpaceEx** function.</span></span> <span data-ttu-id="3d465-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="3d465-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="3d465-106">Les applications doivent appeler **GetDiskFreeSpaceEx** directement.\]</span><span class="sxs-lookup"><span data-stu-id="3d465-106">Applications should call **GetDiskFreeSpaceEx** directly.\]</span></span>

<span data-ttu-id="3d465-107">Obtient l’espace disque disponible.</span><span class="sxs-lookup"><span data-stu-id="3d465-107">Gets the free disk space.</span></span> <span data-ttu-id="3d465-108">Consultez [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span><span class="sxs-lookup"><span data-stu-id="3d465-108">See [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d465-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d465-109">Syntax</span></span>


```C++
BOOL _GetDiskFreeSpaceEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="3d465-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d465-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d465-111">*...*</span><span class="sxs-lookup"><span data-stu-id="3d465-111">*...*</span></span> 
<span data-ttu-id="3d465-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3d465-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3d465-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d465-113">Requirements</span></span>



| <span data-ttu-id="3d465-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d465-114">Requirement</span></span> | <span data-ttu-id="3d465-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d465-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d465-116">DLL</span><span class="sxs-lookup"><span data-stu-id="3d465-116">DLL</span></span><br/> | <dl> <span data-ttu-id="3d465-117"><dt>Msmdun80.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d465-117"><dt>Msmdun80.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d465-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d465-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d465-119">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="3d465-119">**GetDiskFreeSpaceEx**</span></span>](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa)
</dt> </dl>

 

 
