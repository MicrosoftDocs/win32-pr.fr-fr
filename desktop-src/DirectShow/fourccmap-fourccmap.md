---
description: Méthode de constructeur qui fournit le mappage entre les types DWORD de format multimédia anciens et les sous-types de GUID. Cette méthode n’utilise aucun paramètre.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-aucun paramètre'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106537299"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a><span data-ttu-id="25994-104">FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-aucun paramètre</span><span class="sxs-lookup"><span data-stu-id="25994-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - No parameters</span></span>

<span data-ttu-id="25994-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="25994-105">Constructor method.</span></span> <span data-ttu-id="25994-106">Le constructeur fournit le mappage entre les types **DWORD** de format multimédia anciens et les sous-types de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="25994-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="25994-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25994-107">Syntax</span></span>


```C++
FOURCCMap();
```



## <a name="parameters"></a><span data-ttu-id="25994-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25994-108">Parameters</span></span>

<span data-ttu-id="25994-109">Ce constructeur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="25994-109">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="25994-110">Notes</span><span class="sxs-lookup"><span data-stu-id="25994-110">Remarks</span></span>

<span data-ttu-id="25994-111">Si cet objet est construit avec le code **FourCC** , un **GUID** est créé pour le faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="25994-111">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="25994-112">Si cet objet est créé avec un **GUID** existant, la valeur **FourCC** de l’objet est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="25994-112">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="25994-113">Par la suite, la valeur **FourCC** peut être définie ou récupérée à l’aide des fonctions membres [**SetFOURCC**](fourccmap-setfourcc.md) et [**GetFOURCC**](fourccmap-getfourcc.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="25994-113">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="25994-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25994-114">Requirements</span></span>


| <span data-ttu-id="25994-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25994-115">Requirement</span></span> | <span data-ttu-id="25994-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="25994-116">Value</span></span> |
|-|-|
| <span data-ttu-id="25994-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="25994-117">Header</span></span>  | <span data-ttu-id="25994-118">FourCC. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="25994-118">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="25994-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25994-119">Library</span></span> | <span data-ttu-id="25994-120">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="25994-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



## <a name="see-also"></a><span data-ttu-id="25994-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25994-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25994-122">**FOURCCMap, classe**</span><span class="sxs-lookup"><span data-stu-id="25994-122">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




