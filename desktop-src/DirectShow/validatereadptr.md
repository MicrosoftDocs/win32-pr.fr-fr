---
description: Vérifie que le processus appelant dispose d’un accès en lecture à un bloc de mémoire. Si ce n’est pas le cas, la macro appelle la macro DbgBreak.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: ValidateReadPtr macro (Wxdebug. h)
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
ms.openlocfilehash: aa8093ecbd428cafbf1266179b1489cac0d69c4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543956"
---
# <a name="validatereadptr-macro"></a><span data-ttu-id="e1f43-104">ValidateReadPtr macro)</span><span class="sxs-lookup"><span data-stu-id="e1f43-104">ValidateReadPtr macro</span></span>

<span data-ttu-id="e1f43-105">Vérifie que le processus appelant dispose d’un accès en lecture à un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e1f43-105">Verifies that the calling process has read access to a memory block.</span></span> <span data-ttu-id="e1f43-106">Si ce n’est pas le cas, la macro appelle la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="e1f43-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="e1f43-107">Cette macro est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e1f43-107">This macro is deprecated.</span></span> <span data-ttu-id="e1f43-108">Dans le SDK Windows pour Windows Vista (et versions ultérieures), cette macro ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="e1f43-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e1f43-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1f43-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="e1f43-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1f43-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1f43-111">*p*</span><span class="sxs-lookup"><span data-stu-id="e1f43-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="e1f43-112">Pointeur vers un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e1f43-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="e1f43-113">*libéré*</span><span class="sxs-lookup"><span data-stu-id="e1f43-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="e1f43-114">Taille du bloc de mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="e1f43-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1f43-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1f43-115">Return value</span></span>

<span data-ttu-id="e1f43-116">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e1f43-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1f43-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e1f43-117">Remarks</span></span>

<span data-ttu-id="e1f43-118">Cette macro est ignorée sauf si DEBUG, \_ Debug ou VFWROBUST est défini lorsque le fichier d’en-tête de classe de base DirectShow est inclus.</span><span class="sxs-lookup"><span data-stu-id="e1f43-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="e1f43-119">Cette macro peut avoir un impact significatif sur les performances.</span><span class="sxs-lookup"><span data-stu-id="e1f43-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f43-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1f43-120">Requirements</span></span>



| <span data-ttu-id="e1f43-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1f43-121">Requirement</span></span> | <span data-ttu-id="e1f43-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1f43-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f43-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1f43-123">Header</span></span><br/> | <dl> <span data-ttu-id="e1f43-124"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1f43-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f43-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1f43-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f43-126">Macros de validation du pointeur</span><span class="sxs-lookup"><span data-stu-id="e1f43-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




