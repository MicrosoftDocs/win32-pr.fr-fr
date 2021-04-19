---
description: La fonction FindPropertyInstance recherche la première instance de la propriété spécifiée par le paramètre hProperty.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: FindPropertyInstance, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514572"
---
# <a name="findpropertyinstance-function"></a><span data-ttu-id="b49b1-103">FindPropertyInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="b49b1-103">FindPropertyInstance function</span></span>

<span data-ttu-id="b49b1-104">La fonction **FindPropertyInstance** recherche la première instance de la propriété spécifiée par le paramètre *hProperty* .</span><span class="sxs-lookup"><span data-stu-id="b49b1-104">The **FindPropertyInstance** function finds the first instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b49b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b49b1-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="b49b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b49b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b49b1-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b49b1-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49b1-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="b49b1-108">Handle to the frame.</span></span> <span data-ttu-id="b49b1-109">Le descripteur de frame peut être récupéré par un appel à la fonction [GetFrame](getframe.md) .</span><span class="sxs-lookup"><span data-stu-id="b49b1-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b49b1-110">*hProperty* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b49b1-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49b1-111">Handle vers la propriété que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="b49b1-111">Handle to the property you want to find.</span></span> <span data-ttu-id="b49b1-112">Le descripteur de propriété peut être récupéré par un appel à la fonction [GetProperty](getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="b49b1-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b49b1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b49b1-113">Return value</span></span>

<span data-ttu-id="b49b1-114">Si la fonction réussit (autrement dit, si la propriété est trouvée), la valeur de retour est un pointeur vers la première instance de la propriété.</span><span class="sxs-lookup"><span data-stu-id="b49b1-114">If the function is successful (that is, if the property is found), the return value is a pointer to the first instance of the property.</span></span>

<span data-ttu-id="b49b1-115">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="b49b1-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b49b1-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b49b1-116">Remarks</span></span>

<span data-ttu-id="b49b1-117">Pour récupérer l’instance suivante de la propriété, appelez [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span><span class="sxs-lookup"><span data-stu-id="b49b1-117">To retrieve the next instance of the property, call [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span></span>

<span data-ttu-id="b49b1-118">Les [*experts*](e.md) et les [*analyseurs*](p.md)peuvent appeler la fonction **FindPropertyInstance** .</span><span class="sxs-lookup"><span data-stu-id="b49b1-118">[*Experts*](e.md) and [*parsers*](p.md)can call the **FindPropertyInstance** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49b1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b49b1-119">Requirements</span></span>



| <span data-ttu-id="b49b1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b49b1-120">Requirement</span></span> | <span data-ttu-id="b49b1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b49b1-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b49b1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b49b1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b49b1-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b49b1-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b49b1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b49b1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b49b1-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b49b1-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b49b1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b49b1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b49b1-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b49b1-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b49b1-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b49b1-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="b49b1-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b49b1-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b49b1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b49b1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b49b1-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b49b1-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b49b1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b49b1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b49b1-133">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="b49b1-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




