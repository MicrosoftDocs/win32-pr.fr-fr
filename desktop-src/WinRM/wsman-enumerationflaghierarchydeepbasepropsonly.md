---
title: Méthode WSMan. EnumerationFlagHierarchyDeepBasePropsOnly (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’énumération EnumerationFlagHierarchyDeepBasePropsOnly à utiliser dans le paramètre flags de session. Enumerate.
ms.assetid: f4c5966a-0d9f-4d93-9ccd-2e8a5f32b77f
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode EnumerationFlagHierarchyDeepBasePropsOnly
- Méthode EnumerationFlagHierarchyDeepBasePropsOnly Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode EnumerationFlagHierarchyDeepBasePropsOnly
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeepBasePropsOnly
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a0ed7d725f60e673d3426be1b11179ec8333d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510748"
---
# <a name="wsmanenumerationflaghierarchydeepbasepropsonly-method"></a><span data-ttu-id="c7e50-106">Méthode WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</span><span class="sxs-lookup"><span data-stu-id="c7e50-106">WSMan.EnumerationFlagHierarchyDeepBasePropsOnly method</span></span>

<span data-ttu-id="c7e50-107">La méthode **WSMan. EnumerationFlagHierarchyDeepBasePropsOnly** retourne la valeur de l’indicateur d’énumération **EnumerationFlagHierarchyDeepBasePropsOnly** pour une utilisation dans le paramètre *Flags* de [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="c7e50-107">The **WSMan.EnumerationFlagHierarchyDeepBasePropsOnly** method returns the value of the enumeration flag **EnumerationFlagHierarchyDeepBasePropsOnly** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="c7e50-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="c7e50-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="c7e50-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c7e50-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="c7e50-110">**EnumerationFlagHierarchyDeepBasePropsOnly** est une constante dans l’énumération **\_ WSManEnumFlags** et est décrite dans [**constantes d’énumération**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c7e50-110">**EnumerationFlagHierarchyDeepBasePropsOnly** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e50-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7e50-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyDeepBasePropsOnly( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="c7e50-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7e50-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e50-113">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c7e50-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e50-114">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="c7e50-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e50-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7e50-115">Return value</span></span>

<span data-ttu-id="c7e50-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c7e50-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c7e50-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7e50-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e50-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7e50-118">Requirements</span></span>



| <span data-ttu-id="c7e50-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7e50-119">Requirement</span></span> | <span data-ttu-id="c7e50-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7e50-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e50-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7e50-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e50-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7e50-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c7e50-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7e50-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e50-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7e50-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c7e50-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7e50-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7e50-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7e50-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7e50-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="c7e50-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7e50-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7e50-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7e50-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c7e50-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7e50-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7e50-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7e50-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c7e50-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7e50-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7e50-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7e50-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7e50-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e50-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="c7e50-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="c7e50-135">**session**</span><span class="sxs-lookup"><span data-stu-id="c7e50-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





