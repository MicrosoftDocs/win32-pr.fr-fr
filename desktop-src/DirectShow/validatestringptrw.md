---
description: Vérifie que le processus appelant dispose d’un accès en lecture à une chaîne de caractères larges. Si ce n’est pas le cas, la macro appelle la macro DbgBreak.
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: ValidateStringPtrW macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrW
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1ece2caa0f2263c038121cd1ffd031cbe42d336a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542778"
---
# <a name="validatestringptrw-macro"></a><span data-ttu-id="dff64-104">ValidateStringPtrW macro)</span><span class="sxs-lookup"><span data-stu-id="dff64-104">ValidateStringPtrW macro</span></span>

<span data-ttu-id="dff64-105">Vérifie que le processus appelant dispose d’un accès en lecture à une chaîne de caractères larges.</span><span class="sxs-lookup"><span data-stu-id="dff64-105">Verifies that the calling process has read access to a wide-character string.</span></span> <span data-ttu-id="dff64-106">Si ce n’est pas le cas, la macro appelle la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="dff64-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="dff64-107">Cette macro est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dff64-107">This macro is deprecated.</span></span> <span data-ttu-id="dff64-108">Dans le SDK Windows pour Windows Vista (et versions ultérieures), cette macro ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="dff64-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="dff64-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dff64-109">Syntax</span></span>


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="dff64-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dff64-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff64-111">*p*</span><span class="sxs-lookup"><span data-stu-id="dff64-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="dff64-112">Pointeur vers une chaîne de caractères larges se terminant par NULL.</span><span class="sxs-lookup"><span data-stu-id="dff64-112">Pointer to a NULL-terminated wide-character string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dff64-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dff64-113">Return value</span></span>

<span data-ttu-id="dff64-114">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dff64-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dff64-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dff64-115">Remarks</span></span>

<span data-ttu-id="dff64-116">Cette macro est ignorée sauf si DEBUG, \_ Debug ou VFWROBUST est défini lorsque le fichier d’en-tête de classe de base DirectShow est inclus.</span><span class="sxs-lookup"><span data-stu-id="dff64-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="dff64-117">Cette macro peut avoir un impact significatif sur les performances.</span><span class="sxs-lookup"><span data-stu-id="dff64-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="dff64-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dff64-118">Requirements</span></span>



| <span data-ttu-id="dff64-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dff64-119">Requirement</span></span> | <span data-ttu-id="dff64-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dff64-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dff64-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="dff64-121">Header</span></span><br/> | <dl> <span data-ttu-id="dff64-122"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dff64-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dff64-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dff64-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff64-124">Macros de validation du pointeur</span><span class="sxs-lookup"><span data-stu-id="dff64-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




