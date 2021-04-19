---
description: Vérifie que le processus appelant dispose d’un accès en lecture/écriture à un bloc de mémoire. Si ce n’est pas le cas, la macro appelle la macro DbgBreak.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: ValidateReadWritePtr macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: b551f3c72a2480ea1f160b2b384fe87dbede51f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538158"
---
# <a name="validatereadwriteptr-macro"></a><span data-ttu-id="0f473-104">ValidateReadWritePtr macro)</span><span class="sxs-lookup"><span data-stu-id="0f473-104">ValidateReadWritePtr macro</span></span>

<span data-ttu-id="0f473-105">Vérifie que le processus appelant dispose d’un accès en lecture/écriture à un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0f473-105">Verifies that the calling process has read/write access to a memory block.</span></span> <span data-ttu-id="0f473-106">Si ce n’est pas le cas, la macro appelle la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="0f473-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="0f473-107">Cette macro est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0f473-107">This macro is deprecated.</span></span> <span data-ttu-id="0f473-108">Dans le SDK Windows pour Windows Vista (et versions ultérieures), cette macro ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="0f473-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0f473-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f473-109">Syntax</span></span>


```C++
void ValidateReadWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="0f473-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f473-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f473-111">*p*</span><span class="sxs-lookup"><span data-stu-id="0f473-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="0f473-112">Pointeur vers un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0f473-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="0f473-113">*libéré*</span><span class="sxs-lookup"><span data-stu-id="0f473-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="0f473-114">Taille du bloc de mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="0f473-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f473-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f473-115">Return value</span></span>

<span data-ttu-id="0f473-116">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0f473-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f473-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0f473-117">Remarks</span></span>

<span data-ttu-id="0f473-118">Cette macro est ignorée sauf si DEBUG, \_ Debug ou VFWROBUST est défini lorsque le fichier d’en-tête de classe de base DirectShow est inclus.</span><span class="sxs-lookup"><span data-stu-id="0f473-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="0f473-119">Cette macro peut avoir un impact significatif sur les performances.</span><span class="sxs-lookup"><span data-stu-id="0f473-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f473-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f473-120">Requirements</span></span>



| <span data-ttu-id="0f473-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f473-121">Requirement</span></span> | <span data-ttu-id="0f473-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f473-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f473-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f473-123">Header</span></span><br/> | <dl> <span data-ttu-id="0f473-124"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f473-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f473-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f473-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f473-126">Macros de validation du pointeur</span><span class="sxs-lookup"><span data-stu-id="0f473-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




