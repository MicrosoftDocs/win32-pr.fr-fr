---
description: Met en forme les données d’instance de propriété à l’aide du formateur générique fourni par Moniteur réseau.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: FormatPropertyInstance, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515207"
---
# <a name="formatpropertyinstance-function"></a><span data-ttu-id="2fda9-103">FormatPropertyInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="2fda9-103">FormatPropertyInstance function</span></span>

<span data-ttu-id="2fda9-104">La fonction **FormatPropertyInstance** met en forme les données d’instance de propriété à l’aide du formateur générique fourni par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="2fda9-104">The **FormatPropertyInstance** function formats the property instance data using the generic formatter that Network Monitor provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fda9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fda9-105">Syntax</span></span>


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a><span data-ttu-id="2fda9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fda9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fda9-107">*lpPropertyInst* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2fda9-107">*lpPropertyInst* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fda9-108">Pointeur vers une structure [PROPERTYINST](propertyinst.md) qui contient les données d’instance.</span><span class="sxs-lookup"><span data-stu-id="2fda9-108">A pointer to a [PROPERTYINST](propertyinst.md) structure that contains the instance data.</span></span>

<span data-ttu-id="2fda9-109">En entrée, le formateur générique prend les données d’instance de l’un des membres de l’Union **PROPERTYINST** et convertit ces données en chaîne mise en forme prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="2fda9-109">On input, the generic formatter takes the instance data from one of the **PROPERTYINST** union members and converts that data to a predefined formatted string.</span></span>

<span data-ttu-id="2fda9-110">Lors de la sortie, le formateur générique définit le membre **szPropertyText** de la structure **PROPERTYINST** sur un pointeur vers la chaîne mise en forme.</span><span class="sxs-lookup"><span data-stu-id="2fda9-110">On output, the generic formatter sets the **szPropertyText** member of the **PROPERTYINST** structure to a pointer to the formatted string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fda9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fda9-111">Return value</span></span>

<span data-ttu-id="2fda9-112">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2fda9-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2fda9-113">Si la fonction échoue, la valeur de retour est un code d’erreur de NMerr. h.</span><span class="sxs-lookup"><span data-stu-id="2fda9-113">If the function is unsuccessful, the return value is an error code from NMerr.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fda9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2fda9-114">Remarks</span></span>

<span data-ttu-id="2fda9-115">La DLL de l’analyseur appelle indirectement la fonction **FormatPropertyInstance** lorsque le formateur générique est requis pour mettre en forme les données à afficher dans le volet d’informations de l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="2fda9-115">The parser DLL indirectly calls the **FormatPropertyInstance** function when the generic formatter is required to format data for display in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="2fda9-116">Pour appeler **FormatPropertyInstance** , spécifiez-le dans le membre **InstanceData** de la structure [PROPERTYINFO](propertyinfo.md) lorsque vous définissez la propriété.</span><span class="sxs-lookup"><span data-stu-id="2fda9-116">To call **FormatPropertyInstance** specify it in the **InstanceData** member of the [PROPERTYINFO](propertyinfo.md) structure when you define the property.</span></span>

> [!Note]  
> <span data-ttu-id="2fda9-117">L’analyseur ne reconnaît pas la fonction qui est appelée lorsqu’il doit mettre en forme une instance d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="2fda9-117">The parser does not recognize which function is called when it must format an instance of a property.</span></span> <span data-ttu-id="2fda9-118">La fonction peut être **FormatPropertyInstance** ou une fonction de format personnalisée définie par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="2fda9-118">The function can be **FormatPropertyInstance** or a custom format function defined by the parser.</span></span> <span data-ttu-id="2fda9-119">L’analyseur appelle la fonction de format spécifiée par le membre **InstanceData** de la structure **PROPERTYINFO** pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="2fda9-119">The parser calls whatever format function is specified by the **InstanceData** member of the **PROPERTYINFO** structure for the property.</span></span>

 

<span data-ttu-id="2fda9-120">Pour plus d’informations et pour obtenir un exemple d’implémentation de [formatproperties](formatproperties.md), consultez [implémentation de formatproperties](implementing-formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="2fda9-120">For more information and an example of how to implement [formatproperties](formatproperties.md), see [Implementing FormatProperties](implementing-formatproperties.md).</span></span> <span data-ttu-id="2fda9-121">Pour plus d’informations sur la façon dont le formateur générique met en forme les différents types de données, consultez [sortie du formateur générique](generic-formatter-output.md).</span><span class="sxs-lookup"><span data-stu-id="2fda9-121">For more information about how the generic formatter formats different types of data, see [Generic Formatter Output](generic-formatter-output.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fda9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fda9-122">Requirements</span></span>



| <span data-ttu-id="2fda9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fda9-123">Requirement</span></span> | <span data-ttu-id="2fda9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fda9-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2fda9-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fda9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2fda9-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fda9-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2fda9-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fda9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2fda9-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fda9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2fda9-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fda9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fda9-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fda9-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2fda9-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2fda9-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2fda9-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fda9-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2fda9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2fda9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fda9-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fda9-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fda9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fda9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fda9-136">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="2fda9-136">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="2fda9-137">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="2fda9-137">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




