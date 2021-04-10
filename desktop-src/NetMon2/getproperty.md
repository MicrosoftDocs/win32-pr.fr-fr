---
description: La fonction GetProperty retourne un handle vers une propriété donnée.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: GetProperty, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950959"
---
# <a name="getproperty-function"></a><span data-ttu-id="7dbf5-103">GetProperty, fonction</span><span class="sxs-lookup"><span data-stu-id="7dbf5-103">GetProperty function</span></span>

<span data-ttu-id="7dbf5-104">La fonction **GetProperty** retourne un handle vers une propriété donnée.</span><span class="sxs-lookup"><span data-stu-id="7dbf5-104">The **GetProperty** function returns a handle to a given property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dbf5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dbf5-105">Syntax</span></span>


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a><span data-ttu-id="7dbf5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dbf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dbf5-107">*hProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dbf5-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dbf5-108">Handle du protocole.</span><span class="sxs-lookup"><span data-stu-id="7dbf5-108">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="7dbf5-109">*PropertyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dbf5-109">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dbf5-110">Nom de la propriété (par exemple, **checksum**).</span><span class="sxs-lookup"><span data-stu-id="7dbf5-110">Name of the property (for example, **Checksum**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dbf5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7dbf5-111">Return value</span></span>

<span data-ttu-id="7dbf5-112">Si la fonction réussit, la valeur de retour est le handle de la propriété.</span><span class="sxs-lookup"><span data-stu-id="7dbf5-112">If the function is successful, the return value is the handle to the property.</span></span>

<span data-ttu-id="7dbf5-113">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="7dbf5-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dbf5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7dbf5-114">Remarks</span></span>

<span data-ttu-id="7dbf5-115">La fonction **GetProperty** peut être utilisée pour obtenir le handle de propriété nécessaire pour localiser les instances de la propriété.</span><span class="sxs-lookup"><span data-stu-id="7dbf5-115">The **GetProperty** function can be used to obtain the property handle needed to locate instances of the property.</span></span> <span data-ttu-id="7dbf5-116">Les fonctions utilisées pour localiser les instances de propriété sont [FindPropertyInstance](findpropertyinstance.md) (qui localise la première instance) et [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (qui localise l’instance suivante).</span><span class="sxs-lookup"><span data-stu-id="7dbf5-116">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) (which locates the first instance) and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (which locates the next instance).</span></span>

<span data-ttu-id="7dbf5-117">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetProperty** .</span><span class="sxs-lookup"><span data-stu-id="7dbf5-117">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProperty** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dbf5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dbf5-118">Requirements</span></span>



| <span data-ttu-id="7dbf5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7dbf5-119">Requirement</span></span> | <span data-ttu-id="7dbf5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dbf5-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7dbf5-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dbf5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7dbf5-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dbf5-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7dbf5-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dbf5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7dbf5-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dbf5-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7dbf5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7dbf5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dbf5-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dbf5-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7dbf5-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7dbf5-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="7dbf5-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7dbf5-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7dbf5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7dbf5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dbf5-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dbf5-130"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dbf5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dbf5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dbf5-132">FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="7dbf5-132">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="7dbf5-133">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="7dbf5-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




