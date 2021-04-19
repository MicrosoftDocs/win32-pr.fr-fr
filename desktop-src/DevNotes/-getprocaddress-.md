---
description: Obtient l’adresse d’une fonction à partir d’une DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: _GetProcAddress_ , fonction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 0d717036b92e79056fd3b1bf69f1fd17784db713
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537633"
---
# <a name="_getprocaddress_-function"></a><span data-ttu-id="aa7e1-103">\_GetProcAddress, \_ fonction</span><span class="sxs-lookup"><span data-stu-id="aa7e1-103">\_GetProcAddress\_ function</span></span>

<span data-ttu-id="aa7e1-104">\[Cette fonction est un wrapper sur la fonction **GetProcAddress** .</span><span class="sxs-lookup"><span data-stu-id="aa7e1-104">\[This function is a wrapper over the **GetProcAddress** function.</span></span> <span data-ttu-id="aa7e1-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="aa7e1-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="aa7e1-106">Les applications doivent appeler **GetProcAddress** directement.\]</span><span class="sxs-lookup"><span data-stu-id="aa7e1-106">Applications should call **GetProcAddress** directly.\]</span></span>

<span data-ttu-id="aa7e1-107">Obtient l’adresse d’une fonction à partir d’une DLL.</span><span class="sxs-lookup"><span data-stu-id="aa7e1-107">Gets the address of a function from a DLL.</span></span> <span data-ttu-id="aa7e1-108">Consultez [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="aa7e1-108">See [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa7e1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa7e1-109">Syntax</span></span>


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="aa7e1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa7e1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa7e1-111">*...*</span><span class="sxs-lookup"><span data-stu-id="aa7e1-111">*...*</span></span> 
<span data-ttu-id="aa7e1-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="aa7e1-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="aa7e1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa7e1-113">Requirements</span></span>



| <span data-ttu-id="aa7e1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa7e1-114">Requirement</span></span> | <span data-ttu-id="aa7e1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa7e1-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7e1-116">DLL</span><span class="sxs-lookup"><span data-stu-id="aa7e1-116">DLL</span></span><br/> | <dl> <span data-ttu-id="aa7e1-117"><dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa7e1-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa7e1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa7e1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa7e1-119">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="aa7e1-119">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
