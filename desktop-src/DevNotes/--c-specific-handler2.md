---
description: Appelé par le compilateur pour implémenter des extensions de gestion structurée des exceptions.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: Fonction __C_specific_handler (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542298"
---
# <a name="__c_specific_handler-function"></a><span data-ttu-id="1fb3c-103">\_\_\_Fonction de gestionnaire spécifique à C \_</span><span class="sxs-lookup"><span data-stu-id="1fb3c-103">\_\_C\_specific\_handler function</span></span>

<span data-ttu-id="1fb3c-104">Appelé par le compilateur pour implémenter des extensions de gestion structurée des exceptions.</span><span class="sxs-lookup"><span data-stu-id="1fb3c-104">Called by the compiler to implement structured exception handling extensions.</span></span>

<span data-ttu-id="1fb3c-105">L’adresse relative du gestionnaire spécifique au langage est présente dans les informations de déroulement \_ chaque fois que Flags UNW Flag \_ \_ EHANDLER ou UNW \_ Flag \_ UHANDLER sont définis.</span><span class="sxs-lookup"><span data-stu-id="1fb3c-105">The relative address of the language specific handler is present in the UNWIND\_INFO whenever flags UNW\_FLAG\_EHANDLER or UNW\_FLAG\_UHANDLER are set.</span></span> <span data-ttu-id="1fb3c-106">Le gestionnaire spécifique au langage est appelé dans le cadre de la recherche d’un gestionnaire d’exceptions ou dans le cadre d’un déroulement.</span><span class="sxs-lookup"><span data-stu-id="1fb3c-106">The language specific handler is called as part of the search for an exception handler or as part of an unwind.</span></span> <span data-ttu-id="1fb3c-107">Pour plus d’informations, consultez [gestionnaire spécifique](/cpp/build/language-specific-handler)à une langue.</span><span class="sxs-lookup"><span data-stu-id="1fb3c-107">For more information see [Language Specific Handler](/cpp/build/language-specific-handler).</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb3c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fb3c-108">Syntax</span></span>


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a><span data-ttu-id="1fb3c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fb3c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fb3c-110">*ExceptionRecord* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fb3c-110">*ExceptionRecord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb3c-111">Fournit un pointeur vers un enregistrement d’exception, qui a la définition Win64 standard.</span><span class="sxs-lookup"><span data-stu-id="1fb3c-111">Supplies a pointer to an exception record, which has the standard Win64 definition.</span></span>

</dd> <dt>

<span data-ttu-id="1fb3c-112">*EstablisherFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fb3c-112">*EstablisherFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb3c-113">Adresse de la base de l’allocation de pile fixe pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1fb3c-113">The address of the base of the fixed stack allocation for this function.</span></span>

</dd> <dt>

<span data-ttu-id="1fb3c-114">*ContextRecord* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1fb3c-114">*ContextRecord* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb3c-115">Pointe vers le contexte d’exception au moment où l’exception a été levée (dans le cas du gestionnaire d’exceptions) ou dans le contexte de « déroulement » actuel (dans le cas du gestionnaire de terminaisons).</span><span class="sxs-lookup"><span data-stu-id="1fb3c-115">Points to the exception context at the time the exception was raised (in the exception handler case) or the current "unwind" context (in the termination handler case).</span></span>

</dd> <dt>

<span data-ttu-id="1fb3c-116">*DispatcherContext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1fb3c-116">*DispatcherContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb3c-117">Pointe vers le contexte du répartiteur pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1fb3c-117">Points to the dispatcher context for this function.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fb3c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fb3c-118">Requirements</span></span>



| <span data-ttu-id="1fb3c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fb3c-119">Requirement</span></span> | <span data-ttu-id="1fb3c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fb3c-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb3c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fb3c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1fb3c-122"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3c-122"><dt>Wdm.h</dt></span></span> </dl>        |
| <span data-ttu-id="1fb3c-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1fb3c-123">Library</span></span><br/> | <dl> <span data-ttu-id="1fb3c-124"><dt>NtosKrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3c-124"><dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="1fb3c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1fb3c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1fb3c-126"><dt>Ntoskrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3c-126"><dt>Ntoskrnl.exe</dt></span></span> </dl> |



 

