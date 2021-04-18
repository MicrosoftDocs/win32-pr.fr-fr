---
description: Obtient le nom de l'utilisateur.
ms.assetid: 1373fc9d-ab1c-49b9-8b82-de2e99c4821c
title: _GetUserName fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetUserName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: f61be4596c5076dd7763ed171124888382f3ef6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532780"
---
# <a name="_getusername-function"></a><span data-ttu-id="d0025-103">\_GetUserName, fonction</span><span class="sxs-lookup"><span data-stu-id="d0025-103">\_GetUserName function</span></span>

<span data-ttu-id="d0025-104">\[Cette fonction est un wrapper sur la fonction **getUserName** .</span><span class="sxs-lookup"><span data-stu-id="d0025-104">\[This function is a wrapper over the **GetUserName** function.</span></span> <span data-ttu-id="d0025-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="d0025-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="d0025-106">Les applications doivent appeler **getUserName** directement.\]</span><span class="sxs-lookup"><span data-stu-id="d0025-106">Applications should call **GetUserName** directly.\]</span></span>

<span data-ttu-id="d0025-107">Obtient le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d0025-107">Gets the user name.</span></span> <span data-ttu-id="d0025-108">Consultez [**getUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea).</span><span class="sxs-lookup"><span data-stu-id="d0025-108">See [**GetUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0025-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0025-109">Syntax</span></span>


```C++
BOOL _GetUserName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="d0025-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0025-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0025-111">*...*</span><span class="sxs-lookup"><span data-stu-id="d0025-111">*...*</span></span> 
<span data-ttu-id="d0025-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d0025-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d0025-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0025-113">Requirements</span></span>



| <span data-ttu-id="d0025-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0025-114">Requirement</span></span> | <span data-ttu-id="d0025-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0025-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0025-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d0025-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d0025-117"><dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0025-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0025-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0025-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0025-119">**GetUserName**</span><span class="sxs-lookup"><span data-stu-id="d0025-119">**GetUserName**</span></span>](/windows/win32/api/winbase/nf-winbase-getusernamea)
</dt> </dl>

 

 
