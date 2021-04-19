---
description: Charge une bibliothèque.
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: _LoadLibrary fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: ce4502813c1ca2a292486a18f1946f4c605c96cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542484"
---
# <a name="_loadlibrary-function"></a><span data-ttu-id="bc2e9-103">\_Fonction LoadLibrary</span><span class="sxs-lookup"><span data-stu-id="bc2e9-103">\_LoadLibrary function</span></span>

<span data-ttu-id="bc2e9-104">\[Cette fonction est un wrapper sur la fonction **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="bc2e9-104">\[This function is a wrapper over the **LoadLibrary** function.</span></span> <span data-ttu-id="bc2e9-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="bc2e9-106">Les applications doivent appeler **LoadLibrary** directement.\]</span><span class="sxs-lookup"><span data-stu-id="bc2e9-106">Applications should call **LoadLibrary** directly.\]</span></span>

<span data-ttu-id="bc2e9-107">Charge une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-107">Loads a library.</span></span> <span data-ttu-id="bc2e9-108">Consultez [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="bc2e9-108">See [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc2e9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc2e9-109">Syntax</span></span>


```C++
HMODULE _LoadLibrary(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="bc2e9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc2e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc2e9-111">*...*</span><span class="sxs-lookup"><span data-stu-id="bc2e9-111">*...*</span></span> 
<span data-ttu-id="bc2e9-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bc2e9-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bc2e9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc2e9-113">Requirements</span></span>



| <span data-ttu-id="bc2e9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc2e9-114">Requirement</span></span> | <span data-ttu-id="bc2e9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc2e9-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc2e9-116">DLL</span><span class="sxs-lookup"><span data-stu-id="bc2e9-116">DLL</span></span><br/> | <dl> <span data-ttu-id="bc2e9-117"><dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e9-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc2e9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc2e9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc2e9-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="bc2e9-119">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
