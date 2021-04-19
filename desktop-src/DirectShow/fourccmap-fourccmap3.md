---
description: Méthode de constructeur qui fournit le mappage entre les types DWORD de format multimédia anciens et les sous-types de GUID. Cette méthode utilise le paramètre « pguid ».
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-paramètre pguid'
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
ms.openlocfilehash: 3e36f0ea58c99930d4c6c2e0929f27a43184c6be
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106539172"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a><span data-ttu-id="83fdf-104">FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-paramètre pguid</span><span class="sxs-lookup"><span data-stu-id="83fdf-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - pguid parameter</span></span>

<span data-ttu-id="83fdf-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="83fdf-105">Constructor method.</span></span> <span data-ttu-id="83fdf-106">Le constructeur fournit le mappage entre les types **DWORD** de format multimédia anciens et les sous-types de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="83fdf-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="83fdf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83fdf-107">Syntax</span></span>


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="83fdf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83fdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83fdf-109">*pguid*</span><span class="sxs-lookup"><span data-stu-id="83fdf-109">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="83fdf-110">Pointeur vers l’identificateur global unique (**GUID**).</span><span class="sxs-lookup"><span data-stu-id="83fdf-110">Pointer to the globally unique identifier (**GUID**).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83fdf-111">Notes</span><span class="sxs-lookup"><span data-stu-id="83fdf-111">Remarks</span></span>

<span data-ttu-id="83fdf-112">Si cet objet est construit avec le code **FourCC** , un **GUID** est créé pour le faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="83fdf-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="83fdf-113">Si cet objet est créé avec un **GUID** existant, la valeur **FourCC** de l’objet est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="83fdf-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="83fdf-114">Par la suite, la valeur **FourCC** peut être définie ou récupérée à l’aide des fonctions membres [**SetFOURCC**](fourccmap-setfourcc.md) et [**GetFOURCC**](fourccmap-getfourcc.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="83fdf-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="83fdf-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83fdf-115">Requirements</span></span>

| <span data-ttu-id="83fdf-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83fdf-116">Requirement</span></span> | <span data-ttu-id="83fdf-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="83fdf-117">Value</span></span> |
|-|-|
| <span data-ttu-id="83fdf-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="83fdf-118">Header</span></span>  | <span data-ttu-id="83fdf-119">FourCC. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="83fdf-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="83fdf-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="83fdf-120">Library</span></span> | <span data-ttu-id="83fdf-121">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="83fdf-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="83fdf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83fdf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83fdf-123">**FOURCCMap, classe**</span><span class="sxs-lookup"><span data-stu-id="83fdf-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




