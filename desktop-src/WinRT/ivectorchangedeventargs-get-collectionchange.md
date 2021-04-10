---
description: Obtient le type de modification qui s’est produite dans le vecteur.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'IVectorChangedEventArgs :: get_CollectionChange, méthode (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201442"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a><span data-ttu-id="4d346-103">IVectorChangedEventArgs :: obten, \_ méthode CollectionChange</span><span class="sxs-lookup"><span data-stu-id="4d346-103">IVectorChangedEventArgs::get\_CollectionChange method</span></span>

<span data-ttu-id="4d346-104">Obtient le type de modification qui s’est produite dans le vecteur.</span><span class="sxs-lookup"><span data-stu-id="4d346-104">Gets the type of change that occurred in the vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d346-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d346-105">Syntax</span></span>


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a><span data-ttu-id="4d346-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d346-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d346-107">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4d346-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4d346-108">Type : \**CollectionChange \** _</span><span class="sxs-lookup"><span data-stu-id="4d346-108">Type: \**CollectionChange\** _</span></span>

<span data-ttu-id="4d346-109">Valeur de l’énumération [_ *CollectionChange* \*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) qui décrit la modification.</span><span class="sxs-lookup"><span data-stu-id="4d346-109">A value from the [_ *CollectionChange*\*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) enumeration that describes the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d346-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d346-110">Return value</span></span>

<span data-ttu-id="4d346-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4d346-111">Type: **HRESULT**</span></span>

<span data-ttu-id="4d346-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4d346-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d346-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d346-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d346-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d346-114">Requirements</span></span>



| <span data-ttu-id="4d346-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d346-115">Requirement</span></span> | <span data-ttu-id="4d346-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d346-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d346-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d346-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4d346-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4d346-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="4d346-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d346-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4d346-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d346-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="4d346-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d346-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d346-122"><dt>IVectorChangedEventArgs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d346-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d346-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d346-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d346-124">**IVectorChangedEventArgs**</span><span class="sxs-lookup"><span data-stu-id="4d346-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 
