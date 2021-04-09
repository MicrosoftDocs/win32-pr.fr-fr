---
title: Méthode WSMan. EnumerationFlagHierarchyDeep (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’énumération EnumerationFlagHierarchyDeep à utiliser dans le paramètre flags de session. Enumerate.
ms.assetid: b84b82fa-0b2e-418e-850f-6d7a4749fdc1
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode EnumerationFlagHierarchyDeep
- Méthode EnumerationFlagHierarchyDeep Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode EnumerationFlagHierarchyDeep
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeep
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61982c6117d0a91ec253af35657f0cbbf5af12c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942709"
---
# <a name="wsmanenumerationflaghierarchydeep-method"></a><span data-ttu-id="a2262-106">Méthode WSMan. EnumerationFlagHierarchyDeep</span><span class="sxs-lookup"><span data-stu-id="a2262-106">WSMan.EnumerationFlagHierarchyDeep method</span></span>

<span data-ttu-id="a2262-107">La méthode **EnumerationFlagHierarchyDeep** retourne la valeur de l’indicateur d’énumération **EnumerationFlagHierarchyDeep** pour une utilisation dans le paramètre *Flags* de [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="a2262-107">The **EnumerationFlagHierarchyDeep** method returns the value of the enumeration flag **EnumerationFlagHierarchyDeep** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="a2262-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="a2262-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="a2262-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a2262-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="a2262-110">**EnumerationFlagHierarchyDeep** est une constante dans l’énumération **\_ WSManEnumFlags** et est décrite dans [**constantes d’énumération**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a2262-110">**EnumerationFlagHierarchyDeep** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2262-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2262-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyDeep( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="a2262-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2262-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2262-113">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a2262-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2262-114">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="a2262-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2262-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2262-115">Return value</span></span>

<span data-ttu-id="a2262-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a2262-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a2262-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a2262-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2262-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2262-118">Requirements</span></span>



| <span data-ttu-id="a2262-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2262-119">Requirement</span></span> | <span data-ttu-id="a2262-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2262-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2262-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2262-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2262-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2262-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a2262-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2262-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2262-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2262-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a2262-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2262-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2262-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2262-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2262-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="a2262-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2262-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2262-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a2262-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a2262-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2262-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a2262-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a2262-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a2262-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2262-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2262-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a2262-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2262-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2262-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="a2262-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="a2262-135">**session**</span><span class="sxs-lookup"><span data-stu-id="a2262-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





