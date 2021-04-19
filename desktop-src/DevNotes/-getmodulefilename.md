---
description: Obtient le chemin d’accès du module.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: _GetModuleFileName fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 5bf18e8baac62de6474f4ce1e48a0ae115ced778
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542722"
---
# <a name="_getmodulefilename-function"></a><span data-ttu-id="be4ee-103">\_GetModuleFileName, fonction</span><span class="sxs-lookup"><span data-stu-id="be4ee-103">\_GetModuleFileName function</span></span>

<span data-ttu-id="be4ee-104">\[Cette fonction est un wrapper sur la fonction **GetModuleFileName** .</span><span class="sxs-lookup"><span data-stu-id="be4ee-104">\[This function is a wrapper over the **GetModuleFileName** function.</span></span> <span data-ttu-id="be4ee-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="be4ee-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="be4ee-106">Les applications doivent appeler **GetModuleFileName** directement.\]</span><span class="sxs-lookup"><span data-stu-id="be4ee-106">Applications should call **GetModuleFileName** directly.\]</span></span>

<span data-ttu-id="be4ee-107">Obtient le chemin d’accès du module.</span><span class="sxs-lookup"><span data-stu-id="be4ee-107">Gets the module path.</span></span> <span data-ttu-id="be4ee-108">Consultez [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span><span class="sxs-lookup"><span data-stu-id="be4ee-108">See [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="be4ee-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be4ee-109">Syntax</span></span>


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="be4ee-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be4ee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be4ee-111">*...*</span><span class="sxs-lookup"><span data-stu-id="be4ee-111">*...*</span></span> 
<span data-ttu-id="be4ee-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="be4ee-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="be4ee-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be4ee-113">Requirements</span></span>



| <span data-ttu-id="be4ee-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be4ee-114">Requirement</span></span> | <span data-ttu-id="be4ee-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="be4ee-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be4ee-116">DLL</span><span class="sxs-lookup"><span data-stu-id="be4ee-116">DLL</span></span><br/> | <dl> <span data-ttu-id="be4ee-117"><dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be4ee-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be4ee-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be4ee-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be4ee-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="be4ee-119">**GetModuleFileName**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
