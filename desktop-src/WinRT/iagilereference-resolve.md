---
description: Obtient l’ID d’interface d’une référence agile à un objet.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'IAgileReference :: Resolve, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544662"
---
# <a name="iagilereferenceresolve-method"></a><span data-ttu-id="b75d0-103">IAgileReference :: Resolve, méthode</span><span class="sxs-lookup"><span data-stu-id="b75d0-103">IAgileReference::Resolve method</span></span>

<span data-ttu-id="b75d0-104">Obtient l’ID d’interface d’une référence agile à un objet.</span><span class="sxs-lookup"><span data-stu-id="b75d0-104">Gets the interface ID of an agile reference to an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b75d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b75d0-105">Syntax</span></span>


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a><span data-ttu-id="b75d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b75d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b75d0-107">*riid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b75d0-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b75d0-108">ID d’interface de l’interface à récupérer à partir de la référence agile.</span><span class="sxs-lookup"><span data-stu-id="b75d0-108">The interface ID of the interface to be retrieved from the agile reference.</span></span> <span data-ttu-id="b75d0-109">Il n’est pas nécessaire qu’il soit identique à l’interface inscrite.</span><span class="sxs-lookup"><span data-stu-id="b75d0-109">It is not required to be the same as the registered interface.</span></span>

</dd> <dt>

<span data-ttu-id="b75d0-110">*ppvObjectReference* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b75d0-110">*ppvObjectReference* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b75d0-111">Une fois l’opération terminée, \* *ppvObjectReference* est un pointeur vers l’interface spécifiée par *riid*.</span><span class="sxs-lookup"><span data-stu-id="b75d0-111">On successful completion, \**ppvObjectReference* is a pointer to the interface specified by *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b75d0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b75d0-112">Return value</span></span>

<span data-ttu-id="b75d0-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b75d0-113">This method can return one of these values.</span></span>



| <span data-ttu-id="b75d0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b75d0-114">Return value</span></span>                                                                              | <span data-ttu-id="b75d0-115">Description</span><span class="sxs-lookup"><span data-stu-id="b75d0-115">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b75d0-116"><dt>\_OK</dt></span><span class="sxs-lookup"><span data-stu-id="b75d0-116"><dt>S\_OK</dt></span></span> </dl>          | <span data-ttu-id="b75d0-117">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="b75d0-117">The method completed successfully.</span></span><br/>                                  |
| <dl> <span data-ttu-id="b75d0-118"><dt>E \_ NOinterface</dt></span><span class="sxs-lookup"><span data-stu-id="b75d0-118"><dt>E\_NOINTERFACE</dt></span></span> </dl> | <span data-ttu-id="b75d0-119">L’interface demandée n’est pas implémentée sur l’objet inscrit.</span><span class="sxs-lookup"><span data-stu-id="b75d0-119">The requested interface isn't implemented on the registered object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b75d0-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b75d0-120">Remarks</span></span>

<span data-ttu-id="b75d0-121">Appelez la fonction [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) pour créer une référence agile à un objet.</span><span class="sxs-lookup"><span data-stu-id="b75d0-121">Call the [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) function to create an agile reference to an object.</span></span> <span data-ttu-id="b75d0-122">Appelez la méthode **Resolve** pour localiser l’objet dans le cloisonnement dans lequel **Resolve** est appelé.</span><span class="sxs-lookup"><span data-stu-id="b75d0-122">Call the **Resolve** method to localize the object into the apartment in which **Resolve** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="b75d0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b75d0-123">Requirements</span></span>



| <span data-ttu-id="b75d0-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b75d0-124">Requirement</span></span> | <span data-ttu-id="b75d0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b75d0-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b75d0-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b75d0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b75d0-127">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b75d0-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>            |
| <span data-ttu-id="b75d0-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b75d0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b75d0-129">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b75d0-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b75d0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b75d0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75d0-131">**IAgileReference**</span><span class="sxs-lookup"><span data-stu-id="b75d0-131">**IAgileReference**</span></span>](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[<span data-ttu-id="b75d0-132">**RoGetAgileReference**</span><span class="sxs-lookup"><span data-stu-id="b75d0-132">**RoGetAgileReference**</span></span>](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




