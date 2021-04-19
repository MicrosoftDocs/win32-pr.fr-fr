---
description: La méthode IsClassID détermine si un CLSID correspond à ce modèle de classe.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Méthode CFactoryTemplate. IsClassID (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530989"
---
# <a name="cfactorytemplateisclassid-method"></a><span data-ttu-id="10f58-103">Méthode CFactoryTemplate. IsClassID</span><span class="sxs-lookup"><span data-stu-id="10f58-103">CFactoryTemplate.IsClassID method</span></span>

<span data-ttu-id="10f58-104">La `IsClassID` méthode détermine si un CLSID correspond à ce modèle de classe.</span><span class="sxs-lookup"><span data-stu-id="10f58-104">The `IsClassID` method determines whether a CLSID matches this class template.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f58-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10f58-105">Syntax</span></span>


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="10f58-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10f58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10f58-107">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="10f58-107">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="10f58-108">Référence à un CLSID.</span><span class="sxs-lookup"><span data-stu-id="10f58-108">Reference to a CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10f58-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10f58-109">Return value</span></span>

<span data-ttu-id="10f58-110">Retourne la **valeur true** si le paramètre *rclsid* est le même CLSID que la variable membre [**CFactoryTemplate :: m \_ CLSID**](cfactorytemplate-m-clsid.md) , ou sinon retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="10f58-110">Returns **TRUE** if the *rclsid* parameter is the same CLSID as the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable, or else returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="10f58-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10f58-111">Requirements</span></span>



| <span data-ttu-id="10f58-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10f58-112">Requirement</span></span> | <span data-ttu-id="10f58-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="10f58-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f58-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="10f58-114">Header</span></span><br/>  | <dl> <span data-ttu-id="10f58-115"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10f58-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="10f58-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="10f58-116">Library</span></span><br/> | <dl> <span data-ttu-id="10f58-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="10f58-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10f58-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10f58-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f58-119">**CFactoryTemplate, classe**</span><span class="sxs-lookup"><span data-stu-id="10f58-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




