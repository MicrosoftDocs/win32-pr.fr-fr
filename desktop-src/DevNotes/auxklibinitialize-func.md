---
description: Initialise la \_ bibliothèque klib.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Fonction AuxKlibInitialize (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540645"
---
# <a name="auxklibinitialize-function"></a><span data-ttu-id="999e4-103">AuxKlibInitialize fonction)</span><span class="sxs-lookup"><span data-stu-id="999e4-103">AuxKlibInitialize function</span></span>

<span data-ttu-id="999e4-104">Initialise la \_ bibliothèque klib.</span><span class="sxs-lookup"><span data-stu-id="999e4-104">Initializes the Aux\_klib library.</span></span> <span data-ttu-id="999e4-105">Cette fonction doit être appelée avant que toute autre fonction de la bibliothèque puisse être appelée.</span><span class="sxs-lookup"><span data-stu-id="999e4-105">This function must be called before any other function in the library can be called.</span></span>

## <a name="syntax"></a><span data-ttu-id="999e4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="999e4-106">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="999e4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="999e4-107">Parameters</span></span>

<span data-ttu-id="999e4-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="999e4-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="999e4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="999e4-109">Return value</span></span>

<span data-ttu-id="999e4-110">Si la fonction réussit, la valeur de retour est STATUs \_ successful.</span><span class="sxs-lookup"><span data-stu-id="999e4-110">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="999e4-111">Si la fonction échoue, la valeur de retour peut être l’un des codes d’État définis dans Ntstatus. h, qui est disponible dans le kit WDK.</span><span class="sxs-lookup"><span data-stu-id="999e4-111">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="999e4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="999e4-112">Remarks</span></span>

<span data-ttu-id="999e4-113">La bibliothèque d’objets qui implémente cette API peut être téléchargée à partir d' [ici](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="999e4-113">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="999e4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="999e4-114">Requirements</span></span>



| <span data-ttu-id="999e4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="999e4-115">Requirement</span></span> | <span data-ttu-id="999e4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="999e4-116">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="999e4-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="999e4-117">Redistributable</span></span><br/> | <span data-ttu-id="999e4-118">Bibliothèque d’API auxiliaires Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="999e4-118">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="999e4-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="999e4-119">Header</span></span><br/>          | <dl> <span data-ttu-id="999e4-120"><dt>Aux \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="999e4-120"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="999e4-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="999e4-121">Library</span></span><br/>         | <dl> <span data-ttu-id="999e4-122"><dt>Aux \_ klib. lib</dt></span><span class="sxs-lookup"><span data-stu-id="999e4-122"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="999e4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="999e4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="999e4-124">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="999e4-124">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




