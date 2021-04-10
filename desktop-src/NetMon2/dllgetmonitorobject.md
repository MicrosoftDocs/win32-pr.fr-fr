---
description: La fonction DllGetMonitorObject doit être implémentée par le moniteur. Le MCSVC appelle cette fonction pour créer une instance de l’analyse.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Fonction de rappel DllGetMonitorObject (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868222"
---
# <a name="dllgetmonitorobject-callback-function"></a><span data-ttu-id="14fdf-104">DllGetMonitorObject fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="14fdf-104">DllGetMonitorObject callback function</span></span>

<span data-ttu-id="14fdf-105">La fonction **DllGetMonitorObject** doit être implémentée par le moniteur.</span><span class="sxs-lookup"><span data-stu-id="14fdf-105">The **DllGetMonitorObject** function must be implemented by the monitor.</span></span> <span data-ttu-id="14fdf-106">Le MCSVC appelle cette fonction pour créer une instance de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="14fdf-106">The MCSVC calls this function to create an instance of the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="14fdf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14fdf-107">Syntax</span></span>


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="14fdf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14fdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14fdf-109">*riid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14fdf-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14fdf-110">UUID des analyses, illustré ci-dessous, tel que défini dans le fichier d’en-tête IMonitor. h.</span><span class="sxs-lookup"><span data-stu-id="14fdf-110">UUID of monitors, shown below, as defined in the IMonitor.h header file.</span></span> <span data-ttu-id="14fdf-111">Si un UUID non valide est fourni, la fonction échoue et l’analyse doit retourner E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="14fdf-111">If an invalid UUID is provided, the function fails, and the monitor must return E\_NOINTERFACE.</span></span>

``` syntax
IID_IMonitor
```

</dd> <dt>

<span data-ttu-id="14fdf-112">*ppObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="14fdf-112">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14fdf-113">Pointeur vers un pointeur qui reçoit l’interface demandée dans *riid*.</span><span class="sxs-lookup"><span data-stu-id="14fdf-113">Pointer to a pointer that receives the interface requested in *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14fdf-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14fdf-114">Return value</span></span>

<span data-ttu-id="14fdf-115">Si la fonction réussit, la valeur de retour est S \_ OK (ce qui est identique à la valeur de l’erreur).</span><span class="sxs-lookup"><span data-stu-id="14fdf-115">If the function is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="14fdf-116">Si la fonction échoue, la valeur de retour est un code d’échec.</span><span class="sxs-lookup"><span data-stu-id="14fdf-116">If the function is unsuccessful, the return value is a failure code.</span></span> <span data-ttu-id="14fdf-117">Lorsqu’un code d’erreur est retourné, MCSVC ne crée pas l’objet d’analyse, et la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) n’est pas appelée sur le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="14fdf-117">When a failure code is returned, the MCSVC does not create the monitor object, and the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method is not called on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="14fdf-118">Notes</span><span class="sxs-lookup"><span data-stu-id="14fdf-118">Remarks</span></span>

<span data-ttu-id="14fdf-119">La fonction **DllGetMonitorObject** est appelée chaque fois que le MCSVC essaie de créer une instance de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="14fdf-119">The **DllGetMonitorObject** function is called each time the MCSVC tries to create an instance of the monitor.</span></span> <span data-ttu-id="14fdf-120">Cette fonction est intentionnellement une forte ressemblance avec la fonction [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) la plus courante.</span><span class="sxs-lookup"><span data-stu-id="14fdf-120">This function intentionally bears a strong resemblance to the more common [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) function.</span></span> <span data-ttu-id="14fdf-121">La principale différence est qu’un CLSID n’est pas transmis à **DllGetMonitorObject**.</span><span class="sxs-lookup"><span data-stu-id="14fdf-121">The main difference is that a CLSID is not passed in to **DllGetMonitorObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="14fdf-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14fdf-122">Requirements</span></span>



| <span data-ttu-id="14fdf-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14fdf-123">Requirement</span></span> | <span data-ttu-id="14fdf-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="14fdf-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="14fdf-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14fdf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="14fdf-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14fdf-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="14fdf-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14fdf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="14fdf-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14fdf-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="14fdf-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="14fdf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="14fdf-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="14fdf-130"><dt>Netmon.h</dt></span></span> </dl> |



 

