---
description: Obtient le nom de l'ordinateur.
ms.assetid: 8b6fd61a-dd5a-46b8-920e-cc8a848732b6
title: _GetComputerName fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetComputerName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a8fc124e9a5b036e1be83e49e504d2a4d42ea27a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532631"
---
# <a name="_getcomputername-function"></a><span data-ttu-id="80b2d-103">\_GetComputerName (fonction)</span><span class="sxs-lookup"><span data-stu-id="80b2d-103">\_GetComputerName function</span></span>

<span data-ttu-id="80b2d-104">\[Cette fonction est un wrapper sur la fonction **GetComputerName** .</span><span class="sxs-lookup"><span data-stu-id="80b2d-104">\[This function is a wrapper over the **GetComputerName** function.</span></span> <span data-ttu-id="80b2d-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="80b2d-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="80b2d-106">Les applications doivent appeler **GetComputerName** directement.\]</span><span class="sxs-lookup"><span data-stu-id="80b2d-106">Applications should call **GetComputerName** directly.\]</span></span>

<span data-ttu-id="80b2d-107">Obtient le nom de l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="80b2d-107">Gets the computer name.</span></span> <span data-ttu-id="80b2d-108">Consultez [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span><span class="sxs-lookup"><span data-stu-id="80b2d-108">See [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="80b2d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80b2d-109">Syntax</span></span>


```C++
BOOL _GetComputerName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="80b2d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80b2d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80b2d-111">*...*</span><span class="sxs-lookup"><span data-stu-id="80b2d-111">*...*</span></span> 
<span data-ttu-id="80b2d-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="80b2d-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="80b2d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80b2d-113">Requirements</span></span>



| <span data-ttu-id="80b2d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80b2d-114">Requirement</span></span> | <span data-ttu-id="80b2d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="80b2d-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b2d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="80b2d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="80b2d-117"><dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80b2d-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80b2d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80b2d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b2d-119">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="80b2d-119">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> </dl>

 

 
