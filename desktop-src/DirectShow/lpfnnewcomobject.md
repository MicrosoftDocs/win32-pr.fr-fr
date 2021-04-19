---
description: Pointeur vers une fonction qui crée une instance de l’objet.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Pointeur de fonction LPFNNewCOMObject (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 07c0f8ab961c872c9dc0f92d2fff519b94cd049e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543251"
---
# <a name="lpfnnewcomobject-function-pointer"></a><span data-ttu-id="733ab-103">Pointeur de fonction LPFNNewCOMObject</span><span class="sxs-lookup"><span data-stu-id="733ab-103">LPFNNewCOMObject function pointer</span></span>

<span data-ttu-id="733ab-104">Pointeur vers une fonction qui crée une instance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="733ab-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="733ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="733ab-105">Syntax</span></span>


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="733ab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="733ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733ab-107">*pUnkOuter*</span><span class="sxs-lookup"><span data-stu-id="733ab-107">*pUnkOuter*</span></span> 
</dt> <dd>

<span data-ttu-id="733ab-108">Pointeur vers l’interface **IUnknown** de l’objet qui agrège le nouvel objet, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="733ab-108">Pointer to the **IUnknown** interface of the object that aggregates the new object, if any.</span></span> <span data-ttu-id="733ab-109">Ce pointeur peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="733ab-109">This pointer can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="733ab-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="733ab-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="733ab-111">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="733ab-111">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="733ab-112">Si le constructeur échoue, ce paramètre reçoit un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="733ab-112">If the constructor fails, this parameter receives an error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733ab-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="733ab-113">Return value</span></span>

<span data-ttu-id="733ab-114">Retourne un pointeur vers une nouvelle instance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="733ab-114">Returns a pointer to a new instance of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="733ab-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="733ab-115">Requirements</span></span>



| <span data-ttu-id="733ab-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="733ab-116">Requirement</span></span> | <span data-ttu-id="733ab-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="733ab-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="733ab-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="733ab-118">Header</span></span><br/> | <dl> <span data-ttu-id="733ab-119"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="733ab-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733ab-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="733ab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733ab-121">**CFactoryTemplate, classe**</span><span class="sxs-lookup"><span data-stu-id="733ab-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




