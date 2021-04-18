---
description: Cet opérateur ajoute deux heures de référence.
ms.assetid: 4dfc087a-ec4f-4a8a-8bd4-4da9e1699bcd
title: COARefTime. Operator +, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a6f5019c61d4c1baec47652db8842aa5085b675
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543246"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="8e341-103">COARefTime. Operator +, méthode</span><span class="sxs-lookup"><span data-stu-id="8e341-103">COARefTime.operator+ method</span></span>

<span data-ttu-id="8e341-104">Cet opérateur ajoute deux heures de référence.</span><span class="sxs-lookup"><span data-stu-id="8e341-104">This operator adds two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e341-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e341-105">Syntax</span></span>


```C++
COARefTime operator+(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="8e341-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e341-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e341-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="8e341-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8e341-108">Référence à l’objet **COARefTime** à ajouter.</span><span class="sxs-lookup"><span data-stu-id="8e341-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e341-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e341-109">Return value</span></span>

<span data-ttu-id="8e341-110">Retourne un nouvel objet **COARefTime** égal à la somme des heures de référence.</span><span class="sxs-lookup"><span data-stu-id="8e341-110">Returns a new **COARefTime** object equal to the sum of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e341-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e341-111">Requirements</span></span>



| <span data-ttu-id="8e341-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e341-112">Requirement</span></span> | <span data-ttu-id="8e341-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e341-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e341-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e341-114">Header</span></span><br/>  | <dl> <span data-ttu-id="8e341-115"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e341-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8e341-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8e341-116">Library</span></span><br/> | <dl> <span data-ttu-id="8e341-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8e341-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e341-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e341-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e341-119">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="8e341-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




