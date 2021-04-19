---
description: Spécifie la valeur supposée par une propriété à un moment donné.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: Structure DEXTER_PARAM (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535258"
---
# <a name="dexter_param-structure"></a><span data-ttu-id="fe3bd-103">\_Structure de paramètre Dexter</span><span class="sxs-lookup"><span data-stu-id="fe3bd-103">DEXTER\_PARAM structure</span></span>

> [!Note]  
> <span data-ttu-id="fe3bd-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-104">\[Deprecated.</span></span> <span data-ttu-id="fe3bd-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fe3bd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fe3bd-106">Spécifie la valeur supposée par une propriété à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-106">Specifies the value that a property assumes at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3bd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe3bd-107">Syntax</span></span>


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a><span data-ttu-id="fe3bd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fe3bd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe3bd-109">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-109">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="fe3bd-110">Nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-110">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="fe3bd-111">**Égal**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-111">**dispID**</span></span>
</dt> <dd>

<span data-ttu-id="fe3bd-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-112">Reserved.</span></span> <span data-ttu-id="fe3bd-113">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-113">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fe3bd-114">**Nvaleurs**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-114">**nValues**</span></span>
</dt> <dd>

<span data-ttu-id="fe3bd-115">Nombre de valeurs supposées par la propriété.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-115">Number of values that the property assumes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe3bd-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fe3bd-116">Remarks</span></span>

<span data-ttu-id="fe3bd-117">L’objet doit prendre en charge l’interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="fe3bd-117">The object must support the **IDispatch** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe3bd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe3bd-118">Requirements</span></span>



| <span data-ttu-id="fe3bd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe3bd-119">Requirement</span></span> | <span data-ttu-id="fe3bd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe3bd-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3bd-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe3bd-121">Header</span></span><br/> | <dl> <span data-ttu-id="fe3bd-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe3bd-122"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe3bd-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe3bd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3bd-124">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-124">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-125">**valeur de DEXTERity \_**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-125">**DEXTER\_VALUE**</span></span>](dexter-value.md)
</dt> </dl>

 

 




