---
description: Méthode de constructeur qui fournit le mappage entre les types DWORD de format multimédia anciens et les sous-types de GUID. Cette méthode utilise le paramètre « FourCC ».
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-paramètre FourCC'
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
ms.openlocfilehash: cbcd5e8a7c37d3265f508ac7632ffd4b18c8a00f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106531383"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a><span data-ttu-id="3e24a-104">FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-paramètre FourCC</span><span class="sxs-lookup"><span data-stu-id="3e24a-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - Fourcc parameter</span></span>

<span data-ttu-id="3e24a-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="3e24a-105">Constructor method.</span></span> <span data-ttu-id="3e24a-106">Le constructeur fournit le mappage entre les types **DWORD** de format multimédia anciens et les sous-types de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="3e24a-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e24a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e24a-107">Syntax</span></span>


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a><span data-ttu-id="3e24a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e24a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e24a-109">*FourCC*</span><span class="sxs-lookup"><span data-stu-id="3e24a-109">*Fourcc*</span></span> 
</dt> <dd>

<span data-ttu-id="3e24a-110">**Valeur DWORD** qui spécifie le FourCC.</span><span class="sxs-lookup"><span data-stu-id="3e24a-110">**DWORD** that specifies the FOURCC.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e24a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3e24a-111">Remarks</span></span>

<span data-ttu-id="3e24a-112">Si cet objet est construit avec le code **FourCC** , un **GUID** est créé pour le faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="3e24a-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="3e24a-113">Si cet objet est créé avec un **GUID** existant, la valeur **FourCC** de l’objet est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="3e24a-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="3e24a-114">Par la suite, la valeur **FourCC** peut être définie ou récupérée à l’aide des fonctions membres [**SetFOURCC**](fourccmap-setfourcc.md) et [**GetFOURCC**](fourccmap-getfourcc.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="3e24a-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e24a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e24a-115">Requirements</span></span>

| <span data-ttu-id="3e24a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e24a-116">Requirement</span></span> | <span data-ttu-id="3e24a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e24a-117">Value</span></span> |
|-|-|
| <span data-ttu-id="3e24a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e24a-118">Header</span></span>  | <span data-ttu-id="3e24a-119">FourCC. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="3e24a-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="3e24a-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3e24a-120">Library</span></span> | <span data-ttu-id="3e24a-121">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="3e24a-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="3e24a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e24a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e24a-123">**FOURCCMap, classe**</span><span class="sxs-lookup"><span data-stu-id="3e24a-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




