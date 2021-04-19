---
description: 'Récupère un pointeur d’interface et incrémente le décompte de références. Cette méthode implémente la méthode INonDelegatingUnknown :: NonDelegatingQueryInterface.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Méthode CUnknown. NonDelegatingQueryInterface (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521682"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a><span data-ttu-id="982b1-104">Méthode CUnknown. NonDelegatingQueryInterface</span><span class="sxs-lookup"><span data-stu-id="982b1-104">CUnknown.NonDelegatingQueryInterface method</span></span>

<span data-ttu-id="982b1-105">Récupère un pointeur d’interface et incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="982b1-105">Retrieves an interface pointer and increments the reference count.</span></span> <span data-ttu-id="982b1-106">Cette méthode implémente la méthode **INonDelegatingUnknown :: NonDelegatingQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="982b1-106">This method implements the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="982b1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="982b1-107">Syntax</span></span>


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="982b1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="982b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="982b1-109">*riid*</span><span class="sxs-lookup"><span data-stu-id="982b1-109">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="982b1-110">Identificateur de l’interface.</span><span class="sxs-lookup"><span data-stu-id="982b1-110">Identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="982b1-111">*ppv*</span><span class="sxs-lookup"><span data-stu-id="982b1-111">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="982b1-112">Adresse d’un pointeur pour recevoir l’interface.</span><span class="sxs-lookup"><span data-stu-id="982b1-112">Address of a pointer to receive the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="982b1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="982b1-113">Return value</span></span>

<span data-ttu-id="982b1-114">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="982b1-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="982b1-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="982b1-115">Return code</span></span>                                                                                   | <span data-ttu-id="982b1-116">Description</span><span class="sxs-lookup"><span data-stu-id="982b1-116">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="982b1-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="982b1-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="982b1-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="982b1-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="982b1-119"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="982b1-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="982b1-120">L’objet ne prend pas en charge cette interface.</span><span class="sxs-lookup"><span data-stu-id="982b1-120">Object does not support this interface.</span></span><br/> |
| <dl> <span data-ttu-id="982b1-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="982b1-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="982b1-122">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="982b1-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="982b1-123">Notes</span><span class="sxs-lookup"><span data-stu-id="982b1-123">Remarks</span></span>

<span data-ttu-id="982b1-124">La classe **CUnknown** expose uniquement l’interface **IUknown** .</span><span class="sxs-lookup"><span data-stu-id="982b1-124">The **CUnknown** class exposes only the **IUknown** interface.</span></span> <span data-ttu-id="982b1-125">Substituez cette méthode pour exposer des interfaces supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="982b1-125">Override this method to expose additional interfaces.</span></span> <span data-ttu-id="982b1-126">Pour plus d’informations sur la façon de substituer cette méthode, consultez [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="982b1-126">For information on how to override this method, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="982b1-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="982b1-127">Requirements</span></span>



| <span data-ttu-id="982b1-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="982b1-128">Requirement</span></span> | <span data-ttu-id="982b1-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="982b1-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="982b1-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="982b1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="982b1-131"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="982b1-131"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="982b1-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="982b1-132">Library</span></span><br/> | <dl> <span data-ttu-id="982b1-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="982b1-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




