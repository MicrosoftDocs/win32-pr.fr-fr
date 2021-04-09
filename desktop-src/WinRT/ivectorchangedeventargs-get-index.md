---
description: Obtient la position dans le vecteur où la modification s’est produite.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'IVectorChangedEventArgs :: get_Index, méthode (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033988"
---
# <a name="ivectorchangedeventargsget_index-method"></a><span data-ttu-id="fadfb-103">IVectorChangedEventArgs :: obtient l' \_ index, méthode</span><span class="sxs-lookup"><span data-stu-id="fadfb-103">IVectorChangedEventArgs::get\_Index method</span></span>

<span data-ttu-id="fadfb-104">Obtient la position dans le vecteur où la modification s’est produite.</span><span class="sxs-lookup"><span data-stu-id="fadfb-104">Gets the position in the vector where the change occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="fadfb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fadfb-105">Syntax</span></span>


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a><span data-ttu-id="fadfb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fadfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fadfb-107">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fadfb-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fadfb-108">Tapez : \**unsigned \** _</span><span class="sxs-lookup"><span data-stu-id="fadfb-108">Type: \**unsigned\** _</span></span>

<span data-ttu-id="fadfb-109">Position de base zéro dans le vecteur où la modification s’est produite, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="fadfb-109">The zero-based position in the vector where the change occurred, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fadfb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fadfb-110">Return value</span></span>

<span data-ttu-id="fadfb-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="fadfb-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="fadfb-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fadfb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fadfb-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fadfb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fadfb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fadfb-114">Requirements</span></span>



| <span data-ttu-id="fadfb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fadfb-115">Requirement</span></span> | <span data-ttu-id="fadfb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fadfb-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fadfb-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fadfb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fadfb-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fadfb-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="fadfb-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fadfb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fadfb-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fadfb-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="fadfb-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="fadfb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fadfb-122"><dt>IVectorChangedEventArgs. h</dt></span><span class="sxs-lookup"><span data-stu-id="fadfb-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fadfb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fadfb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fadfb-124">**IVectorChangedEventArgs**</span><span class="sxs-lookup"><span data-stu-id="fadfb-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 




