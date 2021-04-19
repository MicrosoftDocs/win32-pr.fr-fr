---
description: Vérifie que le processus appelant dispose d’un accès en lecture à une chaîne. Si ce n’est pas le cas, la macro appelle la macro DbgBreak.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: ValidateStringPtr macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 19bf0b9e43ecbbbdea0e11284cd1cb4a058e22cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530029"
---
# <a name="validatestringptr-macro"></a><span data-ttu-id="239dc-104">ValidateStringPtr macro)</span><span class="sxs-lookup"><span data-stu-id="239dc-104">ValidateStringPtr macro</span></span>

<span data-ttu-id="239dc-105">Vérifie que le processus appelant dispose d’un accès en lecture à une chaîne.</span><span class="sxs-lookup"><span data-stu-id="239dc-105">Verifies that the calling process has read access to a string.</span></span> <span data-ttu-id="239dc-106">Si ce n’est pas le cas, la macro appelle la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="239dc-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="239dc-107">Cette macro est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="239dc-107">This macro is deprecated.</span></span> <span data-ttu-id="239dc-108">Dans le SDK Windows pour Windows Vista (et versions ultérieures), cette macro ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="239dc-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="239dc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="239dc-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="239dc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="239dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="239dc-111">*p*</span><span class="sxs-lookup"><span data-stu-id="239dc-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="239dc-112">Pointeur vers une chaîne **TCHAR** terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="239dc-112">Pointer to a NULL-terminated **TCHAR** string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="239dc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="239dc-113">Return value</span></span>

<span data-ttu-id="239dc-114">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="239dc-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="239dc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="239dc-115">Remarks</span></span>

<span data-ttu-id="239dc-116">Cette macro est ignorée sauf si DEBUG, \_ Debug ou VFWROBUST est défini lorsque le fichier d’en-tête de classe de base DirectShow est inclus.</span><span class="sxs-lookup"><span data-stu-id="239dc-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="239dc-117">Cette macro peut avoir un impact significatif sur les performances.</span><span class="sxs-lookup"><span data-stu-id="239dc-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="239dc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="239dc-118">Requirements</span></span>



| <span data-ttu-id="239dc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="239dc-119">Requirement</span></span> | <span data-ttu-id="239dc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="239dc-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239dc-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="239dc-121">Header</span></span><br/> | <dl> <span data-ttu-id="239dc-122"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="239dc-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239dc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="239dc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239dc-124">Macros de validation du pointeur</span><span class="sxs-lookup"><span data-stu-id="239dc-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




