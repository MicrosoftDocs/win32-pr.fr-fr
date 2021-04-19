---
description: La \_ structure de filtre AMOVIESETUP contient des informations sur l’inscription d’un filtre.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: Structure AMOVIESETUP_FILTER (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535339"
---
# <a name="amoviesetup_filter-structure"></a><span data-ttu-id="c1fbb-103">\_Structure de filtre AMOVIESETUP</span><span class="sxs-lookup"><span data-stu-id="c1fbb-103">AMOVIESETUP\_FILTER structure</span></span>

<span data-ttu-id="c1fbb-104">La structure de **\_ filtre AMOVIESETUP** contient des informations sur l’inscription d’un filtre.</span><span class="sxs-lookup"><span data-stu-id="c1fbb-104">The **AMOVIESETUP\_FILTER** structure contains information for registering a filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1fbb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1fbb-105">Syntax</span></span>


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a><span data-ttu-id="c1fbb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c1fbb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1fbb-107">**Identificateur**</span><span class="sxs-lookup"><span data-stu-id="c1fbb-107">**clsID**</span></span>
</dt> <dd>

<span data-ttu-id="c1fbb-108">Identificateur de classe du filtre.</span><span class="sxs-lookup"><span data-stu-id="c1fbb-108">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="c1fbb-109">**strName**</span><span class="sxs-lookup"><span data-stu-id="c1fbb-109">**strName**</span></span>
</dt> <dd>

<span data-ttu-id="c1fbb-110">Nom du filtre.</span><span class="sxs-lookup"><span data-stu-id="c1fbb-110">Name of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="c1fbb-111">**dwMerit**</span><span class="sxs-lookup"><span data-stu-id="c1fbb-111">**dwMerit**</span></span>
</dt> <dd>

<span data-ttu-id="c1fbb-112">Mérite de filtre.</span><span class="sxs-lookup"><span data-stu-id="c1fbb-112">Filter merit.</span></span> <span data-ttu-id="c1fbb-113">Utilisé par l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) lors de la construction d’un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c1fbb-113">Used by the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface when constructing a filter graph.</span></span> <span data-ttu-id="c1fbb-114">Pour obtenir la liste des valeurs mérites, consultez [mérite](merit.md).</span><span class="sxs-lookup"><span data-stu-id="c1fbb-114">For a list of merit values, see [Merit](merit.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1fbb-115">**nPins**</span><span class="sxs-lookup"><span data-stu-id="c1fbb-115">**nPins**</span></span>
</dt> <dd>

<span data-ttu-id="c1fbb-116">Nombre d’éléments dans le tableau *lpPin* .</span><span class="sxs-lookup"><span data-stu-id="c1fbb-116">Number of elements in the *lpPin* array.</span></span> <span data-ttu-id="c1fbb-117">Si *lpPin* a la **valeur null**, affectez la valeur zéro à ce membre.</span><span class="sxs-lookup"><span data-stu-id="c1fbb-117">If *lpPin* is **NULL**, set this member to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1fbb-118">**lpPin**</span><span class="sxs-lookup"><span data-stu-id="c1fbb-118">**lpPin**</span></span>
</dt> <dd>

<span data-ttu-id="c1fbb-119">Pointeur vers un tableau de structures [**AMOVIESETUP \_ pin**](amoviesetup-pin.md) , de taille *nPins*.</span><span class="sxs-lookup"><span data-stu-id="c1fbb-119">Pointer to an array of [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structures, of size *nPins*.</span></span> <span data-ttu-id="c1fbb-120">Chaque membre de ce tableau décrit un code confidentiel sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="c1fbb-120">Each member of this array describes a pin on the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1fbb-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c1fbb-121">Remarks</span></span>

<span data-ttu-id="c1fbb-122">Pour plus d’informations sur l’utilisation de cette structure, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="c1fbb-122">For information about using this structure, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="c1fbb-123">Utilisez cette structure uniquement pour les filtres qui sont enregistrés dans la catégorie de filtre par défaut (CLSID \_ LegacyAmFilterCategory).</span><span class="sxs-lookup"><span data-stu-id="c1fbb-123">Use this structure only for filters that are registered in the default filter category (CLSID\_LegacyAmFilterCategory).</span></span> <span data-ttu-id="c1fbb-124">Pour inscrire un filtre dans une autre catégorie, utilisez la méthode [**IFilterMapper2 :: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) , comme décrit dans [implémentation de DllRegisterServer](implementing-dllregisterserver.md).</span><span class="sxs-lookup"><span data-stu-id="c1fbb-124">To register a filter in a different category, use the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method, as described in [Implementing DllRegisterServer](implementing-dllregisterserver.md).</span></span>

> [!Note]  
> <span data-ttu-id="c1fbb-125">Le fichier d’en-tête ComBase. h est fourni avec les [classes de base DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c1fbb-125">The header file combase.h is provided with the [DirectShow Base Classes](directshow-base-classes.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1fbb-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1fbb-126">Requirements</span></span>



| <span data-ttu-id="c1fbb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1fbb-127">Requirement</span></span> | <span data-ttu-id="c1fbb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1fbb-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fbb-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1fbb-129">Header</span></span><br/> | <dl> <span data-ttu-id="c1fbb-130"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1fbb-130"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1fbb-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1fbb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1fbb-132">Structures DirectShow</span><span class="sxs-lookup"><span data-stu-id="c1fbb-132">DirectShow Structures</span></span>](directshow-structures.md)
</dt> </dl>

 

 




