---
title: Méthode WSMan. EnumerationFlagReturnEPR (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’énumération EnumerationFlagReturnEPR à utiliser dans le paramètre flags de session. Enumerate.
ms.assetid: 5e168aa9-5be1-46b3-bb9b-59895e68a75d
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode EnumerationFlagReturnEPR
- Méthode EnumerationFlagReturnEPR Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode EnumerationFlagReturnEPR
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 129aca059bcca1b1a6f6729d4df97fbf8617fa52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464306"
---
# <a name="wsmanenumerationflagreturnepr-method"></a><span data-ttu-id="7ed01-106">Méthode WSMan. EnumerationFlagReturnEPR</span><span class="sxs-lookup"><span data-stu-id="7ed01-106">WSMan.EnumerationFlagReturnEPR method</span></span>

<span data-ttu-id="7ed01-107">La méthode **EnumerationFlagReturnEPR** retourne la valeur de l’indicateur d’énumération **EnumerationFlagReturnEPR** pour une utilisation dans le paramètre *Flags* de [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="7ed01-107">The **EnumerationFlagReturnEPR** method returns the value of the enumeration flag **EnumerationFlagReturnEPR** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="7ed01-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="7ed01-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="7ed01-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7ed01-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="7ed01-110">**EnumerationFlagReturnEPR** est une constante dans l’énumération **\_ WSManEnumFlags** et est décrite dans [**constantes d’énumération**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7ed01-110">**EnumerationFlagReturnEPR** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ed01-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ed01-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagReturnEPR( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="7ed01-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ed01-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ed01-113">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7ed01-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ed01-114">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="7ed01-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ed01-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ed01-115">Return value</span></span>

<span data-ttu-id="7ed01-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7ed01-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ed01-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ed01-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ed01-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ed01-118">Requirements</span></span>



| <span data-ttu-id="7ed01-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ed01-119">Requirement</span></span> | <span data-ttu-id="7ed01-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ed01-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed01-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ed01-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed01-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ed01-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7ed01-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ed01-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed01-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ed01-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7ed01-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ed01-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ed01-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ed01-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ed01-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="7ed01-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ed01-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ed01-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7ed01-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ed01-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ed01-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7ed01-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7ed01-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7ed01-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ed01-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ed01-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ed01-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ed01-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed01-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="7ed01-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="7ed01-135">**session**</span><span class="sxs-lookup"><span data-stu-id="7ed01-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





