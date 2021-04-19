---
description: Vérifie que le processus appelant dispose d’un accès en lecture à une chaîne ANSI. Si ce n’est pas le cas, la macro appelle la macro DbgBreak.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: ValidateStringPtrA macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 94ce34393ec494f34cce621afc168a4d6bbe4325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530028"
---
# <a name="validatestringptra-macro"></a><span data-ttu-id="410e3-104">ValidateStringPtrA macro)</span><span class="sxs-lookup"><span data-stu-id="410e3-104">ValidateStringPtrA macro</span></span>

<span data-ttu-id="410e3-105">Vérifie que le processus appelant dispose d’un accès en lecture à une chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="410e3-105">Verifies that the calling process has read access to an ANSI string.</span></span> <span data-ttu-id="410e3-106">Si ce n’est pas le cas, la macro appelle la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="410e3-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="410e3-107">Cette macro est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="410e3-107">This macro is deprecated.</span></span> <span data-ttu-id="410e3-108">Dans le SDK Windows pour Windows Vista (et versions ultérieures), cette macro ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="410e3-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="410e3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="410e3-109">Syntax</span></span>


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="410e3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="410e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="410e3-111">*p*</span><span class="sxs-lookup"><span data-stu-id="410e3-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="410e3-112">Pointeur vers une chaîne ANSI terminée par le caractère NULL.</span><span class="sxs-lookup"><span data-stu-id="410e3-112">Pointer to a NULL-terminated ANSI string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="410e3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="410e3-113">Return value</span></span>

<span data-ttu-id="410e3-114">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="410e3-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="410e3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="410e3-115">Remarks</span></span>

<span data-ttu-id="410e3-116">Cette macro est ignorée sauf si DEBUG, \_ Debug ou VFWROBUST est défini lorsque le fichier d’en-tête de classe de base DirectShow est inclus.</span><span class="sxs-lookup"><span data-stu-id="410e3-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span>

## <a name="requirements"></a><span data-ttu-id="410e3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="410e3-117">Requirements</span></span>



| <span data-ttu-id="410e3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="410e3-118">Requirement</span></span> | <span data-ttu-id="410e3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="410e3-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="410e3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="410e3-120">Header</span></span><br/> | <dl> <span data-ttu-id="410e3-121"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="410e3-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="410e3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="410e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410e3-123">Macros de validation du pointeur</span><span class="sxs-lookup"><span data-stu-id="410e3-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




