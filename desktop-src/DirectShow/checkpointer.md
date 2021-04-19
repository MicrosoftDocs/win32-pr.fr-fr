---
description: Vérifie si un pointeur est NULL. Si le pointeur est NULL, la fonction ou la méthode dans laquelle la macro apparaît retourne la valeur spécifiée.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro de point de contrôle (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538128"
---
# <a name="checkpointer-macro"></a><span data-ttu-id="1189f-104">Point de contrôle, macro</span><span class="sxs-lookup"><span data-stu-id="1189f-104">CheckPointer macro</span></span>

<span data-ttu-id="1189f-105">Vérifie si un pointeur est **null**.</span><span class="sxs-lookup"><span data-stu-id="1189f-105">Checks whether a pointer is **NULL**.</span></span> <span data-ttu-id="1189f-106">Si le pointeur est **null**, la fonction ou la méthode dans laquelle la macro apparaît retourne la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1189f-106">If the pointer is **NULL**, the function or method in which the macro appears returns the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1189f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1189f-107">Syntax</span></span>


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a><span data-ttu-id="1189f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1189f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1189f-109">*p*</span><span class="sxs-lookup"><span data-stu-id="1189f-109">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="1189f-110">Pointeur à vérifier.</span><span class="sxs-lookup"><span data-stu-id="1189f-110">Pointer to check.</span></span>

</dd> <dt>

<span data-ttu-id="1189f-111">*Av*</span><span class="sxs-lookup"><span data-stu-id="1189f-111">*ret*</span></span> 
</dt> <dd>

<span data-ttu-id="1189f-112">Valeur que la fonction ou la méthode retourne si *p* est **null**.</span><span class="sxs-lookup"><span data-stu-id="1189f-112">Value that the function or method returns if *p* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1189f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1189f-113">Return value</span></span>

<span data-ttu-id="1189f-114">La fonction environnante retourne *RET* si *p* est **null**.</span><span class="sxs-lookup"><span data-stu-id="1189f-114">The surrounding function returns *ret* if *p* is **NULL**.</span></span> <span data-ttu-id="1189f-115">Dans le cas contraire, la macro n’entraîne pas le retour de la fonction environnante.</span><span class="sxs-lookup"><span data-stu-id="1189f-115">Otherwise, the macro does not cause the surrounding function to return.</span></span>

## <a name="examples"></a><span data-ttu-id="1189f-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="1189f-116">Examples</span></span>


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a><span data-ttu-id="1189f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1189f-117">Requirements</span></span>



| <span data-ttu-id="1189f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1189f-118">Requirement</span></span> | <span data-ttu-id="1189f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1189f-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1189f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1189f-120">Header</span></span><br/> | <dl> <span data-ttu-id="1189f-121"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1189f-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1189f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1189f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1189f-123">Macros de validation du pointeur</span><span class="sxs-lookup"><span data-stu-id="1189f-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




