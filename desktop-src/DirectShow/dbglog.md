---
description: La macro DbgLog envoie une chaîne à l’emplacement de sortie de débogage, si la journalisation est activée pour le type et le niveau spécifiés. Cette macro est ignorée dans les versions commerciales.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: DbgLog macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537484"
---
# <a name="dbglog-macro"></a><span data-ttu-id="9c6b9-104">DbgLog macro)</span><span class="sxs-lookup"><span data-stu-id="9c6b9-104">DbgLog macro</span></span>

<span data-ttu-id="9c6b9-105">La macro **DbgLog** envoie une chaîne à l’emplacement de sortie de débogage, si la journalisation est activée pour le type et le niveau spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-105">The **DbgLog** macro sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> <span data-ttu-id="9c6b9-106">Cette macro est ignorée dans les versions commerciales.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-106">This macro is ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c6b9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c6b9-107">Syntax</span></span>


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
);
```



## <a name="parameters"></a><span data-ttu-id="9c6b9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c6b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c6b9-109">*Types*</span><span class="sxs-lookup"><span data-stu-id="9c6b9-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="9c6b9-110">Combinaison d’opérations de bits d’un ou plusieurs types de messages.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="9c6b9-111">*Niveau*</span><span class="sxs-lookup"><span data-stu-id="9c6b9-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="9c6b9-112">Niveau de journalisation pour ce message.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-112">Logging level for this message.</span></span>

</dd> <dt>

<span data-ttu-id="9c6b9-113">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="9c6b9-113">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="9c6b9-114">Chaîne de format **printf** -style.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-114">A **printf** -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="9c6b9-115">*...*</span><span class="sxs-lookup"><span data-stu-id="9c6b9-115">*...*</span></span> 
</dt> <dd>

<span data-ttu-id="9c6b9-116">Arguments supplémentaires pour la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-116">Additional arguments for the format string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c6b9-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c6b9-117">Return value</span></span>

<span data-ttu-id="9c6b9-118">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-118">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c6b9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9c6b9-119">Remarks</span></span>

<span data-ttu-id="9c6b9-120">Si la journalisation du débogage de l’un des types de messages est définie au niveau spécifié ou supérieur, cette macro envoie la chaîne mise en forme à l’emplacement de sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-120">If debug logging for any of the message types is set to the specified level or higher, this macro sends the formatted string to the debug output location.</span></span>

<span data-ttu-id="9c6b9-121">La macro ajoute automatiquement un caractère de saut de ligne à la chaîne de sortie.</span><span class="sxs-lookup"><span data-stu-id="9c6b9-121">The macro automatically adds a newline character to the output string.</span></span>

> [!Note]  
> <span data-ttu-id="9c6b9-122">Un ensemble supplémentaire de parenthèses doit contenir les paramètres de macro :</span><span class="sxs-lookup"><span data-stu-id="9c6b9-122">An additional set of parentheses must enclose the macro parameters:</span></span>

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a><span data-ttu-id="9c6b9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c6b9-123">Requirements</span></span>



| <span data-ttu-id="9c6b9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c6b9-124">Requirement</span></span> | <span data-ttu-id="9c6b9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c6b9-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6b9-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c6b9-126">Header</span></span><br/> | <dl> <span data-ttu-id="9c6b9-127"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c6b9-127"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c6b9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c6b9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c6b9-129">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="9c6b9-129">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




