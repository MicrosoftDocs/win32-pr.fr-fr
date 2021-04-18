---
description: Méthode de constructeur.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Constructeur CUnknown. CUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b500e7f12a2242b6c05367bc061f50680d2d608b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532800"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="aecef-103">Constructeur CUnknown. CUnknown</span><span class="sxs-lookup"><span data-stu-id="aecef-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="aecef-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="aecef-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aecef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aecef-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="aecef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aecef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aecef-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="aecef-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="aecef-108">Chaîne contenant le nom de l’objet. utilisé dans le constructeur [**CBaseObject**](cbaseobject.md) pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="aecef-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="aecef-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="aecef-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="aecef-110">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="aecef-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="aecef-111">Si l’objet est agrégé, passer un pointeur vers l’interface IUnknown de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="aecef-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="aecef-112">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="aecef-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aecef-113">Notes</span><span class="sxs-lookup"><span data-stu-id="aecef-113">Remarks</span></span>

<span data-ttu-id="aecef-114">L’objet est initialisé avec un nombre de références égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="aecef-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="aecef-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aecef-115">Requirements</span></span>



| <span data-ttu-id="aecef-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aecef-116">Requirement</span></span> | <span data-ttu-id="aecef-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aecef-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aecef-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="aecef-118">Header</span></span><br/>  | <dl> <span data-ttu-id="aecef-119"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aecef-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aecef-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aecef-120">Library</span></span><br/> | <dl> <span data-ttu-id="aecef-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="aecef-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




